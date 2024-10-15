[**中文**](./README.md) | [**English**](./README_EN.md)



# A Corpus for Named Entity Recognition in Chinese Novels with Multi-genres



Our paper was published in PACLIC2023

## Overview 

To promote the research of literary NER, we build a multi-genre literary NER corpus containing
263,135 entities in 105,851 sentences from 260 online Chinese novels spanning 13 different genres. 

Based on the corpus, we investigate characteristics of entities from different genres. We conduct several baseline NER models and conduct cross-genre and cross-domain experiments. Experimental results show that genre difference significantly impact NER performance though not as much as domain difference like literary domain and news domain.

For more details about our work, please refer to our paper:[A Corpus for Named Entity Recognition in Chinese Novels with Multi-genres](https://aclanthology.org/2023.paclic-1.39/)。

## Update

- [x] [2024/10/14] Dataset is now open-source

## Dataset

#### Data Acquisition

From [Qidian Chinese website](https://www.qidian.com/), we collect novels of 13 different genres, including Xianxia(仙侠), Sport(体育), Military(军事), History(历史),Fantasy(奇幻), Suspense(悬疑), Wuxia(武侠),Game(游戏), Xuanhuan(玄幻), Reality(现实), Sci-Fi(科幻), Urban(都市), and Light Novel(轻小说).

For each genre, we crawl the top 20 works from the genre’s collection list (as of 2021) and annotate the first 10 chapters of each selected work. All annotated chapters are publicly accessible.

#### Annotation Guidelines(see the paper for details)

- Omit single-character entities.
- Nested entities are ignored, only the longest external entity is annotated.
- Entities are composed of a central noun without quantifiers, pronouns, adjective modifiers, etc.
- An entity must refer to a specific entity in the novel.



#### Data Statistics

1. Dataset statistics

| Entity type | #Entity | #Distinct | Avg.length |
| :---------: | ------: | --------: | ---------: |
|     PER     | 197,597 |    17,013 |       3.64 |
|     LOC     |  45,094 |     4,641 |       3.60 |
|     ORG     |  20,444 |     2,804 |       4.87 |
|     ALL     | 263,135 |    24,458 |       3.73 |

2. Statistics of entities in each genre (see the paper for details)

   


## Model

| Model              | Link                                                         | Description                                         |
| ------------------ | ------------------------------------------------------------ | --------------------------------------------------- |
| roberta-bilstm-crf | [Download](https://huggingface.co/zhao73/MultiGenre-ChineseNovel) | NER model based on MultiGenre-ChineseNovel training |



## Experimental Results

1. Cross-genre experimental results, the confusion matrix of Micro-F1 on the left and ORG-F1 on the right

<div align="left">
  <img src="assets/Micro-F1.png" alt="F1" width="45%">
  <img src="assets/org-F1.png" alt="ORG" width="45%">
</div>



## Statement

The data we obtained are all publicly available on Qidian Chinese website and are only used for scientific research purposes.

## Acknowledgements

This project was initiated by Zhengzhou University's [Natural Language Processing Laboratory](http://www5.zzu.edu.cn/nlp/index.htm). The responsible students by [Hanjie Zhao](https://github.com/hjzhao73) with guidance from teachers  Yuxiang Jia,  Hongying Zanhttps://github.com/hfxunlp). We thank all the teachers in the laboratory for their strong support, as well as for providing valuable data and computing resources.

## Citation

If you would like to cite this work, please use the following format:

```text
@inproceedings{zhao-etal-2023-corpus,
    title = "A Corpus for Named Entity Recognition in {C}hinese Novels with Multi-genres",
    author = "Zhao, Hanjie  and
      Xie, Jinge  and
      Yan, Yuchen  and
      Jia, Yuxiang  and
      Ye, Yawen  and
      Zan, Hongying",
    editor = "Huang, Chu-Ren  and
      Harada, Yasunari  and
      Kim, Jong-Bok  and
      Chen, Si  and
      Hsu, Yu-Yin  and
      Chersoni, Emmanuele  and
      A, Pranav  and
      Zeng, Winnie Huiheng  and
      Peng, Bo  and
      Li, Yuxi  and
      Li, Junlin",
    booktitle = "Proceedings of the 37th Pacific Asia Conference on Language, Information and Computation",
    month = dec,
    year = "2023",
    address = "Hong Kong, China",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2023.paclic-1.39",
    pages = "398--405",
}
```
