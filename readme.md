# `工具箱的`深度學習記事簿

本仓库的功能：`入门深度学习`、`参考常用代码`、`了解深度神经网络经典论文`。

请注意，本仓库后半部分主要讨论计算机视觉领域的基于深度学习的方法。

<details>
<summary><strong>点击此处展开一堆P话</strong></summary>
“理解机器学习和深度学习的最佳方法是学以致用。”

Akasaki很菜，所以慢慢地学着，并在记事簿上写下笔记。Akasaki希望这个记事簿对自己很多有用，希望它对你也一样有用。这里包含了我从入门到依然在入门的过程中接触到的大部分知识。对于目录中的每一条，基本会有以下内容：

<p><strong>  1. 这个知识有什么用</strong></p>
<p><strong>  2. 这个知识如何使用或如何实现</strong></p>

请注意，本仓库中的大部分内容都在互联网上或各种书籍上能找得到。我所做的只是夹带私货地把它们串联在一起。

</details>

本仓库的很多代码主要使用[Tensorflow](https://www.tensorflow.org/)等实现。也许等我写完后[我的朋友们](https://github.com/PaperFormulaIV)会帮我翻译出一份pytorch版本。

**这个仓库的部分文稿包含了LaTex公式**。我在每一个包含公式的文档头加入了mathjax相关的引用。如果你希望正常阅读，**请挂梯子访问[本仓库的网页版](https://ml.akasaki.space)**。如果你的网络条件导致了公式加载失败，请克隆本仓库到本地，并使用typora等markdown编辑器阅读。

##  目录

目录的使用方法：**点击就可以跳转到相关页面**。其中前面打了对勾的是已经可供阅读的部分，未打勾的是还没有写或正在写的部分。本仓库在宣布`archive`之前会保持更新。

>  如果你在阅读的过程中遇到了不明白的名词，**为了防止出现递归式学习，可以参照[附录-常见词汇](./appendix/similar-vocabularies.md)了解相关词汇的释义。**

### 第零章：在开始之前

诶**等等**！你确定你真的想碰这个方向吗？

- [x] [01. 毁灭网友的人工智能](./ch0/ai-that-destroying-netizens.md)
- [x] [02. 选框架比陪女朋友逛超市还难](./ch0/nn-and-frameworks.md)
- [x] [03. 剁手买一块显卡的理由（可不阅读）](./ch0/configure-gpu.md)
- [x] [04. 体验痛苦：安装轮子和管理环境](./ch0/create-new-environment-using-conda.md)

---

### 第一章上：HelloWorld！

我猜你见过一些诸如深度学习的计算机视觉、深度学习的自然语言处理等名词，但是你肯定没看到过深度学习自己单独出现。没错，**深度学习是一种方法，往往用来解决各种问题。所以我们首先要了解方法的基本思想，才能看如何用它解决问题**。所以这一章我们主要了解最基本的机器学习任务线性回归以及其他的一些基础知识。看**完本章也许初学者会不知所以然**。但是请继续看下去，你就会发现这些东西的实际用处。

- [x] [01. 试着读取、操作和显示数据](./ch1p1/operate-on-data.md)
- [x] [02. 自动求梯度](./ch1p1/automatic-gradient.md)
- [x] [03. 机器学习的HelloWorld：线性回归](./ch1p1/linear-regression.md)，以及[线性回归的代码实现](./ch1/linear-regression-code.md)
- [x] [04. softmax 回归](./ch1p1/softmax-regression.md)，以及[代码实现](./ch1/softmax-regression-code.md)

---

### 第一章下：深度学习基础

- [x] [05. 多层感知机](./ch1p2/multilayer-perceptron.md)，以及[代码实现]()
- [ ] [06. 模型的选择，欠拟合和过拟合]()
- [ ] [07. 权重衰减]()
- [ ] [08. 丢弃法]()
- [ ] [09. 正向传播和反向传播]()

---

### 第二章上：卷积神经网络及其要素

卷积神经网络，听上去似乎是一个很厉害的东西。在这里先抛出一个结论：**相较于全连接网络，卷积神经网络相对的进步在于卷积层结构和池化结构的引入**。也就是说，在全连接网络的基本思想上，塞进卷积和池化，就变成了一个“更厉害”的东西。所以在这半章，我们主要了解这两样东西。

- [x] [01. 卷积神经网络和卷积操作](./ch2p1/convolutional-nn-and-ops.md)
- [ ] [02. 二维卷积层的基本]()
- [ ] [03. 填充、填充和感受野]()
- [ ] [04. 多输入通道和多输出通道的进一步理解]()
- [ ] [05. 池化的写法]()
- [ ] [06. 批量归一化的用处]()

---

### 第二章下：经典卷积神经网络

上半章对卷积神经网络的一些基础知识做了简单介绍，下半章主要以历史的眼光观察经典的卷积神经网络。从LeNet手写数字识别成为第一个卷积神经网络的应用开始，到后来卷积神经网络往越来越深，成为深度卷积神经网络，再到后来出现并行、残差等概念，它们逐渐变得越来越成熟。这半章我们会了解这些网络的大体思路和代码写法。当然，如果你有兴趣可以阅读论文本身。

- [x] [01. 第一个卷积神经网络：LeNet](./ch2p2/LeNet.md)、相应[论文](./ch2p2/lecun-01a.pdf)以及[代码](./ch2p2/LeNet-code.md)
- [ ] [02. 小插曲：Keras高级API]()
- [ ] [03. 更深的卷积的神经网络：AlexNet]()、相应[论文](./ch2p2/NIPS-2012-imagenet-classification-with-deep-convolutional-neural-networks-Paper.pdf)以及[代码]()
- [ ] [04. 可复用的的网络单元：VGG]()、相应[论文](./ch2p2/1409.1556VGG.pdf)以及[代码]()
- [ ] [05. 带有残差的网络：ResNet]()、相应[论文](./ch2p2/1512.03385ResNet.pdf)以及[代码]()
- [ ] [06. 网络中的网络：NiN]()
- [ ] [07. 致敬LeNet：含有并行连接的网络GoogLeNet]()
- [ ] [08. 稠密链接网络：DenseNet]()

---

### 第三章：谈一些计算机视觉的方向

深度学习是一种方法，它可以用来解决各类问题。但是很明显地球上所有的问题多到不能被枚举（怎么突然上升到了哲学高度），而上一章我们恰好聊了卷积神经网络，并且卷积神经网络近年来在计算机视觉领域有着很突出的表现。所以我们在这里**以计算机视觉为例讨论一些深度学习的应用**。

- [x] [01. 深度学习之于计算机视觉](./ch3/deep-learning-for-computer-vision.md)
- [x] [02. 图像增广和微调](./ch3/image-augmentation.md)
- [ ] [03. 目标检测中的边界框和锚框]()
- [ ] [04. 多尺度目标检测]()
- [ ] [05. 目标检测数据集（皮卡丘）]()
- [ ] [06. 单发多框检测(SSD)]()
- [ ] [07. 区域卷积神经网络(R-CNN)系列]()
- [ ] [08. 语义分割和数据集]()
- [ ] [09. 全卷积网络(FCN)]()
- [ ] [10. 样式迁移]()
- [ ] [11. 实战 Sifar-10]()，以及[实战 ImageNet-Dogs]()

---

### 第四章：循环神经网络

- [ ] [01. 呃，语言模型是啥]()
- [ ] [02. 循环神经网络！]()，以及[代码实现]()
- [ ] [03. 一个语言模型的数据集（歌词）]()
- [ ] [04. 通过时间反向传播]()
- [ ] [05. 门控制循环单元(GRU)]()
- [ ] [06. 长短期记忆(LSTM)]()
- [ ] [07. 深度循环神经网络]()
- [ ] [08. 双向循环神经网络]()

---

### 附录

- [x] [01. 常见的词汇](./appendix/similar-vocabularies.md)
- [ ] [02. 快速配置环境以及安装包](./appendix/quick-envs-and-packages.md)
- [x] [03. 工地matplotlib](./appendix/introducing-matplotlib.md)
- [x] [04. 激活函数们](./appendix/activation-functions.md)
- [x] [05. 总是用到的代码块](./appendix/similar-codeblocks.md)
- [ ] [06. 常见的包]()
- [x] [07. 工具箱？](./appendix/who-is-akasaki-toolbox.md)

---

### 第-1章：数字信号处理（DSP）

- [x] [01. 何为DSP，为何DSP](./ch-1/about-dsp.md)
- [x] [02. 周期信号](./ch-1/periodic-signal.md)
- [ ] [03. 谐波]()
- [ ] [04. 非周期信号]()
- [ ] [05. 噪声]()
- [ ] [06. 自相关]()
- [ ] [07. 离散余弦变换]()
- [ ] [08. 离散傅里叶变换]()
- [ ] [09. 滤波与卷积]()
- [ ] [10. 微分与积分]()
- [ ] [11. LTI系统]()
- [ ] [11. 调制和采样]()

---

### 第-2章：TensorFlow编程策略

能翻到这里，说明你也应该在愁这些东西了。

- [x] [01. TF张量操作API第一部分](./ch-2/operation-on-tensors-1.md)
- [x] [02. TF张量操作API第二部分](./ch-2/operation-on-tensors-2.md)
- [x] [03. 对张量进行基本数学运算](./ch-2/operator-for-tensors.md)
- [x] [04. TensorFLow编程策略](./ch-2/tensorflow-strategy.md)
- [ ] [05. 让数据变得能够训练]()


---

## 继续学习

当你看完本仓库所有内容时，恭喜你，你已经**快要入门了**。你在这里简要了解了深度神经网络对计算机视觉以及其他一些机器学习任务的深刻影响，接下来你应该选一个你想继续深刻研究的方向。在你开始研究的初期，你可以找到一个听上去很感兴趣的方向，然后试着读以下该方向的综述，确定你是否真的喜欢它。一般情况下我会这样了解一个方向：

- [ ] 这里应该马上会有一篇短文

我还会继续开放用于下一步学习的仓库（在写了在写了），以便后续参考。

---

## 捐助

如果这个仓库有用的话请在[github](https://github.com/visualDust/talkischeap)为[本仓库](https://github.com/visualDust/talkischeap)施舍一个star，这便是最好的捐助，是我继续写笔记的动力。

![_](https://jwenjian-visitor-badge-5.glitch.me/badge?page_id=VisualDust.anything)
![_](https://img.shields.io/github/stars/VisualDust/talkischeap.svg?style=flat)
![_](https://img.shields.io/github/license/visualdust/talkischeap.svg?style=flat&label=license&message=notspecified)