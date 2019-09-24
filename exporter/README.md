# 第4章 使用Exporter

在第1章中为了采集主机的监控样本数据，我们在主机上安装了一个Node Exporter程序，该程序对外暴露了一个用于获取当前监控样本数据的HTTP访问地址。这样的一个程序称为Exporter，Exporter的实例称为一个Target。Prometheus通过轮询的方式定时从这些Target中获取监控数据样本，并且存储在数据库当中。 在这一章节当中我们将重点讨论这些用于获取特定目标监控样本数据的程序Exporter。

本章的主要内容：

* 常用Exporter的使用，例如如何监控数据库，消息中间件等
* 如何实现自定义的Exporter程序
* 如何对已有的应用程序扩展Prometheus监控支持