# Code-rain
使用linux C语言实现数字雨，类似于《黑客帝国》屏幕上显示流动的数字；

本项目所使用的linux系统版本为：Linux version 3.13.0-24-generic，32位；

编程时需要ncurses.h 头文件，打开usr/include，若没有则打开终端输入命令来安装ncurses：`sudo apt-get install libncurses5-dev libncursesw5-dev`；

使用gcc编译；

运行结果仅为个人学习展示，可能并不理想。

**编程思路：**

1.确定屏幕的长宽xy，坐标轴顶点在左上角；

2.将代码雨分解成一个一个队列，每个队列包含n个节点，队列起始位置在x轴上，每个队列起始位置不重叠，队列依次在y轴加1，形成“下雨”效果；

3.当队列到达y轴最大值后，丢弃队列头节点 ，然后在尾节点插入新节点 ，循环往复。

原理示意图：

[https://img-blog.csdnimg.cn/20190912162701315.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dhbmdxaW5nY2h1YW45Mg==,size_16,color_FFFFFF,t_70](https://img-blog.csdnimg.cn/20190912162701315.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dhbmdxaW5nY2h1YW45Mg==,size_16,color_FFFFFF,t_70)


**运行效果：**

[https://img-blog.csdnimg.cn/2019091216243850.gif](https://img-blog.csdnimg.cn/2019091216243850.gif)

**版本记录：**

2019.9.12 初次提交 V1.0
