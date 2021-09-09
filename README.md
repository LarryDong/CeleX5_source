# CeleX5_resource

原CeleX的SDK的git因包含安装包等内容，过大难以保存修改。
（官方仓库：[https://github.com/CelePixel/CeleX5-MIPI](https://github.com/CelePixel/CeleX5-MIPI) ）

这里只保留了：
1. CeleX5的源代码
2. CeleX5的Demo源代码
3. Samples示例
4. 文档

更新(2021.02)：上传 CeleX5新一版的用户手册(v2.2)。官方的github没有给出来（还是v2.0版本），是自己从别的网页搜到的。

## 源码维护
由于芯仑并没有维护源码，我个人在这里对bug进行维护。如果您在使用时遇到bug，无论是否修复，都清联系我，我在这里尽可能对源码保持更新。

Bug1：`tOffPixelIncreasing`和`tInPixelIncreasing`在计算时溢出的问题。

问提原因：源码计算时间时，`uint32_t`造成溢出。改用`size_t`格式。  
您需要重新编译`Sources`文件，以生成更新的`libCeleX.so`库文件，并替换原有库。  


## 技术交流
如果在使用CeleX传感器遇到技术问题，欢迎在issue中提问，大家一起交流。


## 友情链接
这里提供一些我个人的一些总结，包括代码和CSDN博客。持续更新。

传统相机与事件相机融合的特征跟踪算法：[https://github.com/LarryDong/FusionTracking](https://github.com/LarryDong/FusionTracking)

翻转DVS事件极性的demo：[https://github.com/LarryDong/dvs_inverter](https://github.com/LarryDong/dvs_inverter)

不依赖ROS环境的纯C++读取事件的demo：[https://github.com/LarryDong/dvs_cpp_dataLoader](https://github.com/LarryDong/dvs_cpp_dataLoader)

---

# English Comment
This is a brief version of CeleX5 SDK.
(official) SDK for CeleX5 sensor: [https://github.com/LarryDong/CeleX5-MIPI](https://github.com/LarryDong/CeleX5-MIPI)

Here I only reserve: CeleX_MP Source code, demo, samples, and key documents.

Update(2021.02): User guide (v2.2) is uploaded. The newest version on official git so far is v2.0. This new version was found from google.

## Personal Support

CelePixel did not maintain this code any more. I would try to fix bugs if you meet. Please contact me no matter you have solved one or just need some help.  

Bug1：`tOffPixelIncreasing` and `tInPixelIncreasing` overflow.

`celex5dataprocessor.cpp` is modified. Please re-compile your source code to generate `libCeleX.so` and replace the old one.

## Technical Issue
If you meet some difficulties using this sensor, and cannot find any solutions from reference documents, you can make an issue here. We can try to solve it together.

## Advertising Links
Some codes/blogs about event-based camera & using CeleX_MP, from myself:

Standard and Event camera fusion for feature tracking: [FusionTracking](https://github.com/LarryDong/FusionTracking)

Demo: invert polaritis in events, using ROS: [https://github.com/LarryDong/dvs_inverter](https://github.com/LarryDong/dvs_inverter)

Demo: event stream processing by C++, without ROS: [https://github.com/LarryDong/dvs_cpp_dataLoader](https://github.com/LarryDong/dvs_cpp_dataLoader)

