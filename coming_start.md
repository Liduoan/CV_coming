本次的项目是基于边缘计算的仪表读数识别系统的开发

首先  边缘计算  识别  系统

设计内容：

基于边缘计算框架  开发仪表读数识别系统

特色：！！！！ 亮点

基于树莓派实现轻量级边缘结点

针对 LED 数显式 指针式仪表  利用摄像头来获取仪表读数

自适应提取特征  

把数据发送到云平台数据中心



1、树莓派linux系统配置

1、计算机识别仪表读数，并发送给云数据中心





学习路线

相应的基础能力 数学 统计等

编程语言  Matlab  Python C++

以下来自https://blog.csdn.net/gdengden/article/details/80369458

----

专业工具

OpenCV编程入门

毛星云老师编著的OpenCV3编程入门

深度学习框架

莫凡教程系列之PyTorch :https://morvanzhou.github.io/tutorials/machine-learning/torch/

TensorFlow中文社区：

http://www.tensorfly.cn/

[深度学习 21天实战Caffe](http://mp.weixin.qq.com/s?__biz=MzU4NzE2MTgyNQ==&mid=2247484795&idx=2&sn=a140796f4cf025ddff006ee4e1b6609f&chksm=fdf10cf5ca8685e351aef72e977c77e4caa80426f2eea60ac07ae7852e89eb48b353f561b130&scene=21#wechat_redirect)

![这里写图片描述](https://img-blog.csdn.net/20180313200540824?watermark/2/text/Ly9ibG9nLmNzZG4ubmV0L2VsZWN0ZWNoNg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)



入门书籍

以下是我站在一个小白的视角给出一个入门计算机视觉的相对轻松的姿势。

## 一、宏观认识

小白通常看到这么多的细分方向大脑一片茫然，到底是学习人脸识别、物体跟踪，又或者是计算摄影，三维重建呢？不知道该怎么下手。其实这些细分方向有很多共通的知识，我的建议是心急吃不了热豆腐，只有对计算机视觉这个领域有了一个初步的全面了解，你才能够结合实际问题找到自己感兴趣的研究方向，而兴趣能够支持一个自学的小白克服困难持续走下去。

### 1、入门书籍

既然说是入门，这里就不推荐类似《 Multiple View Geometry in Computer Vision》这种虽然经典但是小白看了容易放弃的书了。

像素级的图像处理知识是计算机视觉的底层基础知识。不管你以后从事计算机视觉的哪个细分领域，这些基础知识都是必须要了解的。即使一个急切入门的小白，这一关也必须走的踏实。看到网上有人说直接从某个项目开始，边做边学，这样学的快。对此我表示部分赞成，原因是他忽略了基础知识的重要性，脑子里没有基本的术语概念知识打底，很多问题他根本不知道如何恰当的表达，遇到问题也没有思路，不知道如何搜索，这会严重拖慢进度，也无法做较深入的研究，欲速则不达。

入门图像处理的基础知识也不是直接去啃死书，否则几个公式和术语可能就会把小白打翻在地。这里推荐两条途径，都是从实践出发并与理论结合：一个是OpenCV，一个是MATLAB。

OpenCV以C++为基础，需要具备一定的编程基础，可移植性强，运行速度比较快，比较适合实际的工程项目，在公司里用的较多；MATLAB只需要非常简单的编程基础就可以很快上手，实现方便，代码比较简洁，可参考的资料非常丰富，方便快速尝试某个算法效果，适合做学术研究。当然两者搭配起来用更好啦。下面分别介绍一下。

#### 用MATLAB学习图像处理

推荐使用冈萨雷斯的《数字图像处理（MATLAB版）》（英文原版2001年出版，中译版2005年）。不需要一上来就全部过一遍，只需要结合MATLAB学习一下基本原理、图像变换、形态学处理、图像分割，以上章节强烈建议按照书上手动敲一遍代码（和看一遍的效果完全不同），其他章节可快速扫描一遍即可。但这本书比较注重实践，对理论的解释不多，理论部分不明白的可以在配套的冈萨雷斯的《数字图像处理（第二版）》这本书里查找，这本书主要是作为工具书使用，以后遇到相关术语知道去哪里查就好。 
![这里写图片描述](https://img-blog.csdn.net/20180313200727523?watermark/2/text/Ly9ibG9nLmNzZG4ubmV0L2VsZWN0ZWNoNg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

#### 用OpenCV学习图像处理

OpenCV（Open Source Computer Vision Library）是一个开源跨平台计算机视觉程序库，主要有C++预研编写，包含了500多个用于图像/视频处理和计算机视觉的通用算法。

学习OpenCV参考《学习OpenCV》或者《OpenCV 2 计算机视觉编程手册》都可以。这两本都是偏实践的书，理论知识较少，按照书上的步骤敲代码，可以快速了解到OpenCV的强大，想要实现某个功能，只要学会查函数（在https://www.docs.opencv.org/查询对应版本），调函数就可以轻松搞定。由于每个例子都有非常直观的可视化图像输出，所以学起来比较轻松有趣。 
![这里写图片描述](https://img-blog.csdn.net/20180313200745142?watermark/2/text/Ly9ibG9nLmNzZG4ubmV0L2VsZWN0ZWNoNg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

### 2、进阶书籍

经过前面对图像处理的基本学习，小白已经了解了图像处理的基础知识，并且会使用OpenCV或MATLAB来实现某个简单的功能。但是这些知识太单薄了，并且比较陈旧，计算机视觉领域还有大量的新知识在等你。

同样给你两种选择，当然两个都选更佳。一本书是2010年出版的美国华盛顿大学Richard Szeliski写的《Computer Vision: Algorithms and Application》；一本是2012年出版的，加拿大多伦多大学Simon J.D. Prince写的《Computer Vision: Models, Learning, and Inference》。两本书侧重点不同，前者侧重视觉和几何知识，后者侧重机器学习模型。当然两本书也有互相交叉的部分。虽然都有中文版，但是如果有一定的英语阅读基础，推荐看英文原版（见文末获取方式）。老外写的书，图和示例还是挺丰富的，比较利于 理解。 
![这里写图片描述](https://img-blog.csdn.net/20180313200810513?watermark/2/text/Ly9ibG9nLmNzZG4ubmV0L2VsZWN0ZWNoNg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

#### 《Computer Vision: Algorithms and Application》

这本书图文并茂地介绍了计算机视觉这门学科的诸多大方向，有了前面《数字图像处理》的基础，这本书里有些内容你已经熟悉了，没有那么强的畏惧感。相对前面的图像处理基础本书增加了许多新的内容，比如特征检测匹配、运动恢复结构、稠密运动估计、图像拼接、计算摄影、立体匹配、三维重建等，这些都是目前比较火非常实用的方向。如果有时间可以全书浏览，如果时间不够，你可以根据兴趣，选择性的看一些感兴趣的方向。这本书的中文版翻译的不太好，可以结合英文原版看。

#### 《Computer Vision: Models, Learning, and Inference》

该书从基础的概率模型讲起，涵盖了计算机视觉领域常用的概率模型、回归分类模型、图模型、优化方法等，以及偏底层的图像处理、多视角几何知识，图文并茂，并辅以非常多的例子和应用，非常适合入门。在其主页： 
http://www.computervisionmodels.com/ 
上可以免费下载电子书。此外还有非常丰富的学习资源，包括给教师用的PPT、每章节对应的开源项目、代码、数据集链接等，非常有用。 
![这里写图片描述](https://img-blog.csdn.net/20180313200848880?watermark/2/text/Ly9ibG9nLmNzZG4ubmV0L2VsZWN0ZWNoNg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

### 2、视觉SLAM

SLAM（Simultaneous Localization and Mapping）（详见《SLAM初识》），中文译作同时定位与地图创建。视觉SLAM就是用摄像头作为主传感器，用拍摄的视频流作为输入来实现SLAM。视觉SLAM广泛应用于VR/AR、自动驾驶、智能机器人、无人机等前沿领域。

视觉SLAM最好的入门资料是高翔（清华博士，慕尼黑理工博后）的《视觉SLAM十四讲-从理论到实践》。该书每章节都涵盖了基础理论和代码示例，深入浅出，非常注重理论与实践结合，大大降低了小白的学习门槛。 
![这里写图片描述](https://img-blog.csdn.net/20180313200939780?watermark/2/text/Ly9ibG9nLmNzZG4ubmV0L2VsZWN0ZWNoNg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)







