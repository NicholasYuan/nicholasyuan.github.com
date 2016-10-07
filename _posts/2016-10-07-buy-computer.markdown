---
layout: post
title:  "深度学习攒机小计"
date:   2016-10-07 14:30:11
author: nicholas
categories: DeepLearning
cover:  "/assets/buy-computer/all.jpg"
---

从搜集资料，到兼容性、价格比对，到机箱规格，最后到组装机器，安装配置环境，终于在9月份把自己的一台深度学习机器配置完成了。
最终配置：

- gpu : ASUS ROG [STRIX-GTX1080-8G-GAMING](http://www.asus.com.cn/Compare/Product.aspx?P_ID=1zMvS5oNHEGDTh6Q)
- CPU : Intel i7 [6850k](http://ark.intel.com/zh-cn/products/94188/Intel-Core-i7-6850K-Processor-15M-Cache-up-to-3_80-GHz)
- 主板 : ASUS X99 A II 
- 内存 : 金士顿 16G * 4 fury 2400mHz
- ssd : 三星950 pro
- 硬盘 : 东芝 3T DT01ACA300 (可以参考我在知乎下的一篇[硬盘选购](https://www.zhihu.com/question/27569776/answer/115022394?from=profile_answer_card))
- 电源 : 海韵1050W X-1050
- 机箱 : 迎广 IN WIN 303

## 收集资料

说一说自己的目标，就是围绕GTX1080显卡配置一台机器。

然后先说自己收集的资料，主要依照参考了两个博客：

- [深度学习主机攒机小记](http://mp.weixin.qq.com/s?__biz=MjM5ODkzMzMwMQ==&mid=2650408303&idx=1&sn=e4a61de98b82028bb49424e7acc4f805&scene=1&srcid=0729ivn68K1Eea5bDFPmCbyk&from=singlemessage&isappinstalled=0#wechat_redirecthttp://mp.weixin.qq.com/s?__biz=MjM5ODkzMzMwMQ==&mid=2650408303&idx=1&sn=e4a61de98b82028bb49424e7acc4f805&scene=1&srcid=0729ivn68K1Eea5bDFPmCbyk&from=singlemessage&isappinstalled=0#wechat_redirecthttp://mp.weixin.qq.com/s?__biz=MjM5ODkzMzMwMQ==&mid=2650408303&idx=1&sn=e4a61de98b82028bb49424e7acc4f805&scene=1&srcid=0729ivn68K1Eea5bDFPmCbyk&from=singlemessage&isappinstalled=0#wechat_redirecthttp://mp.weixin.qq.com/s?__biz=MjM5ODkzMzMwMQ==&mid=2650408303&idx=1&sn=e4a61de98b82028bb49424e7acc4f805&scene=1&srcid=0729ivn68K1Eea5bDFPmCbyk&from=singlemessage&isappinstalled=0#wechat_redirecthttp://mp.weixin.qq.com/s?__biz=MjM5ODkzMzMwMQ==&mid=2650408303&idx=1&sn=e4a61de98b82028bb49424e7acc4f805&scene=1&srcid=0729ivn68K1Eea5bDFPmCbyk&from=singlemessage&isappinstalled=0#wechat_redirecthttp://mp.weixin.qq.com/s?__biz=MjM5ODkzMzMwMQ==&mid=2650408303&idx=1&sn=e4a61de98b82028bb49424e7acc4f805&scene=1&srcid=0729ivn68K1Eea5bDFPmCbyk&from=singlemessage&isappinstalled=0#wechat_redirecthttp://mp.weixin.qq.com/s?__biz=MjM5ODkzMzMwMQ==&mid=2650408303&idx=1&sn=e4a61de98b82028bb49424e7acc4f805&scene=1&srcid=0729ivn68K1Eea5bDFPmCbyk&from=singlemessage&isappinstalled=0#wechat_redirect)
- [深度学习主机环境配置: Ubuntu16.04+GeForce GTX 1080+TensorFlow](http://www.52nlp.cn/深度学习主机环境配置-ubuntu16-04-geforce-gtx1080-tensorflow)

然后对GTX-1080做了一些调研，发现市面上总有[NVIDIA（公版）](http://www.geforce.cn/hardware/desktop-gpus)，和[ASUS](http://www.asus.com.cn/Compare/)、EVGA、微型、七彩虹等非公版，而且对于每种非公版，也都有至少两种选择，如华硕就有8g和o8g两款，但是市面上买不到o8g。对于GTX-1080的选择，目前大家都认为顶配显卡各个厂商做工都差不多，包括七彩虹的也都很好，因为GTX-1080自身的电气性能以及很好了，大家改动并不会很大。但是鉴于这是自己第一块GPU，还是选择了ASUS这个比较放心的厂家。

## 购买渠道

对于购买渠道我想多说两句，目前CPU在中国海关是重点商品（CPU被扣的时候详细摸了摸过关目录），加上15年11月份出了严查重点商品，CPU几乎是全部打开检测过关的，虽然不知道要检测什么，回来CPU四角有明显压痕，肯定是帮我测试CPU好不好用了，另外我这一个 cpu 6850k 对中国有专门的一款for china的，目前没有调查到有什么不同，海关说多数都有些小变动。但是呢，GPU并不是重点商品，所以过关一般都比较快乐~

国内的购买渠道不说了，另外大家不要忘了ASUS有一个官方商城，大家有想买的记得去看看，货有保障而且便宜。国外的我在亚马上海外购了CPU和GPU，加完税GPU便宜比国内要便宜近一千，CPU差不多。重点是GPU国内经常没货，有货的加价卖，赶上ASUS放货，就海外购了。

## CPU选购

- i7-6700k ￥2600
    - 4/8、8MB三级缓存、4.0-4.2GHz、PCIe3.0/16、DDR4-2133/DDR3L-1600、
- i7-6800k ￥3300
    - 6/12、15MB、3.4-3.6、PCIe3.0/28、DDR4-2400、140W
- i7-5820 ￥2900
    - 6/12、15MB、3.3-3.6、PCIe3.0/28、DDR4-2133、140W
- i7-5930 ￥4399
    - 6/12、15MB、3.5-3.7、PCIe3.0/40、DDR4-2133、140W
- i7-6850k ￥4700
    - 6/12、15、3.6-3.8、40、DDR4-2400、140W

这是当时调研的类似的[CPU规格](http://ark.intel.com/zh-cn/compare/94189,94188,94196)
最后选择6850K是考虑到自己可能会做两路GPU级联（GTX-1080需要16根总线通道，两路除了主板支持还要CPUPCIe通道大于32），28通道实在尴尬，就选择了6850k，后来证明和我一样这么想的人很多，6850k货很紧张，而6800k总是有货。

## 主板选择

CPU定下来其实主板的型号就比较好选择了，intel 官网给出的兼容主板就一款X99，好吧，接着看主板厂家。
主板的重要性大家应该都知道，总线、各个数据转换地很容易成为瓶颈，这里就选了两个比较大的厂家：[ASUS](http://www.asus.com.cn/Compare/)和[技嘉](http://www.gigabyte.cn/products/comparison/list.aspx?ck=2&pids=5284,5281,5812)，上面对比了自己家出的X99的不同款。

我最后还是选择了ASUS，华硕的X99系列总共有四类吧：A(A II)、X99 pro（带wifi）、A DELUXE（军工条件稳定性，家用没必要）和豪华顶配ROG系列。当然，推荐ASUS家的ROG系列，土豪专用，自己预算不够，把目光放在了 pro 上，很遗憾，没有货，就入了A II。

## 内存条 & 硬盘 

内存的意义在于做数据处理的时候，交换的速度，当然是频率越高越好，海盗船已经出了4000mHz的内存条，看了看，需要ROG主板超频才能支持，而且价格高的离谱，思考了一下自己需要做的实验，通常是一个实验做很久，内存缺失页并不会太高，这里并不是评价，于是中规中矩，买了金士顿fury系列2400mHz的，16g*4。

对于硬盘的选择，我的搭配是SSD+机械硬盘，也是现在的标配。机械硬盘请参考我在[知乎上的分析](https://www.zhihu.com/question/27569776/answer/115022394?from=profile_answer_card)。

对于SSD，确实需要认真说一下，这个坑目前还没有那么大。[知乎](https://www.zhihu.com/question/20369676)上的这个问题的回答很有参考价值，请认真看一下对于颗粒主控的简介。
而对于SSD的接口，现在有USB、SATA、M2、PCIe 和 NVMe，速度越来越快，价格越来越高。Macbook air 用的是非通用的M2接口，本来还以为可以给自己本更换一下，结果发现是非通用的。M2的SSD体积非常小，PCIe的价格太贵了，比较了几款品牌，最后放在了三星上，三星的950pro还是比850快很多的，于是就买了这一刻，另外951在国内不知道如何买到真货，某宝水太深价格便宜性能强劲，实在不放心。
![M2](/assets/buy-computer/m2.jpg)

## 电源 & 机箱

买的靠谱的老牌厂家海韵，因为以后可能会扩展双路，就买了1050W的电源，可以自己加一加CPU，GPU等的瓦数，多点没事。电源不能买差的，不然波动的电压会毁掉所有硬件。

最后我觉得最麻烦的是机箱，要考虑的情况比较繁琐，可以看看Tt，迎广这些品牌，我总结了几条：

- 机箱49cm是一个坎，上下分成支持水冷和不支持水冷，看自己后期需不需要水冷。
- 主要显卡GTX系列大多是26.7cm，显卡要能装下
- 高瓦数电源长度会变长，比如我买的海韵1050W长度是190mm，要考虑电源槽能容得下
- 底部有风扇的会比较好，但是保证和电源不冲突。
- 对于静音要谨慎考虑，散热是关键。

对于散热，我最后选择的方案是底部如风，后侧出风，CPU选择水冷。我书桌电脑主机位高度极限是49.5cm，非常尴尬，这样我就变成了选择：高度、散热风扇位置，电源卡槽够长，X99主板，CPU水冷。事实证明这些考虑仍然没有周全，就是硬盘盘位。
最后选择的迎广303唯一的确定就是硬盘盘位，在侧面，而且只能兼容两个SATA硬盘，虽然我只买了一个。而且，主板带的L型的SATA口硬盘线并不能插进去，又买的平口转换口，哎。

## 以上就是全部，开始组装

如果有时间视频压缩好了这里会插入视频。
![computer](/assets/buy-computer/computer.jpg)

# 开始装机

装机最开始就点亮，看主板OS的一些配置，看看GPU，内存条，SSD硬盘等有没有正常启动，大概长这样。
![x99](/assets/buy-computer/x99.jpg)
碰到了某东买的内存条其中一个不好使，但是过了七天了，打电话问售后怎么办，很有意思，售后说：在保修期的话，我们会根据情况维修，某些情况下也会更换。我问：那这个内存条保险多久？售后说：我看看，（过了一会），是终·身·保·修。我说那你们产品延保一年什么用？？

## 装操作系统

下面就是装操作系统。这里选择的还是Ubuntu16.04。

然后安装CUDA和cuDNN。这里是第二次按照CUDA，有一些坑，当时装CUDA7.0的时候，先装GPU的显卡，在装CUDA的时候就会黑屏，只能重装系统，现在不需要了，但是有一些顺序和版本需要注意一下。

这里我主要参考的是52nlp里的。我就不详细说了，有一些地方提醒一下。

- 先按照显卡驱动
- CUDA8.0 支持pasical架构
- 安装CUDA8.0的时候选择runfile按照方案 
- 在按照CUDA8.0的时候不要按照自带的显卡驱动方案。

其他就没什么了，查看显卡使用情况使用'nvidia-smi -l 5'可以5秒自动刷新。查看温度可以用'sensors'，查看所有的硬件使用情况可以用'hardinfo'。

祝大家装机顺利。














