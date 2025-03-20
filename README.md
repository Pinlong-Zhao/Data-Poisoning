# Data Poisoning in Deep Learning: A Survey ☠️

> Data Poisoning in Deep Learning: A Survey
>
>
> 深度学习中的数据投毒：综述


<p align="center">
  <img src="assets/fig1.png" alt="Data poisoning" width="400" height="400"/>
</p>
<p align="center"><b>📌 Fig. 1.</b> Types of Adversarial Attacks.</p>


💉This repository is a collection of resources on **data poisoning in deep learning**, serving as a supplement to our survey paper:  
📜 "[Data Poisoning in Deep Learning: A Survey](https://arxiv.org/abs/ )" 

If you have any recommendations for missing work or suggestions, please feel free to:  
✦ [Submit a pull request](https://github.com/YOUR_REPO/Data-Poisoning/pulls)  
✦ [Contact us](mailto:YOUR_EMAIL) ✉️  
We appreciate your contributions and feedback! 

## Table of Contents 📋
⭐️ [Taxonomy of Poisoning Attacks](#taxonomy-of-poisoning-attacks)  
　🔹 [Attack Objective](#attack-objective)  
　🔹 [Attack Goal](#attack-goal)  
　🔹 [Attack Knowledge](#attack-knowledge)  
　🔹 [Attack Scope](#attack-scope)  
　🔹 [Attack Impact](#attack-impact)  
　🔹 [Attack Variability](#attack-variability)  
 
⭐️ [DATA POISONING ALGORITHMS](#data-poisoning-algorithms)  
　🔹 [Heuristic-based Attacks](#heuristic-based-attacks)  
　🔹 [Label Flipping Attacks](#label-flipping-attacks)  
　🔹 [Feature Space Attacks](#feature-space-attacks)  
　🔹 [Bilevel Optimization Attacks](#bilevel-optimization-attacks)  
　🔹 [Influence-based Attacks](#influence-based-attacks)  
　🔹 [Generative Attacks](#generative-attacks)  
 
⭐️ [DATA POISONING IN LARGE LANGUAGE MODELS](#data-poisoning-in-large-language-models)  
　🔹 [Pre-training](#pre-training)  
　🔹 [Fine-tuning](#fine-tuning)  
　🔹 [Preference Alignment](#preference-alignment)  
　🔹 [Instruction Tuning](#instruction-tuning)  
　🔹 [Prefix Tuning](#prefix-tuning)  
　🔹 [In-Context Learning Phase](#in-context-learning-icl-phase)  
　🔹 [Prompt Injection](#prompt-injection) 


## TAXONOMY OF POISONING ATTACKS

### 🔷 Attack Objective
#### 🌿 Label Modification Attack
- **Efficient label contamination attacks against black-box learning models.**<br>
*Zhao, Mengchen and An, Bo and Gao, Wei and Zhang, Teng.*<br>
IJCAI `2023`. [[Paper](https://dl.acm.org/doi/abs/10.5555/3172077.3172440)] [[Data](https://www.csie.ntu.edu.tw/~cjlin/libsvmtools/datasets/)]
- **Data poisoning attack by label flipping on splitfed learning.**<br>
*Gajbhiye, Saurabh, Priyanka Singh, and Shaifu Gupta.*<br>
RTIP2R `2022`. [[Paper](https://link.springer.com/chapter/10.1007/978-3-031-23599-3_30)]
- **A label flipping attack on machine learning model and its defense mechanism.**<br>
*Li, Qingru and Wang, Xinru and Wang, Fangwei and Wang, Changguang.*<br>
ICA3PP `2022`. [[Paper](https://link.springer.com/chapter/10.1007/978-3-031-22677-9_26)]
- **Label poisoning is all you need.**<br>
*Jha, Rishi and Hayase, Jonathan and Oh, Sewoong.*<br>
NeurIPS `2023`. [[Paper](https://proceedings.neurips.cc/paper_files/paper/2023/hash/e0c9b65fb3e41aaa86576df3ec33ad2e-Abstract-Conference.html)]
- **A Backdoor Approach with Inverted Labels Using Dirty Label-Flipping Attacks.**<br>
*Mengara, Orson.*<br>
IEEE Access `2024`. [[Paper](https://ieeexplore.ieee.org/abstract/document/10483076/)] [[Code](https://github.com/Trusted-AI/adversarial-robustness-toolbox/pull/2376)] [[Data](https://www.kaggle.com/datasets/mfekadu/darpa-timit-acousticphonetic-continuous-speech)]

#### 🌿 Input Modification Attack
- **Poison frogs! targeted clean-label poisoning attacks on neural networks.**<br>
*Shafahi, Ali and Huang, W Ronny and Najibi, Mahyar and Suciu, Octavian and Studer, Christoph and Dumitras, Tudor and Goldstein, Tom.*<br>
NeurIPS  `2018`. [[Paper](https://proceedings.neurips.cc/paper_files/paper/2018/hash/22722a343513ed45f14905eb07621686-Abstract.html)] [[Code](https://github.com/ashafahi/inceptionv3-transferLearn-poison)]
- **When does machine learning {FAIL}? generalized transferability for evasion and poisoning attacks.**<br>
*Suciu, Octavian and Marginean, Radu and Kaya, Yigitcan and Daume III, Hal and Dumitras, Tudor.*<br>
USENIX Security `2018`. [[Paper](https://www.usenix.org/conference/usenixsecurity18/presentation/suciu)][[Code](https://githubcom/sdsatumd)]
- **Transferable clean-label poisoning attacks on deep neural nets.**<br>
*Zhu, Chen and Huang, W Ronny and Li, Hengduo and Taylor, Gavin and Studer, Christoph and Goldstein, Tom.*<br>
ICML `2019`. [[Paper](https://proceedings.mlr.press/v97/zhu19a.html)] [[Code](https://github.com/zhuchen03/ConvexPolytopePosioning.git)] [[Data](https://github.com/kuangliu/
 pytorch-cifar)]
- **Practical poisoning attacks on neural networks.**<br>
*Guo, Junfeng and Liu, Cong.*<br>
ECCV `2020`. [[Paper](https://link.springer.com/chapter/10.1007/978-3-030-58583-9_9)] 
- **Bullseye polytope: A scalable clean-label poisoning attack with improved transferability.**<br>
*Aghakhani, Hojjat and Meng, Dongyu and Wang, Yu-Xiang and Kruegel, Christopher and Vigna, Giovanni.*<br>
EuroS&P `2021`. [[Paper](https://ieeexplore.ieee.org/abstract/document/9581207/)] [[Code](github.com/ucsb-seclab/BullseyePoison.)]
- **Optimizing millions of hyperparameters by implicit differentiation.**<br>
*Lorraine, Jonathan and Vicol, Paul and Duvenaud, David.*<br>
AISTATS `2020`. [[Paper](https://proceedings.mlr.press/v108/lorraine20a.html)]
- **Witches' brew: Industrial scale data poisoning via gradient matching.**<br>
*Geiping, Jonas and Fowl, Liam and Huang, W Ronny and Czaja, Wojciech and Taylor, Gavin and Moeller, Michael and Goldstein, Tom.*<br>
arXiv `2020`. [[Paper](https://arxiv.org/abs/2009.02276)] [[Code](https://github.com/JonasGeiping/
 poisoning-gradient-matching)]
- **.**<br>
* .*<br>
U `2022`. [[Paper]()]
- **.**<br>
* .*<br>
U `2022`. [[Paper]()]







#### 🌿 Data Modification Attack
- *Efficient label contamination attacks against black-box learning models.**<br>
*Zhao, Mengchen and An, Bo and Gao, Wei and Zhang, Teng.*<br>
IJCAI `2023`. [[Paper](https://dl.acm.org/doi/abs/10.5555/3172077.3172440)]






- **.**<br>
* .*<br>
U `2022`. [[Paper]()]
- **.**<br>
* .*<br>
U `2022`. [[Paper]()]


### 🔷 Attack Goal
#### 🌿 Untargeted Attack
#### 🌿 Targeted Attack
#### 🌿 Backdoor Attack

### 🔷 Attack Knowledge
#### 🌿 White-box Attack
#### 🌿 Black-box Attack
#### 🌿 Gray-box Attack

### 🔷 Attack Stealthiness
#### 🌿 Non-stealthy Attack
#### 🌿 Stealthy Attack

### 🔷 Attack Scope
#### 🌿 Single-Instance Attack
#### 🌿 Single-pattern Attack
#### 🌿 Single-class Attack
#### 🌿 Broad-scope Attack

### 🔷 Attack Impact
#### 🌿 Performance Attack
#### 🌿 Robustness Attack
#### 🌿 Fairness Attack

### 🔷 Attack Variability
#### 🌿 Static Attack
#### 🌿 Dynamic Attack


## TAXONOMY OF POISONING ALGORITHMS

### 🔷 Heuristic-based Attacks
### 🔷 Label Flipping Attacks
### 🔷 Feature Space Attacks
### 🔷 Bilevel Optimization Attacks
### 🔷 Influence-based Attacks
### 🔷 Generative Attacks


## DATA POISONING IN LARGE LANGUAGE MODELS

### 🔷 Pre-training
### 🔷 Fine-tuning
### 🔷 Preference Alignment
### 🔷 Instruction Tuning
### 🔷 Prefix Tuning
### 🔷 In-Context Learning
### 🔷 Prompt Injection




## Citation 📖 
The manuscript is avaliable in arXiv:
```sh
"Data Poisoning in Deep Learning: A Survey". arXiv preprint arXiv: [pdf]
```
