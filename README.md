# This repo is for my brief notes when reading papers.

# 论文笔记和原文
1. Training with streaming annotation  
[原文](https://arxiv.org/abs/2002.04165)<br>
[笔记](https://github.com/KilluaKukuroo/paper-reading/blob/master/Training%20with%20streaming%20annotation.pdf)<br>
本文是Siemens Corporate Technology， UIUC， 剑桥， Information Sciences Institute的四位作者2020年2.13放在Arxiv上的文章。主要解决的问题是， 
在带标注的数据分批次到来，并且新来的数据比以前的数据标注质量好的情况下（streaming），如何更好的利用不同质量的数据进行模型训练。实验是
基于预训练的transformer在NLP里的event extraction task上面做的，但是思想可以很容易的扩展到其他通用领域。
 


## 优化方法
1. [Fast Exact Multiplication by the Hessian](http://www.bcl.hamilton.ie/~barak/papers/nc-hessian.pdf)<br>
本文是Siemens Corporate Research的一位作者在1993年发表在《*Neural Computation*》上面的文章。文章关于神经网络的二阶优化的研究，也是最近重新焕发青春的一个方向。
由于计算和存储Hessian矩阵（黑塞矩阵）巨大的开销，使得利用二阶梯度优化神经网络变得困难。本文提出一种巧妙的方法，可以方便的计算Hessian矩阵的很多性质，而不用计算
完整的Hessian矩阵。并且在backpropagation, recurrent backpropagation, Boltzmann Machines上做了实验验证本文方法的有效性。

2. [Practical Gauss-Newton Optimization for Deep Learning](http://proceedings.mlr.press/v70/botev17a/botev17a.pdf)<br>
本文是2017年的工作，引用量目前34。

## 多模态 multi-modal
1. [Multi-modal Approach for Affective Computing](https://arxiv.org/pdf/1804.09452.pdf)<br>
[code](https://github.com/zhanghang1989/ResNeSt)<br>
本文发表在 IEEE 40th International Engineering in Medicine and Biology Conference (EMBC) 2018， 作者来自 UC san diego。<br>


## Mobile && smart city
## scholars
- [Alex 'Sandy' Pentland - MIT media lab](https://scholar.google.com/citations?hl=zh-CN&user=P4nfoKYAAAAJ&view_op=list_works&sortby=pubdate)<br>
- [Yu Zheng - JD.COM](https://scholar.google.com/citations?hl=zh-CN&user=juUcdgYAAAAJ&view_op=list_works&sortby=pubdate)<br>

1.[Mobile Cyber-Physical Systems for Smart Cities](https://dl.acm.org/doi/abs/10.1145/3366424.3382121)<br>
2020年WWW workshop，research overview, 作者Desheng Zhang来自Rutgers CS. <br>
**problem**：城市化面临的问题：congestion，energy consumption需要CPS（IoT）来解决；现有的CPS方法大都是针对single infrastructure and single domain data, 限制了对mobility建模的能力。所以，
针对现在城市的发展可以获得的多种数据，本文介绍作者已经做的*cross-domain interaction*的研究，和潜在的研究方向。
**特点**: 文章非常简短；主要总结了作者自己在CPS领域的工作;
**future work**：1)Measuring and predicting mobility by mobility models; 2)Intervening and altering mobility by city services;

2.[Data Sets, Modeling and Decision Making in Smart Cities: A Survey](https://www.cs.virginia.edu/~stankovic/psfiles/Smart_City_Survey%20(002).pdf)<br>
2019 《ACM Transactions on Cyber-Physical Systems》,作者MEIYI MA, SARAH M. PREUM, and MOHSIN Y. AHMED, ABDELTAWAB HENDAWI and JOHN A. STANKOVIC(University of Virginia),WILLIAM TÄRNEBERG (Lund University, Sweden).<br>
**summary**: 综述了数据集和modeling，decision-making相关的文章，并且从这两个角度介绍了相应的研究方向和面临解决的问题；<br>

3.[Urban Computing: Concepts, Methodologies, and Applications](https://dl.acm.org/doi/pdf/10.1145/2629592)<br>
2014《ACM Transactions on Intelligent Systems and Technology》，citation=971,


## privacy
## scholars
- [Cynthia Dwork](https://scholar.google.com/citations?user=y2H5xmkAAAAJ&hl=zh-CN), distinguished scientist in **Microsoft Research**, citation>30,000;
- [Aaron Roth](https://scholar.google.com/citations?user=kLUQrrYAAAAJ&hl=zh-CN), Associate professor in **U Pennsylvania**, citation > 7,000;
- 

1.[Plausible Deniability for Privacy Preserving Data Synthesis](http://www.vldb.org/pvldb/vol10/p481-bindschaedler.pdf)<br>
2017 VLDB, 作者来自UIUC(Vincent Bindschaedler, Carl A.Gunter), Cornell Tech(Reza Shokri). 目前引用次数61. <br>
**problem**: 一方面很多场景都涉及到数据的分享，另一方面数据的隐私往往得不到很好的保护；
**SoA**:传统的两种保护数据隐私的方法：data de-identification需要对对手有背景知识的了解，exponential mechanism for differential privacy面对高维数据计算量太大；
**Opportunity**: 本文提出一种privacy-preserving 的方法来生成synthetic data;
**Challenges**:
**Contributions**:


2.[Data Synthesis based on Generative Adversarial Networks](http://www.vldb.org/pvldb/vol11/p1071-park.pdf)<br>
2018年VLDB, 作者来自UNCC, Georgy Mason Unviersity, ETRI(South Korea), 目前引用=24. 提出tableGAN生成假的table数据，在保证数据隐私性的同时满足数据分享质量的要求。<br>
**problem**: 
**SoA**:
**opportunity**:
**challenges**:
**contribution**:1)设计了table-GAN,生成数据质量高并且隐私性强的数据；2）生成的数据没有一对一的关系；3)多种实验验证了生成数据的隐私性和质量；<br>
**methods**：1)*table-GAN*改编自DCGAN，比传统的GAN多了一个模块，包括generator,discriminator,classifier(提高生成数据的semantic integrity，让生成的数据更加合理)；2)在原始的loss基础上，
添加information loss(保证生成数据在统计意义上和原始数据一致), classification loss(保证生成数据的semantic integrity);3）从data utility（包括statistical analysis,model compatibility(classification and regression)）, 
privacy两个角度验证生成的数据；

3.[Trajectory Recovery From Ash: User Privacy Is NOT Preserved in Aggregated Mobility Data](https://arxiv.org/pdf/1702.06270.pdf)<br>
2017 WWW.

4.[De-anonymization of Mobility Trajectories: Dissecting the Gaps between Theory and Practice](https://www.ndss-symposium.org/wp-content/uploads/2018/02/ndss2018_06B-3_Wang_paper.pdf)<br>
2018 NDSS. 


## 联邦学习

## deep learning && neural network
1.[ResNeSt: Split-Attention Networks](https://hangzhang.org/files/resnest.pdf)<br>
发表于2020年 arxiv，作者来自 Amason, UC Davis, 包括 Hang Zhang, Mu Li. 网上传言史上最强resnet魔改版。 <br>
**Problem**：目前大部分视觉的任务, e.g., obeject detection and semantic segmentation 还是使用ResNet的变体作为backbone，因为网络结构的简单和结构化。但是ResNet是为了image classification设计，
在CV的其他下游任务性能不是很好，可能因为limited receptive-field and lack of cross-channel interaction. 并且resnet的各种变体往往只能在特定的任务上取得较好性能。而且，最近的cross-channel information
在下游任务被证明很有效，而image classification的模型大都缺乏cross-channel interation，所以本文提出一种带有cross-channel representation的网络模型，目标是*打造一个versatile backbone with universally 
improved feature representation*, 从而同时提高多个任务的性能。 <br>
**SoA**：AlexNet -> NIN(1*1 convolution) -> VGG-Net(modular network design) --> Highway network(highway connection) --> ResNet(identity skip connection); NAS;
GoogleNet(muiti-path representation) --> ResNeXt(group convolution) --> SE-Net(channel-attention) --> SK-Net(feature map attention across two network branches);<br>
**contribution**：1）研究了带有feature map split attention 的resnet网络结构；
2) 在image classification 和其他transfer learning的应用场景种提供了一个大规模的benchmark, 刷新了SoA，在不同任务上分别提高1~3个点;<br>
**future work**: 通过神经网络结构搜索寻找不同硬件上对应得低延时low latency model; 不同的超参数(radix, cardinality, width)组合调优，可能会在不同的具体任务上取得更好的结果；
增加图片的size 可以提高acc；

2.[Backpropagation and the Brain](https://www.nature.com/articles/s41583-020-0277-3.pdf)<br>
发表在2020年《nature reviews|neuroscience》, 作者包括Geoffrey Hinton. <br>
大脑皮层如何修改突触，从而实现学习是一个很神秘的问题。几十年前，backpropagation 被认为是可以用来解释大脑学习机制的一个可能方法，但是由于反向传播机制没有带来很好的网络学习效果，
并且反向传播缺乏生物学上的可解释性，反向传播的意义被忽视。但是，随着近年算力的提升，NN在多个领域以反向传播为学习方法的基础上取得了很好的成绩，我们认为 backpropagation offers
a conceptualframework for understanding how the cortex learns. <br>
**contribution**：
**特点**：通过比较大脑神经元和人工神经网络，介绍了很多关于 learning algorithm的基础概念，e.g., backpropagation, supervised learning, error encoding, auto encoder.


3.[宽度学习-Broad Learning System: An Effective and Efficient Incremental Learning System Without the Need for Deep Architecture](https://ieeexplore.ieee.org/document/7987745)<br>
2017年发表在《IEEE Transactions on Neural Networks and Learning Systems》，作者来自澳门科技大学；

## NLP and web, knowledge graph
1.[Correcting Knowledge Base Assertions](https://arxiv.org/pdf/2001.06917.pdf)<br>
本文发表在2020WWW的oral，作者来自Oxford, Tencent, University of Oslo. <br>
**Problem**: knowledge bases(KB) 在搜索引擎，问答系统，common sense reasoning, machine learning等领域起到了重要的作用，but KB is suffering from quality issues, e.g.,
constraint violations and erroneous assertions.  <br>
SoA: 现有工作在KB quality上主要包含：error detection and assessment, quality improvement via completion, canonicalization.<br>
**Opportunity**: 现有的工作大都是检测出 KB中的错误之后就将错误去除，而不是去更正这些错误。所以更正检测出的erroneous assertions is a new opportunity; 关于correction，现有工作在忽视了assertion的上下文语义信息；
关于quality improvement，现有工作没有提出一个general correction method；<br>
**Challenges**: 
**Contributions**: 1-提出了可以用于更正错误的entity assertions and literal assertions的通用框架；2-利用了semantic embedding and observed features捕捉局部的上下文信息；3-soft property constraint;
4-在meidcal KB验证entity assertions correction, 在DPpedia验证literal assertions correction;  <br>


## CV
1.[A segregated cortical stream for retinal direction selectivity](https://www.nature.com/articles/s41467-020-14643-z.pdf) <br>
[Nature子刊研究颠覆常识：视网膜计算使眼睛先于大脑产生视觉信息](https://mp.weixin.qq.com/s/rzsS203NWKOhLqlenIGeDg)
2020年发表在"nature communication", 作者来自丹麦的Aarhus University. <br>
**problem**: 眼睛视网膜中包含能够可以感知运动的神经元细胞，但是这些神经元细胞如何感知的信息如何贡献给大脑皮层中的神经元细胞仍然
是一个没有被解决的问题；视网膜中有多个spatial-temporal channel感知运动方向、速度等信息，老鼠大脑皮层包含16个higher
 visual area (HVA)分别倾向于处理不同channel的信息比如颜色、方向。但是视网膜中每个通道的信息如何影响HVA，并且多个HVA
 多个通道的信息如何融合还是未解决的难题。<br>
**SoA**:
**Opportunity**:
**Challenges**:
**Contributions**: 描述了一种从眼睛到大脑皮层细胞特殊的神经回路，该回路传输运动视觉信息；可能潜在有助于治疗大脑感官失调
相关的疾病，比如痴呆、精神分裂；研究发现眼睛中一组细胞可以很好的感知运动信息；
Methods: 用小鼠作为实验动物，将小鼠的部分眼睛里面部分神经细胞感染，来研究小鼠眼睛的神经细胞如何对大脑皮层内部神经细胞感知
运动(visual movement)产生影响；<br>
**future work**: 研究在老鼠不同的运动场景下，视网膜中感应运动的细胞如何和何时发挥作用；
## 集成学习
### [review]
[Ensemble methods in Machine Learning](https://web.engr.oregonstate.edu/~tgd/publications/mcs-ensembles.pdf)<br>
本文是Oregon State University的Thomas G.Dietterich 2000年的工作，引用数已经 > 6000，是比较早的模型集成的综述工作。
本文综述了现有的集成方法，并且解释了为什么集成方法往往比单一的分类器效果好，同时用实验解释了为什么adaboost不容易过拟合。

[Ensemble Learning: A survey](https://onlinelibrary.wiley.com/doi/pdf/10.1002/widm.1249)<br>
本文是2018年的工作，引用量已经到100。


## 智慧电网 smart grid
1. [Application of Big Data and Machine Learning in Smart Grid, and Associated Security Concerns: A Review](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8625421)<br>
本文2018年发表在 IEEE Access上，作者来自 Oregon Tech 等多个高校，综述了大数据机器学习在智慧电网中的应用研究，主要介绍智慧电网的安全隐患。智慧电网(smart grid)是将传统电网和
信息通信技术相结合，实现通信和电能流动的双向性，从而增强电力系统的可靠性安全性和效率。In other words, SG is the
integration of technologies, systems and processes to make power grid intelligent and automated。<br>
本文特点：1.介绍了传统电网和智慧电网各自的特点，以及前者到后者的转换原因，遇到的问题和可能的解决办法；2.介绍了电网系统中的物联网组件和特点，介绍了智慧电网的数据采集，存储，分析，
等模块，大数据和机器学习在智慧电网中的应用，比如需求预测，攻击检测，通过采集的数据预测未来一段时间的风能、太阳能产能； 3.介绍了智慧电网中的网络攻击风险，以及可能的解决办法；

2. [Review on the Research and Practice of Deep Learning and Reinforcement Learning in Smart Grids](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8468674)<br>
本文2018年发表在CSEE，作者来自太原理工和中国电力科学研究院，是关于深度学习和强化学习在智慧电网中应用研究的综述。介绍了深度学习和强化学习在智慧电网中的以下几个方面的研究：
These application fields cover load/power consumption forecasting, microgrids, demand response, defect/fault detection, cyber security, stability analysis, and
nearly all the technical fields of smart grids.



