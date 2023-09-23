# Language oriented Neural Decoding
The purpose of this repository is to collect and investigate language oriented neural decoding work.

## 1.Survey
  This section will be supplemented in the future.<br>

## 2.Researches
#### 2.1 EEG数据工作汇总
  [1. Open Vocabulary Electroencephalography-to-Text Decoding and Zero-Shot
Sentiment Classifcation](https://ojs.aaai.org/index.php/AAAI/article/view/20472)<br>
  该工作发表在AAAI-22上，提出了`EEG2Text`任务，并在`ZuCO`数据集上使用BART模型，完成EEG信号生成开放域内的文本重建任务，并在此基础上进一步进行零样本情感分类。 
#### 2.2 MEG数据工作汇总

#### 2.3 fMRI工作汇总
  [1. UniCoRN: Unified Cognitive Signal ReconstructioN bridging cognitive
signals and human language](https://arxiv.org/abs/2307.05355)<br>
该工作发表于2023ACL上，提出了`fMRI2Text`任务和通过脑信号生成文本的UniCoRN框架，并使用该框架在`Narratives`和`ZuCO`数据集上完成了`fMRI2Text`和`EEG2Text`任务，该工作还使用了多种划分数据集的方法进行测试。<br>
  [2. Semantic reconstruction of continuous language from non-invasive brain recordings](https://www.nature.com/articles/s41593-023-01304-9)  `2023-05-01`<br>
  该工作发布于Nature Neuroscience，为每个受试者建立编码器，编码器为`fMRI`体素级建模，提取刺激词的语义特征，通过正则化线性回归预测体素中`BOLD`信号。并为每个受试者估计一个词率模型，预测单词何时被感知。`GPT-1`语言模型用于生成候选词序列，维护一个`beam`，包含k个候选词，当词率模型检测到新词时，为每个候选生成续词，编码模型为每个续词打分，保留分数最高的k个。迭代生成最可能的词序列。<br>
  训练数据来自受试者听16小时的叙述故事的`fMRI`影响。

#### 2.4 多模态和其他信号工作

## 3.Datasets
[1. A natural language fMRI dataset for 
voxelwise encoding models ](https://www.nature.com/articles/s41597-023-02437-z)<br>
[2. The “Narratives” fMRI dataset for 
evaluating models of naturalistic 
language comprehension](https://www.nature.com/articles/s41597-021-01033-3)<br>
该数据集在345名受试者上收集了891份fMRI扫描，刺激呈现方式为语音播放。刺激包含27个故事，每个故事3-56分钟，共4.6小时。刺激材料来源于广播录音、公共演讲、电影动画等。刺激分布如下图所示。<br>
![image](https://github.com/xiaRunZe/Neural-Decoding/blob/main/figures/%E5%9B%BE%E7%89%87.png)


[3. A synchronized multimodal 
neuroimaging dataset for studying 
brain language processing](https://www.nature.com/articles/s41597-022-01708-5)<br>
该数据集收集了12名来自北京的大学生fMRI和MEG扫描记录，在听60个来自人民日报的故事（包含不同话题）时进行扫描，每个故事包含608-1076个词，4-7分钟。其中fMRI经7次扫描，每次1.5小时，第一次扫描结构MRI和静息状态MRI，后六次进行任务扫描fMRI。MEG数据也经6次任务扫描，与fMRI后6次扫描相对应。（但fMRI和MEG扫描中间间隔一个月以上，避免材料被熟记）每次扫描结束时，受试者需回答与故事相关的选择题。<br>
刺激来源（人民日报评论）：https://www.ximalaya.com/album/30917322<br>

[4. ZuCo, a
simultaneous EEG and eye-tracking
resource for natural sentence
reading](https://www.nature.com/articles/sdata2018291)<br>
[5. Open multimodal iEEG-fMRI 
dataset from naturalistic 
stimulation with a short 
audiovisual film](https://www.nature.com/articles/s41597-022-01173-0)<br>
