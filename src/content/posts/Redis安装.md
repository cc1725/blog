---
title: Git安装
published: 2024-07-05
description: ''
image: ''
tags: []
category: '服务器软件安装'
draft: false 
---


# 方式一：通过包管理器安装
yum install git
方式二：
1、准备Git安装包上传到服务器：git-2.28.0.tar.gz
tar -zxvf git-2.28.0.tar.gz
2、提前安装可能所需的依赖
yum install curl-devel expat-devel gettext-devel openssl-devel zlib-devel gcc-c++ perl-ExtUtils-MakeMaker
3、编译安装Git
cd git-2.28.0/
make configure
./configure --prefix=/usr/local/git
make profix=/usr/local/git
make install
4、配置环境变量
vim /etc/profile
export GIT_HOME=/usr/local/git
export PATH=$PATH:$GIT_HOME/bin
source /etc/profile
5、查看安装结果
执⾏ git --version 查看安装后的版本即可
