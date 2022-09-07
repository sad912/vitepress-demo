# 初识 VitePress
VuePress 作为基于 Vue 和 Webpack 驱动的静态网站生成器，为编写静态网站提供了极大的便利，但随着 Vite 的发布，使得基于 Webpack 驱动的 VuePress 稍显逊色，基于 Vite 和 Vue 3 的 VitePress 应运而生。

本文通过简单的 demo 来介绍 VitePress 的基本用法。

## 最简单的 VitePress 应用


首先，创建一个空项目 `vitepress-demo` 并进行初始化。

```Bash
mkdir vitepress-demo && cd vitepress-demo
pnpm init
```


安装 VitePress。

```Bash
pnpm add -D vitepress vue
```


在 package.json 中添加 VitePress 命令

```Bash
{
  ...
  "scripts": {
    "docs:dev": "vitepress dev docs",
    "docs:build": "vitepress build docs",
    "docs:serve": "vitepress serve docs"
  },
  ...
}
```


启动。

```Bash
pnpm docs:dev
```


可以看到，VitePress 已经启动了，不过目前 VitePress 中没有任何静态文档。

![image](https://res.craft.do/user/full/3a190bec-5a1d-c7ff-6eba-777c2791ff14/doc/F6996CE6-62CA-4B7F-9976-B2079332630C/AADA5DB0-70E6-4279-AD60-5C25DE73160F_2/FQ7a6dSlLnz7egM8xvL2Bv1fVp4FxbfcKR33TOp39asz/Image.png)

添加文档。

```Bash
mkdir docs && echo '# Hello VitePress' > docs/index.md
```


![image](https://res.craft.do/user/full/3a190bec-5a1d-c7ff-6eba-777c2791ff14/doc/F6996CE6-62CA-4B7F-9976-B2079332630C/87E4CA26-2166-4903-8C71-21E600D8511A_2/7LJAJtoZdXP0YXiYBO318zJbkliBcmF2l5HvEp8ITSYz/Image.png)

添加配置文件。

```Bash
mkdir docs/.vitepress
touch docs/.vitepress/config.js
```


在 `config.js` 中添加简单的配置。

```javascript
export default {
  title: 'VitePress Demo',
  description: 'VitePress Getting Started'
}
```


至此，最简单的一个基于 VitePress 本地静态网站就实现了。
