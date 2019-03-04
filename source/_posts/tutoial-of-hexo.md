---
title: 利用Hexo+Github搭建个人免费博客
date: 2019-02-15 14:41:24
tags:
---
# 前言
本篇blog将记录个人静态博客的搭建方法,包括：

* Github静态博客是什么，为什么选择Hexo？
* Hexo搭建过程
* Hexo使用方法

<!--more-->

# GitHub静态博客是什么，为什么选择Hexo？
GitHub作为全球最大的程序员交友网站，是一个代码托管平台和开发者社区，开发者可以在Github上创建自己的开源项目并与其他开发者协作编码，同时它也提供了很多服务，其中Pages就是其中一个服务，它提供了免费的托管空间可以用来存放静态博客站点的数据，使用GitHub Pages技术搭建静态博客站点的好处有：

* 多达1G的免费空间。
* 每月100GB的流量。
* 利用GitHub的数据存储备份功能，保证数据的安全。

具体的介绍可以参考[GitHub Pages](https://help.github.com/articles/what-is-github-pages/).

在[Hexo](https://help.github.com/articles/what-is-github-pages/)之前GitHub内置支持的静态网页生成引擎是Jekyll，参考[三脚猫](https://www.jianshu.com/p/b0cae7168352)相比较Jekyll而言，Hexo更容易入手，也更方便配置，顾本人更倾向于使用Hexo。另外Hexo也支持多线备份，可以同步到多个git仓库中，实现境内境外双线解析镜像，不过该功能还未体验。

# Hexo搭建过程
本人是mac系统，参考[全民博客时代的到来——20分钟简要教程](https://www.jianshu.com/p/e99ed60390a8),一步一步下来，将下列工具准备齐全：

* git
* npm
* hexo

在部署hexo过程中可能会遇到一些错误，根据npm提示或者google一些基本就可以解决了。

关于Hexo源代码的保存问题，可以参考[保存Hexo博客源码到Github上](https://www.jianshu.com/p/3c827e38a852)，创建一个新的分支，将代码存入新的分支中，保留master给GitHub Pages引擎用作渲染用。
在实际操作中，该文章中的一些git方法可以根据实际情况进行调整，这里需要掌握一些git的基本语法。

# Hexo使用方法
参考Hexo[帮助](https://hexo.io/zh-cn/docs/)

## 文档结构
安装完Hexo后的目录结构如下：

```
.
├── _config.yml
├── package.json
├── scaffolds
├── source
|   └── _posts
|   └── _drafts (自建添加)
└── themes
└── public
```

### _config.yml
用于记录网站的配置信息

### package.json
node包的信息

### scaffolds
**模版** 文件夹。当您新建文章时，Hexo 会根据 scaffold 来建立文件。

### source
存放用户markdown文件的地方，除 _posts 文件夹之外，开头命名为 _ (下划线)的文件 / 文件夹和隐藏的文件将会被忽略。Markdown 和 HTML 文件会被解析并放到 public 文件夹，而其他文件会被拷贝过去。

可以建立一个_drafts文件夹，存放草稿文件。

### public
发布的文件，最终这些文件将上传到GitHub Page中进行同步。

## 配置参数
配置参数可以[参考](https://hexo.io/zh-cn/docs/configuration)
关于绑定域名，设置搜索选项时，在后续完成的时候再介绍。

## 命令
Hexo命令可以[参考](https://hexo.io/zh-cn/docs/commands)
可以利用一些短命令，比如：

```
hexo g -d
```
实现安装和部署。

更多的命令速查可以参考这个[cheatsheet](https://lvraikkonen.github.io/2017/06/05/Hexo-command-Cheatsheet/)

另外一篇[cheatsheet](https://neo.works/pages/Hexo-Blogging-Cheatsheet/#frequently-used-emoji)中的Emoji也比较有用。