# ChatGPT-Comparison-Detection Project 🔬

![](https://img.shields.io/badge/Languages-%20English%2C%20Chinese-brightgreen) 
![](https://img.shields.io/badge/ChatGPT-Corpus%2C%20Detector-blue)

Official repository of paper ["How Close is ChatGPT to Human Experts? Comparison Corpus, Evaluation, and Detection"](https://arxiv.org/abs/2301.07597). Please star, watch, and fork our repo for the active updates!

See also→([📢 Feedback Space for Detectors](https://github.com/Hello-SimpleAI/chatgpt-comparison-detection/discussions/2) please feel free to leave your feedback here! 请留下您宝贵的意见！)



<img width="600" alt="image" src="https://user-images.githubusercontent.com/37113676/212355768-5ef7a26a-7cc5-4c38-91dc-2ee249ec49d5.png">

---
### Human ChatGPT Comparison Corpus (HC3) / 人类-ChatGPT 问答对比语料集
Yes, we propose the first **Human vs. ChatGPT** comparison corpus, named **HC3**.

我们提出了第一个 **Human vs. ChatGPT** 对比语料, 叫做 **HC3**.

<img width="520" alt="image" src="https://user-images.githubusercontent.com/37113676/213218672-e92b7036-a602-48c8-b70d-50ee1673bac8.png">

The first version of the HC3 datasets are now available on 🤗 Huggingface Datasets:
- [HC3-Engllish](https://huggingface.co/datasets/Hello-SimpleAI/HC3)
- [HC3-Chinese](https://huggingface.co/datasets/Hello-SimpleAI/HC3-Chinese)


在中文社区，HC3 数据集也已在 ModelScope 上可用:
- [HC3-Engllish](https://www.modelscope.cn/datasets/simpleai/HC3)
- [HC3-Chinese](https://www.modelscope.cn/datasets/simpleai/HC3-Chinese)

### Dataset Copyright

If the source datasets used in this corpus has a specific license which is stricter than CC-BY-SA, our products follow the same.
If not, they follow CC-BY-SA license.

| English Split       | Source | Source License | Note |
|----------|-------------|--------|-------------|
| reddit_eli5 | [ELI5](https://github.com/facebookresearch/ELI5)   | BSD License    |     |
| open_qa  | [WikiQA](https://www.microsoft.com/en-us/download/details.aspx?id=52419)  | [PWC Custom](https://paperswithcode.com/datasets/license)   |      |
| wiki_csai   | Wikipedia | CC-BY-SA |   | [Wiki FAQ](https://en.wikipedia.org/wiki/Wikipedia:FAQ/Copyright) |
| medicine    | [Medical Dialog](https://github.com/UCSD-AI4H/Medical-Dialogue-System) | Unknown|  [Asking](https://github.com/UCSD-AI4H/Medical-Dialogue-System/issues/10)|
| finance     | [FiQA](https://paperswithcode.com/dataset/fiqa-1) | Unknown |    |

| Chinese Split       | Source | Source License  | Note |
|----------|-------------|-----------|-------------|
| open_qa  | [WebTextQA & BaikeQA](https://github.com/brightmart/nlp_chinese_corpus) | MIT license |  |  |
| baike     | Baidu Baike  | None   |    |   |
| nlpcc_dbqa  | [NLPCC-DBQA](https://github.com/msra-nlc/ChineseDBQA) | Unknown |   [Asking](https://github.com/UCSD-AI4H/Medical-Dialogue-System/issues/10) |
| medicine    | [Chinese Medical Dialogue](https://tianchi.aliyun.com/dataset/90163) |  CC-BY-NC 4.0 | 
| finance     | [FinanceZhidao](https://www.heywhale.com/mw/dataset/5e9588f8e7ec38002d0331b1/content) | CC-BY 4.0 |  |
| psychology  | [On Baidu AI Studio](https://aistudio.baidu.com/aistudio/datasetdetail/38489) | CC0  | |
|law          | [LegalQA](https://github.com/siatnlp/LegalQA) | Unknown | [Asking](https://github.com/siatnlp/LegalQA/issues/2) |


---

### ChatGPT detectors / 内容检测器
![image](https://user-images.githubusercontent.com/37113676/211677236-d7c028f5-b9a5-4d88-baee-8b86dc942ff7.png)
(Hosted on 🤗 Hugging Face Spaces)


We provide three kinds of detectors, all in Bilingual / 我们提供了三个版本的检测器，且都支持中英文:
- [QA version / 问答版](https://huggingface.co/spaces/Hello-SimpleAI/chatgpt-detector-qa): detect whether an **answer** is generated by ChatGPT for certain **question**, using PLM-based classifiers / 判断某个**问题的回答**是否由ChatGPT生成，使用基于PTM的分类器来开发;
- [Sinlge-text version / 独立文本版](https://huggingface.co/spaces/Hello-SimpleAI/chatgpt-detector-single): detect whether a piece of text is ChatGPT generated, using PLM-based classifiers / 判断**单条文本**是否由ChatGPT生成，使用基于PTM的分类器来开发;
- [Linguistic version / 语言学版](https://huggingface.co/spaces/Hello-SimpleAI/chatgpt-detector-ling): detect whether a piece of text is ChatGPT generated, using linguistic features / 判断**单条文本**是否由ChatGPT生成，使用基于语言学特征的模型来开发;


在 modelscope 中文社区平台，三个版本的检测器也都可用:
- [QA version / 问答版](https://www.modelscope.cn/studios/simpleai/chatgpt-detector-qa)
- [Sinlge-text version / 独立文本版](https://www.modelscope.cn/studios/simpleai/chatgpt-detector-single)
- [Linguistic version / 语言学版](https://www.modelscope.cn/studios/simpleai/chatgpt-detector-ling)


The model weights are all available at 🤗 Hugging Face Models:

| Model Checkpoints              | Comment      |
|-----------------------|------------|
|[chatgpt-detector-roberta](https://huggingface.co/Hello-SimpleAI/chatgpt-detector-roberta)|To detect a single piece of text|
|[chatgpt-qa-detector-roberta](https://huggingface.co/Hello-SimpleAI/chatgpt-qa-detector-roberta)|To detect a question-answer pair|
|[chatgpt-detector-roberta-chinese](https://huggingface.co/Hello-SimpleAI/chatgpt-detector-roberta-chinese)|检测单条文本，中文版|
|[chatgpt-qa-detector-roberta-chinese](https://huggingface.co/Hello-SimpleAI/chatgpt-qa-detector-roberta-chinese)|检测一对QA文本，中文版|

The English models are based on [roberta-base](https://huggingface.co/roberta-base).
The Chinese models are based on [hfl/chinese-roberta-wwm-ext](https://huggingface.co/hfl/chinese-roberta-wwm-ext).


---

### Important Dates / 重要节点:

| Events                | Dates      |
|-----------------------|------------|
| Project Launch / 项目启动        | 2022-12-09 ✅ |
| Comparison Data Collection / 对比数据收集        | 2022-12-11 to Now 🏎️|
| Release ChatGPT Detector (Demo) / 检测器 Demo 发布 | 2023-01-11 ✅|
| Models Release / 模型开源 | 2023-01-18 ✅|
| Comparison Corpus Release / 语料集开源 | 2023-01-18 ✅|
| Research Paper / 研究论文发布 | 2023-01-19 ✅|
|...|...|



---

### Citation

Checkout this paper [arxiv: 2301.07597](https://arxiv.org/abs/2301.07597)

```
@article{guo-etal-2023-hc3,
    title = "How Close is ChatGPT to Human Experts? Comparison Corpus, Evaluation, and Detection",
    author = "Guo, Biyang  and
      Zhang, Xin  and
      Wang, Ziyuan  and
      Jiang, Minqi  and
      Nie, Jinran  and
      Ding, Yuxuan  and
      Yue, Jianwei  and
      Wu, Yupeng",
    journal={arXiv preprint arxiv:2301.07597}
    year = "2023",
}
```



---
### Our Story... / 背景故事

On December 9, 2022, which is 10 days after the launch of [ChatGPT](https://openai.com/blog/chatgpt/), we started this project, for two purposes: 
1. To create some **open-source models** for efficiently detecting ChatGPT-generated content; 
2. To collect a valuable **human-ChatGPT comparison Q&A corpus**, to facilitate releated research.

2022 年 12 月 9 日，也就是 [ChatGPT](https://openai.com/blog/chatgpt/) 推出的第 10 天，我们开始了这个项目，为了两个目的：
1. 做出一些**开源**模型工具来高效检测 ChatGPT 生成的内容；
2. 收集一批有价值的**人类和 ChatGPT 对比**的中英双语问答语料，来助力相关学术研究。

Welcome to follow our project! We have released a preview of our ChatGPT detectors, and the **models, dataset will be open-sourced** in about a week. We look forward to receiving feedback from the community to help improve the models and make contributions to **open** academic research together:)<br>
欢迎关注我们项目，我们目前已经发布ChatGPT检测器预览版，并将于约**一周内发布开源模型、数据集**。期待得到广大群众的反馈，来帮助我们改进模型，为**开放**的学术研究一起做贡献！

### About Us / 关于我们

We are a group of insignificant researchers (in the shadow of ChatGPT) hoping to do some significant work for the community. The team for this projects consists of PhD students and engineers from 6 universities/companies.<br>
我们是一群（在 ChatGPT 的阴影下）渺小的研究人员，但希望为社区做一些有意义的事。这个项目的团队由来自6所大学/公司的博士生和工程师组成。

|   |   |   |   |
|:-:|:-:|:-:|:-:|
| [Biyang Guo](https://github.com/beyondguo) | [Minqi Jiang](https://github.com/Minqi824) | [Ziyuan Wang](https://github.com/SUFEHeisenberg) | [Xin Zhang](https://github.com/izhx) |
|<img src="https://avatars.githubusercontent.com/u/37113676?s=64&v=4" alt="" width="40"/>|<img src="https://avatars.githubusercontent.com/u/39890732?s=64&v=4" alt="" width="40"/>|<img src="https://avatars.githubusercontent.com/u/44188955?s=64&v=4" alt="" width="40"/>|<img src="https://avatars.githubusercontent.com/u/26690193?s=64&v=4" alt="" width="40"/>|
| [Jinran Nie](https://github.com/NJRBarry) | [Yuxuan Ding](https://github.com/yxding95) | [Jianwei Yue](https://github.com/TurquoiseA) | [Yupeng Wu](https://github.com/realRoc) |
|<img src="https://avatars.githubusercontent.com/u/27188419?s=64&v=4" alt="" width="40"/>|<img src="https://avatars.githubusercontent.com/u/16249556?s=70&v=4" alt="" width="40"/>|  <img src="https://avatars.githubusercontent.com/u/23006855?s=64&v=4" alt="" width="40"/> | <img src="https://avatars.githubusercontent.com/u/44936809?s=64&v=4" alt="" width="40"/>  |









