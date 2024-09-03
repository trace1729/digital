# 数字集成电路实验讲义
# 写在前面
## 为什么写这本手册
这里我想先和大家分享一下，我为什么产生了设计这一个系列实验，以及希望编写这本手册的动机，或者说初心。事情还要从一个暑假开始讲起。。。
2024年的大三暑假，在经历了各个学校保研夏令营面试的“拷打”集成电路的专业知识后，我终于有时间可以参加“一生一芯”项目。高中时的我对DIY装机很痴迷，因此认为设计芯片就是体系结构设计，比如Intel和AMD的新架构等等。“一生一芯”项目也和计算机体系结构方向密切贴合。但是，由于我本人是学微电子专业（偏向集成电路设计方向），经过大学本科三年的专业课程学习，我对芯片的理解比高中时候更深刻，我深刻的认识到：**设计芯片绝不只是RTL代码**。我不否认RTL代码的作用，但是要想更深入的理解芯片或者说集成电路产业，还是要和电路、工艺、物理打交道。FPGA只是前期验证，最终一定要ASIC才是真正的芯片，而ASIC就需要数字集成电路、模拟集成电路、半导体物理、半导体工艺等这些课程的理论知识。
因此，我产生了一个想法：何不把数字集成电路的相关内容做一个开源的实验讲义？既是对自己大学本科几年学习的集成电路知识的总结和回顾，也算作是对一生一芯项目的补充知识。我感觉起码这是一件对于我个人来说有意义的事情！如果还可以有幸帮助到更多志同道合的同学，那鄙人不胜感激，也算对是我这几天熬夜的一个回报吧！
## 您将学到什么？
1. 本系列实验，您将通过使用免费的电路仿真工具LTspice仿真数字集成电路的许多典型电路和模块，例如与门、异或门、加法器、移位器等。在这个过程中，您将学习与门、加法器等数字电路中的基本模块，如何使用最基本的元件——晶体管（CMOS工艺）来实现。
2. 您将了解数字集成电路中如何对于性能、功耗以及面积进行综合考虑，进而设计出一个合适的数字集成电路模块。
3. 您将学习数字集成电路设计中常用的优化手段，例如精心设计晶体管尺寸。
## 预估用时
在掌握基本的数字集成电路理论和仿真工具使用方法的情况下，我们预估您完成全部实验的用时为：10小时。
## 参考教材
本系列实验的参考教材为《数字集成电路——电路、系统与设计（第二版）》。

## 实验环境
操作系统：Windows10及以上
仿真软件：LTspice 版本 24.0.12（2024-08-29更新）
## 项目文件内容
项目文件主要分为2部分：
1. 第一部分为讲义的MD文件，还有一些希望大家可以阅读的课外资料，目前只有2篇文章，一篇为摩尔提出摩尔定律的论文，另一篇为图灵提出图灵机概念的论文。
2. 第二部分为LTspice仿真文件，在LTspice_project文件夹中，其中包括各个章节的对应实验仿真文件以及我自己定义的库文件夹my_lib（其中包括一个反相器和传输门），直接使用LTspice打开运行即可。
## 实验目录
+ 实验1 CMOS反相器（非门）
+ 实验2 负载的概念
+ 实验3 （重要）MOSFET的宽长比
+ 实验4 *（CS专业选学）反相器链
+ 实验5 *（CS专业选学）功耗、能量和延时
+ 实验6 CMOS组合逻辑电路设计
+ 实验7 CMOS时序逻辑电路设计
+ 实验8 运算功能模块设计

## 学习建议

对于微电子以及电子信息专业同学，希望大家把每一章节的实验全部学习一遍，并且思考其中每一个电路的原理以及思考题。
对于计算机专业的同学，可以忽略实验4和实验5，以及实验6和实验7中带*的部分章节。

## 仿真局限性说明
由于本系列实验面向的对象是集成电路专业的同学，**因此在本系列实验中使用的仿真晶体管模型非常不准确！仅可以用于本次教学的原理性展示，实验仿真结果也仅供大家参考**。如果有条件的话，非常建议同学们将各个本系列实验使用厂家提供的PDK文件在Cadence、华大九天等商用级EDA中进行复现。

## 内容局限性说明
由于本人学识较浅，也和大家一样，正在学习的过程中，因此难免手册中会出现一些讲解不全面甚至错误的地方，还请大家海涵，也非常欢迎大家及时指出错误，我们一同交流。
本手册也借鉴了“一生一芯”项目中STFW，RTFM等学习方法，希望可以调动大家的学习主动性，对于一些资料非常丰富的内容，我们不再赘述，例如LTspice的安装和使用等等。
本系列实验仅是我从我个人的理解出发，选取了一些我个人比较“偏爱”的电路进行讲解，因此难免会“有失偏颇”，难以覆盖到教材中的每一个知识点和每一个电路结构，如有未涉及的部分，请大家自行学习，也非常欢迎大家补充！

<p align="right">赵振宇</p>
<p align="right">2024年8月31日于南京</p>
