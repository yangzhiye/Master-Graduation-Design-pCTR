# Master-Graduation-Design-pCTR
# 展示广告点击率预估研究

## (1). 想法与思考

## (2). 目前进展

### 1. 基本特征提取 (Done)
### 2. LR计算BaseLine (Done)
### 3. FM计算BaseLine (Done)
### 4. FM及其拓展论文阅读 (Doing)
### 5. embedding + dnn实现与调研 (Doing)

## (3). BaseLine与结果

## (4). 参考论文

### 数据集

#### 1. iPinYou Global RTB Bidding Algorithm Competition Dataset [论文地址](http://wnzhang.net/share/rtb-papers/ipinyou-dataset.pdf)

* 这篇文章在2014年直接抛出了Real-Time Bidding(RTB)展示广告数据集iPinYou。还描述了数据的产生和数据的介绍，这个数据集可以做CTR、CVR预估，竞价策略算法。本文主要在此数据集上做CTR预估研究。 

#### 2. Real-Time Bidding Benchmarking with iPinYou Dataset [论文地址](https://arxiv.org/pdf/1407.7073.pdf)

* 这篇文章相当于对iPinYou数据集做数据分布分析与计算BaseLine。不仅更为详尽的描述了数据的产生与数据的介绍，更大的贡献在于对数据集的整理，按照不同领域的广告分组，用图示对比出不同广告在不同特征下的CTR差异。而且统计了imps、clicks、convs。在训练集15,395,258条展示数据中只有11557条点击数据和935条转化数据，于是数据的稀疏性、正负比不均成为了CTR预估问题的难题。

### CTR预估方法调研

#### 1. Factorization Machines [论文地址](https://www.ismll.uni-hildesheim.de/pub/pdfs/Rendle2010FM.pdf)

* FM的优势在于解决稀疏特征组合问题。并且具有线性的计算复杂度，可以使用SGD、ALS、MCMC学习算法。

#### 2. Deep Interest Network for Click-Through Rate Prediction [论文地址](https://arxiv.org/pdf/1706.06978.pdf)

* 阿里巴巴展示广告组使用的Deep CTR model。也是embedding+dnn模型的改进，主要的想法是用户兴趣的多样性以及局部感知特性(用户的某次点击与部分历史点击有关)。

### 其他文献

## (5). 工具

#### 1. make-ipinyou-data [地址](https://github.com/wnzhang/make-ipinyou-data)

#### 2. FastFM [地址](https://github.com/ibayer/fastFM)