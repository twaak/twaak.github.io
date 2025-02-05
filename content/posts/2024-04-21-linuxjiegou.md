---
title: "Linux 文件系统结构"
draft: false
date: 2024-08-05
description: "Linux文件系统结构"
tags: ["Linux"]
categories: ["技术分享"]
---




Linux文件系统的结构是一个层次化的目录树，所有文件和目录都从根目录（/）开始。以下是一些主要的目录及其作用：  

### 根目录 `/`

这是文件系统的起点，所有其他目录和文件都从这里派生出来。

### `/bin`

存放基本的用户命令，如`ls`, `cp`, `mv`, `rm`等。这些命令在单用户模式和所有用户环境中都可用。

### `/sbin`

存放系统管理员使用的基本命令，如`ifconfig`, `reboot`, `shutdown`等。普通用户一般没有权限执行这些命令。

### `/etc`

存放系统配置文件和子目录。例如，`/etc/passwd`文件包含用户账号信息，`/etc/fstab`文件包含文件系统挂载信息。

### `/home`

存放用户的主目录，每个用户都有一个单独的子目录。例如，用户`alice`的主目录是`/home/alice`。

### `/root`

系统管理员（root用户）的主目录。与普通用户的主目录不同，root用户的主目录位于根目录下。

### `/var`

存放可变数据文件，如日志文件、邮件、临时文件等。常见的子目录有`/var/log`（日志文件）和`/var/tmp`（临时文件）。

### `/tmp`

存放临时文件，系统重启后这些文件通常会被删除。任何用户和应用程序都可以在此创建临时文件。

### `/usr`

存放用户级别的应用程序和文件。常见的子目录有：

- `/usr/bin`: 用户命令。
- `/usr/sbin`: 系统管理员命令。
- `/usr/lib`: 库文件。
- `/usr/share`: 共享数据，如文档和配置文件。
- `/usr/local`: 本地安装的软件和文件，与系统默认软件分开。

### `/lib`

存放系统引导和运行时所需的共享库文件和内核模块。

### `/opt`

存放附加的应用程序软件包。通常用于安装大型第三方软件包。

### `/mnt`

用于临时挂载文件系统。系统管理员可以在此挂载临时文件系统，如光盘或其他存储设备。

### `/media`

用于自动挂载的可移动媒体设备，如U盘、光盘等。现代Linux发行版通常会自动在此目录下创建子目录来挂载这些设备。

### `/dev`

存放设备文件，表示系统中的硬件设备。常见的设备文件有硬盘设备（如`/dev/sda`）、终端设备（如`/dev/tty`）等。

### `/proc`

一个虚拟文件系统，包含系统内核和进程的信息。它动态生成内容，提供系统和进程信息的接口。

### `/sys`

另一个虚拟文件系统，提供设备和内核信息的接口。它主要用于内核和硬件设备的配置和管理。

### `/boot`

存放引导加载程序和内核文件，如`vmlinuz`（内核映像）和`initrd`（初始RAM磁盘）。

### `/srv`

存放系统提供的服务相关的数据，如Web服务器的数据文件。
