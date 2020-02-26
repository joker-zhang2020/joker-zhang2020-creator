---
title: "小张的博客"
date: 2020-02-22T20:50:01+08:00
draft: false
---

# 如何用 hugo 搭建个人博客

<hr>

hugo是GO语言实现的一个博客生成器，是世界上最快的博客生成器。

其搭建个人博客的流程如下：

1. 安装hugo，分两种系统进行：
    > mac电脑运行  `brew install hugo`
    > windows 电脑去 Hugo releases 页面下载 hugo_xxx_windows-64bit.aip
    > 解压，建立单独的安装目录并妥存
    > 把其根目录加到 PATH 中
    > 重启终端，运行 hugo version 查看版本
2. 进入 hugo 官网，点击 Quick Start 快速开始，按照文档进行操作 <br>
   
   ## 搭建本地博客 
   

   <hr>


    - hugo new site 仓库名.github.io-creator (仓库名为github用户名全小写。)
    - cd 仓库名.github.io-creator/
    - git init
    - git submodule add http://github.com/budparr/gohugo-theme-ananke.git themes/ananke  (添加主题)
    - echo 'theme = "ananke"' >> config.toml
    - hugo new posts/博客文件名.md (创建文档名)
    - code themes/ananke/theme.toml  在 0.30.2 两边添加双引号
    - 重新运行 hugo new posts/博客文件名.md
    - 添加博客内容并将draft值改成false，表示这篇文档不是草稿。
    - hugo server -D (不要关闭这个终端，否则无法浏览，终端底部有url地址可以预览自己博客，自此本地博客搭建成功)
    - 搜索 config.toml 将languagecode 内容改成 zh-Hans 表示网页内容为中文。 han 表示中文，s 表示简体。
    - 新打开终端，运行命令 hugo
  <br>

  <hr>

  ## 上传博客到github

  - cd public
  - 在根目录建立 .gitignore 并在里面添加 /public/ 将public作为独立的仓库
  - git init
  - git add .
  - git commit -v
  - github新建仓库，仓库名为--用户名.github.io--名称是固定的，用户名为全小写
  - 将public上传到github仓库
  - setting ---> github pages ---> source --> 勾选 master branch --> 点选上部地址。搭建完毕。

   <br>
 
    流程：
    1. 搭建本地仓库（hugo官网教程）；
    2. 制作编辑 public ，放到忽略里面 ；
    3. 上传 github
    4. 开启 github pages 功能

   