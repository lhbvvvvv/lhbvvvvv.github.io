---
title: Jekyll + Github搭建个人博客
date: 2023-03-23T00:55:42+08:00 # 2022-01-01 13:14:15 +0800 只写日期也行；不写秒也行；这样也行 2022-03-09T00:55:42+08:00
categories: [工具, blog]
tags: [blog]     # TAG names should always be lowercase


author: # 不写默认就是自己
  name: lhb
  link: https://github.com/lhbvvvvv

# # 以下默认false
# math: true
# mermaid: true
# pin: true
---
## 一、Jekyll安装
1. 下载[Ruby+Devkit](https://rubyinstaller.org/downloads/)，按照默认选项即可，下载到本地的位置可以进行调整。
2. 在cmd中运行 `ridk install`。
3. 在cmd中运行 `gem install jekyll bundler` 安装 Jekyll 和 Bundler。
4. 在cmd中输入 `jekyll -v` 显示版本号表明安装成功。

## 二、利用Jekyll模板搭建博客
在GiThub上搜索jekyll，可以找到很多的jekyll模板，这里我选择的是[chirpy](https://github.com/cotes2020/jekyll-theme-chirpy)。Wiki中的Getting Started有使用的教程，主要是以下内容：
> Sign in to GitHub and browse to Chirpy Starter[https://github.com/cotes2020/chirpy-starter], click the button Use this template > Create a new repository, and name the new repository USERNAME.github.io, where USERNAME represents your GitHub username.

完成上面的操作将新创建的仓库clone到本地执行命令 `bundle`。由于是在Windows上运行，但GitHub pages是在linux上部署的，需要运行以下命令来添加 x86_64-linux 下的一些库：
```
bundle lock --add-platform x86_64-linux
```
Jekyll的主要配置信息是在根目录下的`_config.yml`文件中，在完全不更改配置直接push回仓库后，我访问github pages部署后的页面只显示了以下内容：
```
---
layout: home
# Index page
---
```