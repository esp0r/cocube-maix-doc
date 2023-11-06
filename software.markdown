---
layout: page
title: 软件设计
---
![](assets\software.png)
这是Cocube-MAIX的软件结构。对于ESP32主控，我们基于Arduino语法编写了Driver Library，封装了各种硬件功能，用户可以在此之上编写自己的控制逻辑。之后，通过micro-ROS中间件，在ROS2中发布一个Motion节点。ROS2中的其他软件包可以通过与Motion节点通讯来控制机器人运动。对于视觉主控，我们编写了MJPEG图传服务器，将摄像头看到的画面与ROS2中的Camera节点实时同步。

Driver Library 的代码仓库正在整理中