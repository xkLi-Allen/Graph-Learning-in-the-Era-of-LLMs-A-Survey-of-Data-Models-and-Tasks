---
title: 'Graph Learning in the Era of LLMs: A Survey of Data, Models, and Tasks'

---

#    Graph Learning in the Era of LLMs: A Survey of Data, Models, and Tasks
![Last Commit](https://img.shields.io/github/last-commit/xkLi-Allen/Graph-Learning-in-the-Era-of-LLMs-A-Survey-of-Data-Models-and-Tasks?label=Last%20Commit&color=green)
![Visits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https://github.com/xkLi-Allen/Graph-Learning-in-the-Era-of-LLMs-A-Survey-of-Data-Models-and-Tasks&title=Visits&edge_flat=true)
![License](https://img.shields.io/github/license/xkLi-Allen/Graph-Learning-in-the-Era-of-LLMs-A-Survey-of-Data-Models-and-Tasks?label=License)
![Stars](https://img.shields.io/github/stars/xkLi-Allen/Graph-Learning-in-the-Era-of-LLMs-A-Survey-of-Data-Models-and-Tasks?style=social)
![Forks](https://img.shields.io/github/forks/xkLi-Allen/Graph-Learning-in-the-Era-of-LLMs-A-Survey-of-Data-Models-and-Tasks?style=social)

With the proliferation of cross-task and cross-domain textual attribute graphs, the integration of Graph Neural Networks (GNNs) and Large Language Models (LLMs) has become a pivotal approach to addressing complex graph data problems. Using a novel classification framework based on the three core elements of machine learning—data, model, and downstream task—we systematically categorize and summarize current tasks. Through this approach, we provide a structured review of existing GRAPH-LLM advancements across diverse domains and tasks, analyzing data types, model architectures, and their performance in various applications.

![Graph Learning in the Era of LLMs A Survey of Data, Models, and Tasks](https://hackmd.io/_uploads/HkGNTdbX1g.png)


####    Notice
Throughout this manuscript, references to "ICLR'25" denote works submitted to ICLR 2025 but not yet accepted for publication. These submissions are currently under review, and their inclusion here should not be interpreted as confirmation of acceptance. This notation is intended solely to indicate the targeted venue for potential publication and does not imply any final publication status.
## Table of Contents

1. [Graph Learning in the Era of LLMs: A Survey of Data, Models, and Tasks](#graph-learning-in-the-era-of-llms-a-survey-of-data-models-and-tasks)
2. [Table of Contents](#table-of-contents)
3. [Data](#data)
   - [Single Task & Single Domain](#single-task--single-domain)
   - [Single Task & Multi Domain](#single-task--multi-domain)
   - [Multi Task & Single Domain](#multi-task--single-domain)
   - [Multi Task & Multi Domain](#multi-task--multi-domain)
   - [Graph Reasoning](#graph-reasoning)
4. [Model](#model)
   - [GNN and LLM as Independent Collaborative Modules](#gnn-and-llm-as-independent-collaborative-modules)
   - [GNN-enhanced LLM (Learnable)](#gnn-enhanced-llm-learnable)
   - [LLM-enhanced GNN (Learnable)](#llm-enhanced-gnn-learnable)
   - [GNN-only](#gnn-only)
   - [LLM-only](#llm-only)
5. [Task](#task)
   - [Single Domain & Supervised Learning (Fine-tuning)](#single-domain--supervised-learning-fine-tuning)
   - [Single Domain & Unsupervised Learning](#single-domain--unsupervised-learning)
   - [Multi-domain & Supervised Learning (Fine-tuning)](#multi-domain--supervised-learning-fine-tuning)
   - [Multi-domain & Unsupervised Learning](#multi-domain--unsupervised-learning)
   - [Few-shot and Zero-shot Inference](#few-shot-and-zero-shot-inference)
##    Data
### [Single Task & Single Domain](#single-task--single-domain)
*    _(arXiv 2024.02)_ LPNL: Scalable Link Prediction with Large Language Models [[paper]](https://arxiv.org/abs/2401.13227)
*    _(ICLR'25)_ Disentangled Representation Learning with Large Language Models for Text-Attributed Graphs [[paper]](https://arxiv.org/abs/2310.18152)
*    _(arXiv 2024.10)_ Language Models are Graph Learners [[paper]](https://arxiv.org/abs/2410.02296) 
*    _(arXiv 2024.08)_ Learning Graph Quantized Tokenizers for Transformers [[paper]](https://arxiv.org/abs/2410.13798)
*    _(arXiv 2024.01)_ Link Prediction on Textual Edge Graphs [[paper]](https://arxiv.org/abs/2405.16606)
*    _(arXiv 2024.05)_ Unleashing the Potential of Text-attributed Graphs: Automatic Relation Decomposition via Large Language Models [[paper]](https://arxiv.org/abs/2405.18581)
*    _(arXiv 2024.05)_ TAGA: Text-Attributed Graph Self-Supervised Learning by Synergizing Graph and Text Mutual Transformations [[paper]](https://arxiv.org/abs/2405.16800)
*    _(arXiv 2024.10)_ TAGExplainer: Narrating Graph Explanations for Text-Attributed Graph Learning Models [[paper]](https://arxiv.org/abs/2410.15268)
*    _(arXiv 2024.08)_ Distilling Large Language Models for Text-Attributed Graph Learning [[paper]](https://arxiv.org/abs/2402.12022)
*    _(ICLR'25)_ Curriculum GNN-LLM Alignment for Text-Attributed Graphs [[paper]](https://openreview.net/forum?id=tmwR707odU)
*    _(ICLR'25)_ DP-GPL: Differentially Private Graph Prompt Learning [[paper]](https://openreview.net/forum?id=dSQtMx6dPE)
*    _(KDD'22)_ GPPT: Graph Pre-training and Prompt Tuning to Generalize Graph Neural Networks[[paper]](https://openreview.net/forum?id=VqgbNXL4dQF)
*    _(arXiv 2023.04)_ train Your Own GNN Teacher: Graph-Aware Distillation on Textual Graphs[[paper]](https://arxiv.org/abs/2304.10668)
*    _(ICLR'25)_ GraphBridge: Towards Arbitrary Transfer Learning in GNNs [[paper]](https://openreview.net/forum?id=gjRhw5S3A4)
*    _(ICLR'22)_ Node Feature Extraction by Self-Supervised Multi-scale Neighborhood Prediction [[paper]](https://arxiv.org/abs/2111.00064)
*    _(ICLR'23)_ Learning on Large-scale Text-attributed Graphs via Variational Inference [[paper]](https://arxiv.org/abs/2210.14709)
*    _(ICLR'24)_ Label-free Node Classification on Graphs with Large Language Models (LLMS) [[paper]](https://arxiv.org/abs/2310.04668)
*    _(ICLR'24)_ Harnessing Explanations: LLM-to-LM Interpreter for Enhanced Text-Attributed Graph Representation Learning [[paper]](https://arxiv.org/abs/2305.19523)
*    _(IJCAI'24)_ Efficient Tuning and Inference for Large Language Models on Textual Graphs [[paper]](https://arxiv.org/abs/2401.15569)
*    _(KDD'24)_ GAugLLM: Improving Graph Contrastive Learning for Text-Attributed Graphs with Large Language Models [[paper]](https://arxiv.org/abs/2406.11945)
*    _(KDD'24)_ HiGPT: Heterogeneous Graph Language Model [[paper]](https://arxiv.org/abs/2402.16024)
*    _(ICLR'25)_ Link Prediction on Text Attributed Graphs: A New Benchmark and Efficient LM-nested GNN Design [[paper]](https://openreview.net/forum?id=fpTh0UxcmQ)
*    _(NeurIPS'23)_ Universal Prompt Tuning for Graph Neural Networks [[paper]](https://openreview.net/forum?id=0LmWBhIYLi)
*    _(ICLR'25)_ Text Attributed Graph Node Classification Using Sheaf Neural Networks and Large Language Models [[paper]](https://openreview.net/forum?id=V8cMqUZT8o)
*    _(SIGIR'23)_ Augmenting Low-Resource Text Classification with Graph-Grounded Pre-training and Prompting [[paper]](https://arxiv.org/abs/2305.03324)
*    _(ICLR'25)_ Large Language Models Based Gragh Convolution For Text-Attributed Networks [[paper]](https://openreview.net/forum?id=x5FfUvsLIE)
*    _(WWW'24)_ Can GNN be Good Adapter for LLMs? [[paper]](https://arxiv.org/abs/2402.12984)
*    _(WWW'24)_ Can we Soff Prompt LLMs for Graph Learning Tasks? [[paper]](https://dl.acm.org/doi/abs/10.1145/3589335.3651476)
*    _(KDD'24)_ ZeroG: Investigating Cross-dataset Zero-shot Transferability in Graphs [[paper]](https://arxiv.org/abs/2402.11235)
### [Single Task & Multi Domain](#single-task--multi-domain)
*    _(arXiv'24)_ GraphAny: A Foundation Model for
Node Classiffcation on Any Graph [[paper]](https://arxiv.org/abs/2405.20445)
*    _(arXiv'24)_ GraphFM: A generalist graph transformer that learns transferable representations across diverse domains [[paper]](https://openreview.net/forum?id=zaxyuX8eqw)
*    _(WWW'23)_ GraphPrompt: Unifying Pre-Training and Downstream Tasks for Graph Neural Networks [[paper]](https://arxiv.org/abs/2302.08043)
### [Multi Task & Single Domain](#multi-task--single-domain)
*    _(ACL'23)_ Patton: Language Model Pretraining on Text-Rich Networks [[paper]](https://arxiv.org/abs/2305.12268)
*    _(arXiv 2024.07)_ ConGraT: Self-Supervised Contrastive Pretraining for Joint Graph and Text Embeddings [[paper]](https://arxiv.org/abs/2305.14321)
*    _(arXiv 2023.08)_ SimTeG: A Frustratingly Simple Approach Improves Textual Graph Learning [[paper]](https://arxiv.org/abs/2308.02565)
*    _(arXiv 2024.10)_ FineMolTex: Towards Fine-grained Molecular Graph-Text Pre-training [[paper]](https://arxiv.org/abs/2409.14106)
*    _(arXiv 2024.01)_ HIGHT: Hierarchical Graph Tokenization for Graph-Language Alignment [[paper]](https://arxiv.org/abs/2406.14021)
*    _(arXiv 2024.09)_ Generalizing Graph Transformers Across Diverse Graphs and Tasks via Pre-Training on Industrial-Scale Data [[paper]](https://arxiv.org/abs/2407.03953)
*    _(EACL'24)_ Language is All a Graph Needs [[paper]](https://openreview.net/forum?id=kZvv5CPz8i)
*    _(CoRR'21)_ PGT: A Progressive Method for Training Models on Long Videos [[paper]](https://openreview.net/forum?id=qvORFOSiuY)
*    _(EMNLP'23)_ GRENADE: Graph-Centric Language Model for Self-Supervised Representation Learning on Text-Attributed Graphs [[paper]](https://arxiv.org/abs/2310.15109)
*    _(EMNLP'23)_ Pretraining Language Models with Text-Attributed Heterogeneous Graphs [[paper]](https://arxiv.org/abs/2310.12580)
*    _(ICLR'25)_ Low-cost Enhancer for Text Attributed Graph Learning via Graph Alignment [[paper]](https://openreview.net/forum?id=yrnrvfXFaV)
*    _(ICML'24)_ LLaGA: Large Language and Graph Assistant [[paper]](https://arxiv.org/abs/2402.08170)
*    _(ICML'24)_ A Multi-View Mixture-of-Experts based on Language and Graphs for Molecular Properties Prediction [[paper]](https://openreview.net/forum?id=PkDHmg2JLI)
*    _(SIGIR'24)_ GraphGPT: Graph Instruction Tuning for Large Language Models [[paper]](https://arxiv.org/abs/2310.13023)
*    _(KDD'23)_ Graph-Aware Language Model Pre-Training on a Large Graph Corpus Can Help Multiple Graph Applications [[paper]](https://arxiv.org/abs/2306.02592)
*    _(KDD'24)_ ZeroG: Investigating Cross-dataset Zero-shot Transferability in Graphs [[paper]](https://arxiv.org/abs/2402.11235)
*    _(ICLR'25)_ LLM as GNN: Graph Vocabulary Learning for Graph Foundation Model [[paper]](https://openreview.net/forum?id=1FY1apsMxc)
*    _(SIGIR'24)_ TouchUp-G: Improving Feature Representation through Graph-Centric Finetuning [[paper]](https://arxiv.org/abs/2309.13885)
*    _(WWW'24)_ GraphTranslator: Aligning Graph Model to Large Language Model for Open-ended Tasks [[paper]](https://arxiv.org/abs/2402.07197)
*    _(arXiv 2023.10)_ GraphText: Graph Reasoning in Text Space [[paper]](https://arxiv.org/abs/2310.01089)
*    _(KDD'23)_ All in One: Multi-task Prompting for Graph Neural Networks [[paper]](https://arxiv.org/abs/2307.01504)
*    _(ICLR'25)_ One Model for One Graph: A New Perspective for Pretraining with Cross-domain Graphs [[paper]](https://openreview.net/forum?id=10vaHIOdEe)
### [Multi Task & Multi Domain](#multi-task--multi-domain)
*    _(ACL'24)_ InstructGraph: Boosting Large Language Models via Graph-centric Instruction Tuning and Preference Alignment [[paper]](https://arxiv.org/abs/2402.08785)
*    _(arXiv 2023.07)_ GPT4Graph: Can Large Language Models Understand Graph Structured Data ? An Empirical Evaluation and Benchmarking [[paper]](https://arxiv.org/abs/2305.15066)
*    _(arXiv 2024.08)_ AnyGraph: Graph Foundation Model in the Wild [[paper]](https://arxiv.org/abs/2408.10700)
*    _(arXiv 2024.07)_ GOFA: A Generative One-For-All Model for Joint Graph Language Modeling [[paper]](https://arxiv.org/abs/2408.10700)
*    _(arXiv 2024.10)_ Towards Graph Foundation Models: The Perspective of Zero-shot Reasoning on Knowledge Graphs [[paper]](https://arxiv.org/abs/2410.12609)
*    _(arXiv 2024.08)_ UniGraph: Learning a Unified Cross-Domain Foundation Model for Text-Attributed Graphs [[paper]](https://arxiv.org/abs/2402.13630)
*    _(arXiv 2024.10)_OpenGraph: Towards Open Graph Foundation Models [[paper]](https://arxiv.org/abs/2403.01121)
*    _(ICLR'25)_ GFSE: A Foundational Model For Graph Structural Encoding [[paper]](https://openreview.net/forum?id=JQT6iGrXTh)
*    _(ICLR'25)_ Towards Graph Foundation Models: Learning Generalities Across Graphs via Task-trees [[paper]](https://openreview.net/forum?id=kSBIEkHzon)
*    _(ICLR'25)_ GL-Fusion: Rethinking the Combination of Graph Neural Network and Large Language model [[paper]](https://openreview.net/forum?id=exnoX9Iaik)
*    _(ICLR'25)_ GraphBridge: Towards Arbitrary Transfer Learning in GNNs [[paper]](https://openreview.net/forum?id=gjRhw5S3A4)
*    _(ICLR'24)_ One for All: Towards Training One Graph Model for All Classification Tasks [[paper]](https://arxiv.org/abs/2310.00149)
*    _(NeurIPS'23)_ PRODIGY: Enabling In-context Learning Over Graphs [[paper]](https://openreview.net/forum?id=pLwYhNNnoR)
*    _(NeurIPS'23)_ WalkLM: A Uniform Language Model Fine-tuning Framework for Attributed Graph Embedding [[paper]](https://openreview.net/forum?id=ADbGXyx7U7)
*    _(ICLR'25)_ One Model for One Graph: A New Perspective for Pretraining with Cross-domain Graphs [[paper]](https://openreview.net/forum?id=10vaHIOdEe)
*    _(arXiv 2024.03)_ MuseGraph: Graph-oriented Instruction Tuning of Large Language Models for Generic Graph Mining [[paper]](https://arxiv.org/abs/2403.04780)
*    _(arXiv 2024.10)_ RAGraph: A General Retrieval-Augmented Graph Learning Framework [[paper]](https://arxiv.org/abs/2410.23855)
*    _(arXiv 2024.05)_ GraphAlign: Pretraining One Graph Neural Network on Multiple Graphs via Feature Alignment[[paper]](https://arxiv.org/abs/2406.02953)
*    _(ICLR'25)_ Edge Prompt Tuning for Graph Neural Networks [[paper]](https://openreview.net/forum?id=92vMaHotTM)
*    _(WWW'23)_ GraphPrompt: Unifying Pre-Training and Downstream Tasks for Graph Neural Networks [[paper]](https://arxiv.org/abs/2302.08043)
*    _(WWW'23)_ MultiGPrompt for Multi-Task Pre-Training and Prompting on Graphs [[paper]](https://arxiv.org/abs/2312.03731)
### Graph Reasoning  
*    _(arXiv 2023.10)_ GraphLLM: Boosting Graph Reasoning Ability of Large Language Model [[paper]](https://arxiv.org/abs/2310.05845)
*   _(arXiv 2024.10)_ Scalable and Accurate Graph Reasoning with LLM-based Multi-Agents [[paper]](https://arxiv.org/abs/2410.05130)
*   _(arXiv 2024.2)_ Let Your Graph Do the Talking: Encoding Structured Data for LLMs [[paper]](https://arxiv.org/abs/2402.05862)
*   _(ICLR'24)_ Talk like a Graph: Encoding Graphs for Large Language Models [[paper]](https://arxiv.org/abs/2310.04560)
*   _(NeurIPS'23)_ Can Language Models Solve Graph Problems in Natural Language? [[paper]](https://arxiv.org/abs/2305.10037)
##    Model
###    GNN and LLM as Independent Collaborative Modules

*    _(arXiv 2024.07)_ ConGraT: Self-Supervised Contrastive Pretraining for Joint Graph and Text Embeddings [[paper]](https://arxiv.org/abs/2305.14321)
*    _(arXiv 2023.08)_ SimTeG: A Frustratingly Simple Approach Improves Textual Graph Learning [[paper]](https://arxiv.org/abs/2308.02565)
*    _(arXiv 2024.10)_ Language Models are Graph Learners [[paper]](https://arxiv.org/abs/2410.02296) 
*    _(arXiv 2024.10)_ FineMolTex: Towards Fine-grained Molecular Graph-Text Pre-training [[paper]](https://arxiv.org/abs/2409.14106)
*   _(arXiv 2024.2)_ Let Your Graph Do the Talking: Encoding Structured Data for LLMs [[paper]](https://arxiv.org/abs/2402.05862)
*    _(arXiv 2024.01)_ Link Prediction on Textual Edge Graphs [[paper]](https://arxiv.org/abs/2405.16606)
*    _(arXiv 2024.05)_ TAGA: Text-Attributed Graph Self-Supervised Learning by Synergizing Graph and Text Mutual Transformations [[paper]](https://arxiv.org/abs/2405.16800)
*    _(arXiv 2024.08)_ UniGraph: Learning a Unified Cross-Domain Foundation Model for Text-Attributed Graphs [[paper]](https://arxiv.org/abs/2402.13630)
*    _(arXiv 2024.08)_ Distilling Large Language Models for Text-Attributed Graph Learning [[paper]](https://arxiv.org/abs/2402.12022)
*    _(ICLR'25)_ Curriculum GNN-LLM Alignment for Text-Attributed Graphs [[paper]](https://openreview.net/forum?id=tmwR707odU)
*    _(EMNLP'23)_ GRENADE: Graph-Centric Language Model for Self-Supervised Representation Learning on Text-Attributed Graphs [[paper]](https://arxiv.org/abs/2310.15109)
*    _(EMNLP'23)_ Pretraining Language Models with Text-Attributed Heterogeneous Graphs  [[paper]](https://arxiv.org/abs/2310.12580)
*    _(arXiv 2024.05)_ Unleashing the Potential of Text-attributed Graphs: Automatic Relation Decomposition via Large Language Models [[paper]](https://arxiv.org/abs/2405.18581)
*    _(ICLR'25)_ GraphBridge: Towards Arbitrary Transfer Learning in GNNs [[paper]](https://openreview.net/forum?id=gjRhw5S3A4)
*    _(ICLR'25)_ Low-cost Enhancer for Text Attributed Graph Learning via Graph Alignment [[paper]](https://openreview.net/forum?id=yrnrvfXFaV)
*    _(ICLR'22)_ Node Feature Extraction by Self-Supervised Multi-scale Neighborhood Prediction [[paper]](https://arxiv.org/abs/2111.00064)
*    _(ICLR'23)_ Learning on Large-scale Text-attributed Graphs via Variational Inference [[paper]](https://arxiv.org/abs/2210.14709)
*    _(ICLR'24)_ Label-free Node Classification on Graphs with Large Language Models (LLMS) [[paper]](https://arxiv.org/abs/2310.04668)
*    _(ICLR'24)_ Harnessing Explanations: LLM-to-LM Interpreter for Enhanced Text-Attributed Graph Representation Learning [[paper]](https://arxiv.org/abs/2305.19523)
*    _(ICLR'25)_ Link Prediction on Text Attributed Graphs: A New Benchmark and Efficient LM-nested GNN Design [[paper]](https://openreview.net/forum?id=fpTh0UxcmQ)
*    _(ICLR'25)_ One Model for One Graph: A New Perspective for Pretraining with Cross-domain Graphs [[paper]](https://openreview.net/forum?id=10vaHIOdEe)
*    _(SIGIR'23)_ Augmenting Low-Resource Text Classification with Graph-Grounded Pre-training and Prompting [[paper]](https://arxiv.org/abs/2305.03324)
*    _(SIGIR'24)_ TouchUp-G: Improving Feature Representation through Graph-Centric Finetuning [[paper]](https://arxiv.org/abs/2309.13885)
*    _(ICLR'25)_ Large Language Models Based Gragh Convolution For Text-Attributed Networks [[paper]](https://openreview.net/forum?id=x5FfUvsLIE)
*    _(WWW'24)_ GraphTranslator: Aligning Graph Model to Large Language Model for Open-ended Tasks [[paper]](https://arxiv.org/abs/2402.07197)
*    _(ICML'24)_ A Multi-View Mixture-of-Experts based on Language and Graphs for Molecular Properties Prediction [[paper]](https://openreview.net/forum?id=PkDHmg2JLI)
###    GNN-enhanced LLM (Learnable)
*    _(ICLR'25)_ Disentangled Representation Learning with Large Language Models for Text-Attributed Graphs [[paper]](https://arxiv.org/abs/2310.18152)
*    _(arXiv 2024.07)_ GOFA: A Generative One-For-All Model for Joint Graph Language Modeling [[paper]](https://arxiv.org/abs/2408.10700)
*    _(arXiv 2024.01)_ HIGHT: Hierarchical Graph Tokenization for Graph-Language Alignment [[paper]](https://arxiv.org/abs/2406.14021)
*    _(ICLR'25)_ GL-Fusion: Rethinking the Combination of Graph Neural Network and Large Language model [[paper]](https://openreview.net/forum?id=exnoX9Iaik)
*    _(ICML'24)_ LLaGA: Large Language and Graph Assistant [[paper]](https://arxiv.org/abs/2402.08170)
*    _(IJCAI'24)_ Efficient Tuning and Inference for Large Language Models on Textual Graphs [[paper]](https://arxiv.org/abs/2401.15569)
*    _(KDD'24)_ HiGPT: Heterogeneous Graph Language Model [[paper]](https://arxiv.org/abs/2402.16024)
*    _(KDD'24)_ ZeroG: Investigating Cross-dataset Zero-shot Transferability in Graphs [[paper]](https://arxiv.org/abs/2402.11235)
*    _(NeurIPS'23)_ WalkLM: A Uniform Language Model Fine-tuning Framework for Attributed Graph Embedding [[paper]](https://openreview.net/forum?id=ADbGXyx7U7)
*    _(arXiv 2024.08)_ Learning Graph Quantized Tokenizers for Transformers [[paper]](https://arxiv.org/abs/2410.13798)
*    _(ICLR'25)_ Text Attributed Graph Node Classification Using Sheaf Neural Networks and Large Language Models [[paper]](https://openreview.net/forum?id=V8cMqUZT8o)
*    _(ICLR'25)_ LLM as GNN: Graph Vocabulary Learning for Graph Foundation Model [[paper]](https://openreview.net/forum?id=1FY1apsMxc)
*    _(SIGIR'24)_ GraphGPT: Graph Instruction Tuning for Large Language Models [[paper]](https://arxiv.org/abs/2310.13023)
*    _(WWW'24)_ Can GNN be Good Adapter for LLMs? [[paper]](https://arxiv.org/abs/2402.12984)
*    _(WWW'24)_ Can we Soff Prompt LLMs for Graph Learning Tasks? [[paper]](https://dl.acm.org/doi/abs/10.1145/3589335.3651476)
*    _(KDD'23)_ Graph-Aware Language Model Pre-Training on a Large Graph Corpus Can Help Multiple Graph Applications [[paper]](https://arxiv.org/abs/2306.02592)

###    LLM-enhanced GNN (Learnable)
*    _(ACL'23)_ Patton: Language Model Pretraining on Text-Rich Networks [[paper]](https://arxiv.org/abs/2305.12268)
*    _(arXiv 2023.10)_ GraphLLM: Boosting Graph Reasoning Ability of Large Language Model [[paper]](https://arxiv.org/abs/2310.05845)
*    _(arXiv 2024.08)_ AnyGraph: Graph Foundation Model in the Wild [[paper]](https://arxiv.org/abs/2408.10700)
*    _(arXiv'24)_ GraphFM: A generalist graph transformer that learns transferable representations across diverse domains [[paper]](https://openreview.net/forum?id=zaxyuX8eqw)
*    _(CoRR'21)_ PGT: A Progressive Method for Training Models on Long Videos [[paper]](https://openreview.net/forum?id=qvORFOSiuY)
*    _(arXiv 2024.10)_ Towards Graph Foundation Models: The Perspective of Zero-shot Reasoning on Knowledge Graphs [[paper]](https://arxiv.org/abs/2410.12609)
*    _(arXiv 2024.10)_OpenGraph: Towards Open Graph Foundation Models [[paper]](https://arxiv.org/abs/2403.01121)
*    _(ICLR'25)_ GFSE: A Foundational Model For Graph Structural Encoding [[paper]](https://openreview.net/forum?id=JQT6iGrXTh)
*    _(ICLR'24)_ One for All: Towards Training One Graph Model for All Classification Tasks [[paper]](https://arxiv.org/abs/2310.00149)
*    _(KDD'24)_ GAugLLM: Improving Graph Contrastive Learning for Text-Attributed Graphs with Large Language Models [[paper]](https://arxiv.org/abs/2406.11945)
*    _(ECML PKDD'23)_ Train Your Own GNN Teacher: Graph-Aware Distillation on Textual Graphs [[paper]](https://arxiv.org/abs/2304.10668)
*    _(arXiv 2024.05)_ GraphAlign: Pretraining One Graph Neural Network on Multiple Graphs via Feature Alignment[[paper]](https://arxiv.org/abs/2406.02953)
*    _(ICLR'25)_ GraphProp: Training the Graph Foundation Models using Graph Properties [[paper]](https://openreview.net/forum?id=7WgOB2nUaS)
*    _(ICLR'25)_ One Model for One Graph: A New Perspective for Pretraining with Cross-domain Graphs [[paper]](https://openreview.net/forum?id=10vaHIOdEe)

###    GNN-only
*    _(arXiv'24)_ GraphAny: A Foundation Model for
Node Classiffcation on Any Graph [[paper]](https://arxiv.org/abs/2405.20445)
*    _(arXiv'24)_ GraphFM: A generalist graph transformer that learns transferable representations across diverse domains [[paper]](https://openreview.net/forum?id=zaxyuX8eqw)
*    _(ICLR'25)_ DP-GPL: Differentially Private Graph Prompt Learning [[paper]](https://openreview.net/forum?id=dSQtMx6dPE)
*    _(ICLR'25)_ Edge Prompt Tuning for Graph Neural Networks [[paper]](https://openreview.net/forum?id=92vMaHotTM)
*    _(ICLR'25)_ GraphBridge: Towards Arbitrary Transfer Learning in GNNs [[paper]](https://openreview.net/forum?id=gjRhw5S3A4)
*    _(KDD'23)_ All in One: Multi-task Prompting for Graph Neural Networks [[paper]](https://arxiv.org/abs/2307.01504)
*    _(NeurIPS'23)_ Universal Prompt Tuning for Graph Neural Networks [[paper]](https://openreview.net/forum?id=0LmWBhIYLi)
*    _(NeurIPS'23)_ PRODIGY: Enabling In-context Learning Over Graphs [[paper]](https://openreview.net/forum?id=pLwYhNNnoR)
*    _(WWW'23)_ GraphPrompt: Unifying Pre-Training and Downstream Tasks for Graph Neural Networks [[paper]](https://arxiv.org/abs/2302.08043)
*    _(WWW'23)_ MultiGPrompt for Multi-Task Pre-Training and Prompting on Graphs [[paper]](https://arxiv.org/abs/2312.03731)
*    _(arXiv 2024.10)_ RAGraph: A General Retrieval-Augmented Graph Learning Framework [[paper]](https://arxiv.org/abs/2410.23855)
*    _(KDD'22)_ GPPT: Graph Pre-training and Prompt Tuning to Generalize Graph Neural Networks[[paper]](https://openreview.net/forum?id=VqgbNXL4dQF)
*    _(ICLR'25)_ Towards Graph Foundation Models: Learning Generalities Across Graphs via Task-trees [[paper]](https://openreview.net/forum?id=kSBIEkHzon)
###    LLM-only
*    _(ACL'24)_ InstructGraph: Boosting Large Language Models via Graph-centric Instruction Tuning and Preference Alignment [[paper]](https://arxiv.org/abs/2402.08785)
*    _(arXiv 2024.02)_ LPNL: Scalable Link Prediction with Large Language Models [[paper]](https://arxiv.org/abs/2401.13227)
*    _(arXiv 2023.07)_ GPT4Graph: Can Large Language Models Understand Graph Structured Data ? An Empirical Evaluation and Benchmarking [[paper]](https://arxiv.org/abs/2305.15066)
*    _(arXiv 2023.10)_ GraphText: Graph Reasoning in Text Space [[paper]](https://arxiv.org/abs/2310.01089)
*   _(arXiv 2024.10)_ Scalable and Accurate Graph Reasoning with LLM-based Multi-Agents [[paper]](https://arxiv.org/abs/2410.05130)
*    _(arXiv 2024.10)_ TAGExplainer: Narrating Graph Explanations for Text-Attributed Graph Learning Models [[paper]](https://arxiv.org/abs/2410.15268)
*    _(EACL'24)_ Language is All a Graph Needs [[paper]](https://openreview.net/forum?id=kZvv5CPz8i)
*   _(ICLR'24)_ Talk like a Graph: Encoding Graphs for Large Language Models [[paper]](https://arxiv.org/abs/2310.04560)
*   _(NeurIPS'23)_ Can Language Models Solve Graph Problems in Natural Language? [[paper]](https://arxiv.org/abs/2305.10037)
*    _(arXiv 2024.03)_ MuseGraph: Graph-oriented Instruction Tuning of Large Language Models for Generic Graph Mining [[paper]](https://arxiv.org/abs/2403.04780)
##    Task
###    Single Domain & Supervised Learning (Fine-tuning)
*    _(arXiv 2024.02)_ LPNL: Scalable Link Prediction with Large Language Models [[paper]](https://arxiv.org/abs/2401.13227)
*    _(ICLR'25)_ Disentangled Representation Learning with Large Language Models for Text-Attributed Graphs [[paper]](https://arxiv.org/abs/2310.18152) 
*    _(arXiv 2023.10)_ GraphLLM: Boosting Graph Reasoning Ability of Large Language Model [[paper]](https://arxiv.org/abs/2310.05845)
*    _(arXiv 2023.08)_ SimTeG: A Frustratingly Simple Approach Improves Textual Graph Learning [[paper]](https://arxiv.org/abs/2308.02565)
*    _(arXiv 2024.10)_ Language Models are Graph Learners [[paper]](https://arxiv.org/abs/2410.02296) 
*    _(arXiv 2024.08)_ Learning Graph Quantized Tokenizers for Transformers [[paper]](https://arxiv.org/abs/2410.13798)
*    _(arXiv 2024.01)_ HIGHT: Hierarchical Graph Tokenization for Graph-Language Alignment [[paper]](https://arxiv.org/abs/2406.14021)
*    _(arXiv 2024.05)_ Unleashing the Potential of Text-attributed Graphs: Automatic Relation Decomposition via Large Language Models [[paper]](https://arxiv.org/abs/2405.18581)
*    _(ICLR'25)_ Curriculum GNN-LLM Alignment for Text-Attributed Graphs [[paper]](https://openreview.net/forum?id=tmwR707odU)
*    _(ICLR'25)_ DP-GPL: Differentially Private Graph Prompt Learning [[paper]](https://openreview.net/forum?id=dSQtMx6dPE)
*    _(EACL'24)_ Language is All a Graph Needs [[paper]](https://openreview.net/forum?id=kZvv5CPz8i)
*    _(ECML PKDD'23)_ Train Your Own GNN Teacher: Graph-Aware Distillation on Textual Graphs [[paper]](https://arxiv.org/abs/2304.10668)
*    _(ICLR'25)_ GraphBridge: Towards Arbitrary Transfer Learning in GNNs [[paper]](https://openreview.net/forum?id=gjRhw5S3A4)
*    _(ICLR'25)_ Low-cost Enhancer for Text Attributed Graph Learning via Graph Alignment [[paper]](https://openreview.net/forum?id=yrnrvfXFaV)
*    _(ICLR'25)_ GraphProp: Training the Graph Foundation Models using Graph Properties [[paper]](https://openreview.net/forum?id=7WgOB2nUaS)
*    _(ICLR'23)_ Learning on Large-scale Text-attributed Graphs via Variational Inference [[paper]](https://arxiv.org/abs/2210.14709)
*    _(ICLR'22)_ Node Feature Extraction by Self-Supervised Multi-scale Neighborhood Prediction [[paper]](https://arxiv.org/abs/2111.00064)
*    _(ICLR'24)_ Harnessing Explanations: LLM-to-LM Interpreter for Enhanced Text-Attributed Graph Representation Learning [[paper]](https://arxiv.org/abs/2305.19523)
*    _(ICML'24)_ LLaGA: Large Language and Graph Assistant [[paper]](https://arxiv.org/abs/2402.08170)
*    _(ICML'24)_ A Multi-View Mixture-of-Experts based on Language and Graphs for Molecular Properties Prediction [[paper]](https://openreview.net/forum?id=PkDHmg2JLI)
*    _(IJCAI'24)_ Efficient Tuning and Inference for Large Language Models on Textual Graphs [[paper]](https://arxiv.org/abs/2401.15569)
*    _(KDD'24)_ HiGPT: Heterogeneous Graph Language Model [[paper]](https://arxiv.org/abs/2402.16024)
*    _(ICLR'25)_ Link Prediction on Text Attributed Graphs: A New Benchmark and Efficient LM-nested GNN Design [[paper]](https://openreview.net/forum?id=fpTh0UxcmQ)
*    _(NeurIPS'23)_ Universal Prompt Tuning for Graph Neural Networks [[paper]](https://openreview.net/forum?id=0LmWBhIYLi)
*    _(ICLR'25)_ LLM as GNN: Graph Vocabulary Learning for Graph Foundation Model [[paper]](https://openreview.net/forum?id=1FY1apsMxc)
*    _(ICLR'25)_ Text Attributed Graph Node Classification Using Sheaf Neural Networks and Large Language Models [[paper]](https://openreview.net/forum?id=V8cMqUZT8o)
*    _(SIGIR'24)_ GraphGPT: Graph Instruction Tuning for Large Language Models [[paper]](https://arxiv.org/abs/2310.13023)
*    _(SIGIR'24)_ TouchUp-G: Improving Feature Representation through Graph-Centric Finetuning [[paper]](https://arxiv.org/abs/2309.13885)
*    _(ICLR'25)_ Large Language Models Based Gragh Convolution For Text-Attributed Networks [[paper]](https://openreview.net/forum?id=x5FfUvsLIE)
*    _(WWW'24)_ Can GNN be Good Adapter for LLMs? [[paper]](https://arxiv.org/abs/2402.12984)
*    _(WWW'24)_ GraphTranslator: Aligning Graph Model to Large Language Model for Open-ended Tasks [[paper]](https://arxiv.org/abs/2402.07197)
*    _(WWW'24)_ Can we Soff Prompt LLMs for Graph Learning Tasks? [[paper]](https://dl.acm.org/doi/abs/10.1145/3589335.3651476)
*    _(KDD'22)_ GPPT: Graph Pre-training and Prompt Tuning to Generalize Graph Neural Networks[[paper]](https://openreview.net/forum?id=VqgbNXL4dQF)

###    Single Domain & Unsupervised Learning

*    _(ACL'23)_ Patton: Language Model Pretraining on Text-Rich Networks [[paper]](https://arxiv.org/abs/2305.12268)
*    _(arXiv 2024.07)_ ConGraT: Self-Supervised Contrastive Pretraining for Joint Graph and Text Embeddings [[paper]](https://arxiv.org/abs/2305.14321)
*    _(arXiv 2024.10)_ FineMolTex: Towards Fine-grained Molecular Graph-Text Pre-training [[paper]](https://arxiv.org/abs/2409.14106)
*    _(arXiv 2024.01)_ Link Prediction on Textual Edge Graphs [[paper]](https://arxiv.org/abs/2405.16606)
*    _(CoRR'21)_ PGT: A Progressive Method for Training Models on Long Videos [[paper]](https://openreview.net/forum?id=qvORFOSiuY)
*    _(arXiv 2024.10)_ TAGExplainer: Narrating Graph Explanations for Text-Attributed Graph Learning Models [[paper]](https://arxiv.org/abs/2410.15268)
*    _(arXiv 2024.08)_ Distilling Large Language Models for Text-Attributed Graph Learning [[paper]](https://arxiv.org/abs/2402.12022)
*    _(EMNLP'23)_ GRENADE: Graph-Centric Language Model for Self-Supervised Representation Learning on Text-Attributed Graphs [[paper]](https://arxiv.org/abs/2310.15109)
*    _(EMNLP'23)_ Pretraining Language Models with Text-Attributed Heterogeneous Graphs [[paper]](https://arxiv.org/abs/2310.12580)
*    _(KDD'24)_ ZeroG: Investigating Cross-dataset Zero-shot Transferability in Graphs [[paper]](https://arxiv.org/abs/2402.11235)
*    _(SIGIR'23)_ Augmenting Low-Resource Text Classification with Graph-Grounded Pre-training and Prompting [[paper]](https://arxiv.org/abs/2305.03324)
*    _(KDD'24)_ GAugLLM: Improving Graph Contrastive Learning for Text-Attributed Graphs with Large Language Models [[paper]](https://arxiv.org/abs/2406.11945)
*    _(KDD'23)_ Graph-Aware Language Model Pre-Training on a Large Graph Corpus Can Help Multiple Graph Applications [[paper]](https://arxiv.org/abs/2306.02592)
*    _(ICLR'25)_ One Model for One Graph: A New Perspective for Pretraining with Cross-domain Graphs [[paper]](https://openreview.net/forum?id=10vaHIOdEe)

###    Multi-domain & Supervised Learning (Fine-tuning)

*    _(ACL'24)_ InstructGraph: Boosting Large Language Models via Graph-centric Instruction Tuning and Preference Alignment [[paper]](https://arxiv.org/abs/2402.08785)
*    _(ICLR'25)_ GraphBridge: Towards Arbitrary Transfer Learning in GNNs [[paper]](https://openreview.net/forum?id=gjRhw5S3A4)
*    _(KDD'23)_ All in One: Multi-task Prompting for Graph Neural Networks [[paper]](https://arxiv.org/abs/2307.01504)
*    _(ICLR'25)_ Edge Prompt Tuning for Graph Neural Networks [[paper]](https://openreview.net/forum?id=92vMaHotTM)
*    _(WWW'23)_ GraphPrompt: Unifying Pre-Training and Downstream Tasks for Graph Neural Networks [[paper]](https://arxiv.org/abs/2302.08043)
*    _(WWW'23)_ MultiGPrompt for Multi-Task Pre-Training and Prompting on Graphs [[paper]](https://arxiv.org/abs/2312.03731)
*    _(arXiv 2024.03)_ MuseGraph: Graph-oriented Instruction Tuning of Large Language Models for Generic Graph Mining [[paper]](https://arxiv.org/abs/2403.04780)
*    _(arXiv 2024.10)_ RAGraph: A General Retrieval-Augmented Graph Learning Framework [[paper]](https://arxiv.org/abs/2410.23855)
*    _(ICLR'25)_ GraphFM: A generalist graph transformer that learns transferable representations across diverse domains [[paper]](https://openreview.net/forum?id=zaxyuX8eqw)
*    _(ICLR'25)_ Towards Graph Foundation Models: Learning Generalities Across Graphs via Task-trees [[paper]](https://openreview.net/forum?id=kSBIEkHzon)

###    Multi-domain & Unsupervised Learning
*    _(arXiv 2024.08)_ AnyGraph: Graph Foundation Model in the Wild [[paper]](https://arxiv.org/abs/2408.10700)
*    _(arXiv 2024.07)_ GOFA: A Generative One-For-All Model for Joint Graph Language Modeling [[paper]](https://arxiv.org/abs/2408.10700)
*    _(arXiv'24)_ GraphAny: A Foundation Model for
Node Classiffcation on Any Graph [[paper]](https://arxiv.org/abs/2405.20445)
*    _(ICLR'25)_ Towards Graph Foundation Models: Learning Generalities Across Graphs via Task-trees [[paper]](https://openreview.net/forum?id=kSBIEkHzon)
*    _(arXiv 2024.08)_ UniGraph: Learning a Unified Cross-Domain Foundation Model for Text-Attributed Graphs [[paper]](https://arxiv.org/abs/2402.13630)
*    _(arXiv 2024.10)_OpenGraph: Towards Open Graph Foundation Models [[paper]](https://arxiv.org/abs/2403.01121)
*    _(ICLR'25)_ GFSE: A Foundational Model For Graph Structural Encoding [[paper]](https://openreview.net/forum?id=JQT6iGrXTh)
*    _(ICLR'25)_ GL-Fusion: Rethinking the Combination of Graph Neural Network and Large Language model [[paper]](https://openreview.net/forum?id=exnoX9Iaik)
*    _(arXiv 2024.07)_ GOFA: A Generative One-For-All Model for Joint Graph Language Modeling [[paper]](https://arxiv.org/abs/2408.10700)
*    _(NeurIPS'23)_ PRODIGY: Enabling In-context Learning Over Graphs [[paper]](https://openreview.net/forum?id=pLwYhNNnoR)
*    _(NeurIPS'23)_ WalkLM: A Uniform Language Model Fine-tuning Framework for Attributed Graph Embedding [[paper]](https://openreview.net/forum?id=ADbGXyx7U7)
*    _(arXiv 2024.05)_ GraphAlign: Pretraining One Graph Neural Network on Multiple Graphs via Feature Alignment[[paper]](https://arxiv.org/abs/2406.02953)
###    Few-shot and Zero-shot Inference
*    _(arXiv 2023.07)_ GPT4Graph: Can Large Language Models Understand Graph Structured Data ? An Empirical Evaluation and Benchmarking [[paper]](https://arxiv.org/abs/2305.15066)
*    _(arXiv 2023.10)_ GraphText: Graph Reasoning in Text Space [[paper]](https://arxiv.org/abs/2310.01089)
*   _(arXiv 2024.10)_ Scalable and Accurate Graph Reasoning with LLM-based Multi-Agents [[paper]](https://arxiv.org/abs/2410.05130)
*   _(arXiv 2024.2)_ Let Your Graph Do the Talking: Encoding Structured Data for LLMs [[paper]](https://arxiv.org/abs/2402.05862)
*   _(ICLR'24)_ Talk like a Graph: Encoding Graphs for Large Language Models [[paper]](https://arxiv.org/abs/2310.04560)
*   _(NeurIPS'23)_ Can Language Models Solve Graph Problems in Natural Language? [[paper]](https://arxiv.org/abs/2305.10037)
*    _(ICLR'24)_ Label-free Node Classification on Graphs with Large Language Models (LLMS) [[paper]](https://arxiv.org/abs/2310.04668)
