# RAG练习：汽车问答数据

前言：

本项目的来自[动手学RAG bilibili](https://www.bilibili.com/video/BV1vt42157Si/?spm_id_from=333.788&vd_source=591d301054ab5bbff896a4cdf210a23f)，相关代码参考[动手学RAG - 竞赛学习 - Coggle竞赛论坛](http://discussion.coggle.club/t/topic/30)，我是RAG初学者，学习这个项目进行练手。

## 1 主要工作

![image-20241031205504636](C:/Users/wangshaner/AppData/Roaming/Typora/typora-user-images/image-20241031205504636.png)

实线是已经完成的，虚线是可以扩展的。

## 2 环境配置

| **环境** |    **配置**    |
| :------: | :------------: |
|  Python  |      3.9       |
|   cuda   |      11.8      |
| pytorch  |     2.3.1      |
|   GPU    |    RTX3050     |
|   LLM    | ChatGLM4-flash |

## 3 结果分析

|           **模型**           |  **匹配度**  |
| :--------------------------: | :----------: |
|            TFIDF             |   0.377076   |
|             BM25             |   0.390365   |
|           m3e-base           |   0.358804   |
|         BCEmbedding          |   0.358804   |
|    **BM25 + BCEmbedding**    | **0.172757** |
|  ChatGLM4-flash + m3e-base   |   0.684464   |
| ChatGLM4-flash + BCEmbedding |   0.681354   |

多路召回的代码出现了一点问题。