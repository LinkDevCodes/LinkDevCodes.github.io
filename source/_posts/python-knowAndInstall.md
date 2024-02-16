---
title: python的初步认知及安装与执行
excerpt: 本篇会介绍python的基本介绍与安装教程
date: 2024-2-11
categories:
- 编程
tags:
- python
---

## 什么是编程语言
编程语言是一种**形式化**的语言，它定义了计算机程序的执行流程。
> 这种语言使得程序员能够精确地定义计算机所需使用的数据以及在不同情况下所应当采取的行动。编程语言是计算机和人都能识别的语言，它允许程序员编写算法以实现特定的目标或完成特定的任务。

每种编程语言都包含一整套词汇和语法规范，这些规范通常包括数据类型和数据结构、指令类型和指令控制、调用机制和库函数以及不成文的规定(如递进书写、变量命名等)。
> 编程语言的描述通常分为语法和语义两个部分。编程语言可以简单地理解为一种计算机和人都能识别的语言，它让程序员能够准确地定义计算机所需要使用的数据，并精确地定义在不同情况下所应当采取的行动。

## 编译器与解释器
### 解释器
- 解释器是直接执行用编程语言编写的指令的程序
- 解释器的程序总是需要解释器来运行。若想要解释语言的程序独立运行，就需要依赖第三方库，如python中打包成Windows平台下的exe文件，需要依赖*pyinstaller*或者*py2exe* ~~(小声嘟囔:作者更喜欢py2exe)~~

### 编译器
- 编译器是把源代码翻译成更低级语言的程序
- 编译器生成一个独立的程序，编译完成后便不再需要依赖编译器。

## Python简介
Python由荷兰国家数学与计算机科学研究中心的吉多·范罗苏姆于1990年代初设计，作为一门叫做ABC语言的替代品。Python提供了高效的高级数据结构，还能简单有效地面向对象编程。Python语法和动态类型，以及解释型语言的本质，使它成为多数平台上写脚本和快速开发应用的编程语言，随着版本的不断更新和语言新功能的添加，逐渐被用于独立的、大型项目的开发。
> 1. Python在各个编程语言中比较适合新手学习，Python解释器易于扩展，可以使用C、C++或其他可以通过C调用的语言扩展新的功能和数据类型。
2. Python也可用于可定制化软件中的扩展程序语言。
3. Python丰富的标准库，提供了适用于各个主要系统平台的源码或机器码。

(介绍转自[百度百科](baiduboxapp://swan/AZQtr4jkpf90T3X9QMWVLF1bkeV4LXxD/pages/lemma/lemma?lemmaTitle=Python&lemmaId=407313&fr=ge_ala&_baiduboxapp=%7B%22from%22%3A%221081000900000000%22%2C%22ext%22%3A%7B%22searchid%22%3A%228656030703587729271%22%2C%22tplname%22%3A%22sg_kg_entity_san%22%2C%22srcid%22%3A51527%2C%22order%22%3A%221%22%2C%22token%22%3A%22swanubc%22%2C%22url%22%3A%22https%3A%2F%2FAZQtr4jkpf90T3X9QMWVLF1bkeV4LXxD.smartapps.cn%2Fpages%2Flemma%2Flemma%3FlemmaTitle%3DPython%26lemmaId%3D407313%26fr%3Dge_ala%22%2C%22third_ext%22%3A%7B%22ivkSource%22%3A%22h5_schema%22%2C%22token%22%3A%22swanubc%22%2C%22pd%22%3A%22wise%22%7D%2C%22referpd%22%3A%22A%22%2C%22searchQueryEnc%22%3A%22gavDigulBi_KODjW8rmYqk-4rXq4KDbIC_new%22%2C%22urlsign%22%3A%224521512210513296692%22%7D%2C%22sysExt%22%3A%7B%22sessionId%22%3A%22lid%5B8656030703587729271%5D_si%5B51527%5D%22%7D%7D&callback=_bdbox_js_8158&oauthType=search&searchParams=%7B%22failUrl%22%3A%22https%3A%2F%2Fbaike.baidu.com%2Fitem%2FPython%2F407313%3Ffr%3Dge_ala%22%2C%22logParams%22%3A%22pu%3D%24pu%26baiduid%3D%24baiduid%26tcreq4log%3D1%26isAtom%3D1%26cyc%3D1%26mpv%3D1%26p_sv%3D29%26branchname%3Dbaiduboxapp%26clk_info%3D%7B%5C%22tplname%5C%22%3A%5C%22sg_kg_entity_san%5C%22%2C%5C%22srcid%5C%22%3A51527%2C%5C%22ivkStatus%5C%22%3A%5C%22new_ivk_success%5C%22%2C%5C%22type%5C%22%3A%5C%22xcx%5C%22%2C%5C%22naType%5C%22%3A%5C%22%5C%22%2C%5C%22ivkSource%5C%22%3A%5C%22h5_schema%5C%22%2C%5C%22urlsign%5C%22%3A%5C%224521512210513296692%5C%22%2C%5C%22jumpType%5C%22%3A%5C%22xcx%5C%22%2C%5C%22jumpId%5C%22%3A110%2C%5C%22xcx_path%5C%22%3A%5C%22%25252Fpages%25252Flemma%25252Flemma%5C%22%2C%5C%22xcx_id%5C%22%3A%5C%22AZQtr4jkpf90T3X9QMWVLF1bkeV4LXxD%5C%22%2C%5C%22xcx_from%5C%22%3A%5C%221081000900000000%5C%22%7D%26lid%3D8656030703587729271%26l%3D1%26t%3Dzbios%26ref%3Dwww_zbios%26from%3D1013672s%26order%3D1%26w%3D0_10_python%E7%AE%80%E4%BB%8B%26tj%3Dsg_kg_entity_san_1_0_10_l%26src%3Dhttps%25253A%25252F%25252Fbaike.baidu.com%25252Fitem%25252FPython%25252F407313%25253Ffr%25253Dge_ala%22%7D&useTpl=1> ))

## python的安装
python的安装通常分为命令行安装与安装包安装，不同的操作系统安装方式也有所不同。(下面介绍Windows平台和类Unix平台的安装方法)
### Windows操作系统
在这种图形化水平极高的操作系统中，我推荐不使用命令行安装我推荐直接下载***web installer***(网络安装包)或者是***offline installer***(离线安装包)，一步步依照它的引导一步步安装即可，这里推荐才用快速安装，即默认选项，因为初学，各位无须对做更多的配置。如果选择自定义安装且操作不当的话可能会产生很多不必要的麻烦，如果你想知道是什么麻烦，你可以问问3年前的我，其实通俗来说就是~~没法用~~
### 类Unix操作系统
#### Linux平台
##### python包的获取
python预装在大多数Linux发行版上，并作为一个包提供给所有其他用户。 但是各位可能想要使用的某些功能在发行版提供的软件包中不可用。这时您可以选择通过源代码来编译最新版本的python。
如果Python没有预先安装并且不在发行版提供的库中，您可以使用发行版的创建包。具体内容可以参考官方的文档
> - [Debain](https://www.debian.org/doc/manuals/maint-guide/first.en.html)用户通道
> - [OpenSuse](https://en.opensuse.org/Portal:Packaging)用户通道
> - [Fedora](https://docs.fedoraproject.org/en-US/package-maintainers/Packaging_Tutorial_GNU_Hello/)用户通道
> - [Slackware](https://slackbook.org/html/package-management-making-packages.html)用户通道

如果你是使用的Ubuntu发行版本(作者自己在使用)，那么你可通过在终端执行下面指令来安装python。
```
sudo apt-get install python3
```
#### FreeBSD平台
你可以使用下面的指令来添加包
```
pkg install python3
```
#### OpenBSD平台
你可以使用下面的指令来添加包
```
pkg_add -r python
pkg_add ftp://ftp.openbsd.org/pub/OpenBSD/4.2/packages/<architecture>/<version>.tgz
```
对于用"<"与">"括起来的参数是核心架构与python版本，下面以i386获取python3.8的可用版本为例
```
pkg_add ftp://ftp.openbsd.org/pub/OpenBSD/4.2/packages/i386/python-3.8p2.tgz
```
##### python解释器的编译
执行下列指令进行编译python
```
./configure
make
make install
```
##### python权限的添加
执行下列的指令来为python添加权限
```
chmod +x script
```
并在脚本的顶部放置一个合适的Shebang线。一个很好的选择通常是: *#!/usr/bin/env python3*
将在整个**PATH**中搜索Python解释器。但是某些Unix系统可能没有**env**命令，因此可能需要将***/usr/bin/python3***硬编码为解释器路径。

## python的执行
### Windows平台
把打开方式换位python解释器即可(命令行执行也可以，但是你用的是Windows，那又何必呢？编程万事从简)
### Linux平台
终端执行指令来运行python文件，<file>是你文件的路径。其中 **-u** 的意思是赋予你的python程序以管理员的权限，比如删除文件之类的如果没有 **-u** 参数的话，是会报错的，加上 **-u** 可以解决很多因为权限引起的不必要麻烦。
```
python -u <file>
python2 -u <file>
python3 -u <file>
```
前面具体的内容依据你所安装的python版本与系统配置。如果依照教程应该使用python3。

## 作者的私货
python是作者第一名会的编程语言，至今我曾用java给Minecraft写过mod。也是OIer(信息学奥赛选手)，会打C++。这些语言给我最大的感触是，他们有着相同的最底层的逻辑，但是每个语言都有自己的特点。学会一门语言后，其实学习其他语言就很快了，但是有时候可能会串台，近段时间比赛，所以平时写的都是C++，突然回来写python，有时候冷不冷丁突然手顺势打个分号，给条件外加个分号，还挺好笑的，~~嘻嘻嘻~~（作者偷笑）

## 小结
你的**python**的**基本安装**与**基本认知**已经通关了。那么下面我们就可以正式的学习python这门语言。在日后的讲解中，我可能会在举例或是讲解中，将python与C++等语言作对比，让大家更好的了解python这门语言的特点。同时，在后续的讲解过程中我会尽可能避免一些非常专业且晦涩难懂的表述，便于大家理解。本人也会在每章末做一个术语及习惯通注，帮助大家理解。

此教程面向大众，可能存在作者的一些个人见解与不专业的表达，请专业人士谅解，如有错误请转至 [**关于页面**](https://LinkDevCodes.github.io/about) 来联系作者。
