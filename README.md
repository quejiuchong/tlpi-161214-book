# tlpi-161214-book
The Linux Programming Interface Source Code (LINUX/UNIX 系统编程手册源码)

## 概述
个人学习代码库，来源于 [The Linux Programming Interface Source Code (LINUX/UNIX 系统编程手册)](http://man7.org/tlpi/code/index.html)

以下说明与修改适用于 CentOS 6.7 系统 (minimal install)：

* 基础环境安装 :
  - sudo yum update -y
  - sudo yum install gcc gcc-c++ svn git opensssl curl wget
  - sudo yum install libacl-devel libcap-devel


* 源码修改 :  
  - 警告消除 : 为出现 `warning: "_XOPEN_SOURCE" redefined` 警告的文件添加重复定义保护
```
#if ! defined(_XOPEN_SOURCE) || _XOPEN_SOURCE < 500
#define _XOPEN_SOURCE 500
#endif
```
