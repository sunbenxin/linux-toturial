# linux-toturial


### linux 简介
- linux 内核主要模块(进程调度，内存管理，虚拟文件系统，网络接口，进程间通信)

### 文件系统
- fdisk 查看当前磁盘的情况（fdisk -l)
- linux下存储设备的某个分区格式化为文件系统后，有两个主要概念：索引节点和块。
    块用来存储数据
    索引节点用来存储数据的信息，包括文件的大小，属主，归属的用户组，读写权限等。
    索引节点为每个文件进行信息索引，所以就有了索引节点的数值。通过查找索引节点能够快速的找到对应的文件。（使用ls -li filename查看索引节点的信息）
    在linux文件系统中，索引节点值是文件的标识，唯一的。两个不同的文件的索引节点值是不同的。索引节点值相同的文件它的内容是相同的，仅仅文件名不同。
    修改索引节点值相同的文件中的另一个文件，另一个文件的内容也跟着发生变化。索引节点对每个文件有一个引用计数，当创建硬链接的时候引用计数会增加1.
    目录不能创建硬链接，只有文件才能创建硬链接。
- Linux 下用设备文件来表示所支持的设备的，还有三个属性：类型，主设备号，次设备号。
    主设备号：主设备号表示系统存取这个设备的“内核驱动”。
    每一个设备文件都有一个次设备号，定义了这个设备在系统中的物理位置。设备存储选项。
    设备文件名：表示设备的名称。
- linux文件系统用超级块，节点索引，目录结构和文件表示。
    超级块是每个文件系统的根，用于描述和维护文件系统的状态。文件系统中的每个对象在linux中表示为一个索引节点。
    目录解雇dentry实现名称和innode之间的映射。有一个目录缓存用来保存最近使用的dentry。
    dentry还维护目录和文件之间的关系，支持目录和文件在文件系统中的移动。
- linux中用文件描述符来表示设备文件和普通文件。文件描述符是一个整型数据，所有对文件操作都通过文件描述符实现。
    文件描述符范围0～open_max。文件描述符的值仅在同一个进程中有效，即不同进程的文件描述符，同一个值很可能描述的不是同一个设备或者普通文件。(指向了/proc/self/fd 目录下的0,1,2)


### 程序进程线程

### Tcp网络编程基础

### 服务器和客户端信息的获取
### 数据的IO和复用

### 基于udp协议的接收和发送

### 高级套接字

### 套接字选项


### 原始套接字


### 服务器模型选择


### ipv6 简介

### Linux内核中网络部分结构与分布

### netfilter框架内报文处理

