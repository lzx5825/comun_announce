# comun_announce_client

#### 项目名称
小区信息发布系统_客户端

#### 项目描述
本次项目是基于Linux环境的交叉编译arm-linux-gcc，在GEC6818开发板上运行，主要通过SOCKET编程，应用TCP通信链接服务器端，实现与服务器和其他客户端的通信，实现聊天功能，同时应用HTTP请求连接API接口，获取网络信息，如：天气和新闻等数据，通过font字库显示在开发板上。


#### 项目需求

1.  客服端上线后链接到服务器
2.  客户端可通过http请求获取网络信息
3.  客户端可与其他用户进行通信
4.  客户端可接收到服务器的公告消息
5.  客户端可通过服务器发送文件给其他用户

#### 环境搭建

##### 开发平台
Linux
##### 开发工具
交叉编译arm-linux-gcc,Notepad++

##### 其他工具

jpeglib库,font库

##### 编程实现

使用编辑器notepad++编写代码，编写Makefile管理工程目录，利用arm-linux-gcc交叉编译，再通过Linux平台的SSH服务器将编译生成的程序文件传输到开发板中，最后执行。 

#### 涉及知识

##### 基本知识

1.  C语言
2.  文件IO
3.  系统编程
4.  触摸屏处理
5.  jpeglib库使用
6.  font库使用

##### 核心知识

1. TCP 通信

2. HTTP 请求

3. cJSON 数据解析： 运用cJSON数据解析从云API接口中获取所需要的字符串数据。

   

#### 具体描述

客户端上线，链接服务器成功后，可收到服务器通过tcp发送的公告信息，同时可通过点击gec6818开发板获取天气数据和新闻消息，通过cJSON解析数据，然后使用font字库显示在开发板中，触摸开发板可查看广州多日天气预报，另外可选择其他客户端输入格式进行的消息收发和指定文件收发。例如：客户端发送消息格式(To <对方客户端tcp_socket>:<消息内容>)，发送文件格式(send file to sockfd:<对方客户端tcp_socket>)。

#### 项目总结

此次项目主要运用了网络编程中TCP/IP协议、HTTP协议、API接口、触摸屏的坐标处理、进/线程的创建与终止，文件IO。项目关键点在于cJSON数据处理（提取需要的字符串）,font字库使用和tcp协议通信。