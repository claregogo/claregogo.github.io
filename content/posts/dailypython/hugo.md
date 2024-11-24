---
date: '2024-11-24T20:05:01+08:00'
draft: false
title: 'Hugo'
---
以下是使用Markdown格式排版的Hugo制作网站教程：


# 简单的Hugo制作网站教程 - Mac电脑

## 1. 下载Hugo
根据[官网](https://gohugo.io/installation/macos/)教程下载Hugo。

## 2. 创建文件目录
打开终端（cmd+空格）并输入以下命令创建文件目录：
```bash
mkdir ~/Desktop/MyFolder
cd ~/Desktop/MyFolder
```

## 3. 创建Hugo站点
在当前文件夹中创建一个新的Hugo站点：
```bash
hugo new site MyFreshWebsite --format yaml
```
> 将 `MyFreshWebsite` 替换为你的网站名称。

## 4. 添加主题
将PaperMod主题添加到你的站点中：
```bash
git submodule add https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod
```
> 将上面的URL替换为你选择的主题的URL。

## 5. 配置站点
按照[PaperMod的示例配置](https://github.com/adityatelange/hugo-PaperMod/blob/exampleSite/content/archives.md?plain=1)修改自己的 `config.yaml` 配置文件。

## 6. GitHub部署

### 新建一个GitHub仓库
- 新建一个仓库，仓库名称应该是 `<username.github.io>`。

### 初始化Git
在站点目录中执行以下命令初始化Git仓库：
```bash
git init
git remote add origin https://github.com/yourusername/mywebsite.git
git remote -v
git add .
git commit -m "Initial commit"
git push -u origin main
```
> 替换为你自己的GitHub用户名和仓库地址。

### 配置GitHub Pages
1. 打开GitHub仓库，进入 `Settings`。
2. 在 `Pages` 部分，选择 `GitHub Actions` 作为部署方式。

### 创建工作流
在GitHub的 `Pages` 部分旁边，点击 `Create your workflow`，命名为 `hugo.yaml`，然后复制并粘贴[官网的Step 6](https://gohugo.io/hosting-and-deployment/hosting-on-github/)的内容。

## 7. 上传图片
你可以将图片上传到GitHub，注意使用 `raw` 格式复制图片链接，这样才能在网站中正确显示图片。


## 8. 后续有更新
```
git add .
git commit -m "Initial commit"
git pull origin main
git push -u origin main --force
```
