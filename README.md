# nginx-learn
<!-- TOC depthFrom:2 depthTo:3 -->

- [一、Nginx 简介](#一nginx-简介)
- [二、Nginx 入门](#二nginx-入门)
- [三、Nginx 实战](#三nginx-实战)
  - [Http 反向代理](#http-反向代理)
  - [Https 反向代理](#https-反向代理)
  - [负载均衡](#负载均衡)
  - [网站有多个 webapp 的配置](#网站有多个-webapp-的配置)
  - [静态站点](#静态站点)
  - [搭建文件服务器](#搭建文件服务器)
  - [解决跨域](#解决跨域)
- [资源](#资源)

<!-- /TOC -->

## 一、Nginx 简介
**什么是 Nginx?**
**Nginx (engine x)** 是一款轻量级的 Web 服务器 、反向代理服务器及电子邮件（IMAP/POP3）代理服务器。

**什么是反向代理？**
反向代理（Reverse Proxy）方式是指以代理服务器来接受 internet 上的连接请求，然后将请求转发给内部网络上的服务器，并将从服务器上得到的结果返回给 internet 上请求连接的客户端，此时代理服务器对外就表现为一个反向代理服务器。

## 二、Nginx 入门
nginx 的使用比较简单，就是几条命令。
常用到的命令如下：
~~~shell
nginx -s stop       快速关闭Nginx，可能不保存相关信息，并迅速终止web服务。
nginx -s quit       平稳关闭Nginx，保存相关信息，有安排的结束web服务。
nginx -s reload     因改变了Nginx相关配置，需要重新加载配置而重载。
nginx -s reopen     重新打开日志文件。
nginx -c filename   为 Nginx 指定一个配置文件，来代替缺省的。
nginx -t            不运行，仅仅测试配置文件。nginx 将检查配置文件的语法的正确性，并尝试打开配置文件中所引用到的文件。
nginx -v            显示 nginx 的版本。
nginx -V            显示 nginx 的版本，编译器版本和配置参数。
