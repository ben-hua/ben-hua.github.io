---
title: 使用Hexo建立的静态Blog网站
comments: true
date: 2024-12-25 14:35:34
tags:
    - hexo
    - 建站
categories:
    - 建站
keywords:
description: 第一次使用Hexo，记录一下过程吧
top_img:
cover:
abbrlink:
---

## 在Github创建一个仓库

废话不多说，自己看[Github Pages官方文档](https://pages.github.com/)

## Hexo创建一个静态blog框架

很简单，还是看[Hexo官方文档](https://hexo.io/zh-cn/docs/setup)

添加一个页面

```bash
hexo new create-blog-by-hexo
```

## 添加主题样式-butterfly

默认样式不太喜欢，可以在Hexo官网或者Github找自己喜欢的主题样式。

Ben哥找了一圈，比较喜欢的主题[hexo-theme-butterfly](https://github.com/jerryc127/hexo-theme-butterfly)样式。

跟着它的配置文档搞一遍，根据自己的喜好，调一调配置。

## 使用Github Actions部署到 Github Pages

这里还是参考[Hexo 发布Github Pages的文档](https://hexo.io/zh-cn/docs/github-pages)

## 其他问题

+ 指定文件原样复制，跳过Hexo文件渲染

    位于source下的文件，会被Hexo使用theme的样式进行渲染，如果希望某一个html文件原样复制到根目录，则需要如下配置

    ```yml
    skip_render:
        - googled68ab6c92601eab5.html
    ```

+ 覆盖Themes中的样式
    - 新增样式文件 source/css/custom.css
    - 添加配置

        ```yml
        inject:
            head:
                - <link rel="stylesheet" href="/css/custom.css">
        ```

## 参考文献

+ [Github Pages](https://pages.github.com/)
+ [Hexo官网](https://hexo.io/zh-cn/)
+ [Butterfly主题样式](https://github.com/jerryc127/hexo-theme-butterfly)
