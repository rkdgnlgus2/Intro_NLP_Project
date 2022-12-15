# Introduction to NLP final Project
### team 강휘현, 김준오, 윤종선
---
## Google Colab Link
We used [google colab](https://colab.research.google.com/drive/1nxwctxLhl3365XYpvlqJMExGfqqQDfj6?usp=sharing) for training.

---

## Baseline
[Modular multi-source prediction of drug side-effects with DruGNN](https://arxiv.org/abs/2202.08147)

## Motivation and Idea
Tokenize SMILES format, then apply NLP method.
Try using BERT and tokenization.

## Experiment Design
- Dataset : PubChem(chemical structure data) + SIDER(side effect data)
- Tokenizer : Custom tokenizer (A list of vocabulary)
- Training : Pretraining BERT MLM -> mol2vec feature extraction -> Training DNN classifier

## Result  
Baseline : about 86% accuracy   
Ours : Average accuracy 63%... 

## Analysis & Explanation
DNN has no problem. We need better feature extractor. -> Better tokenizer.   
Currenet tokenizer provides too much C&O, which have less meanings.   
The most plausible improvement : Devising new tokenizer.   
So that we can get CCOC, =O,.... from    
'[CLS] C C O C ( = O ) C = C 1 C 1 ( C C 1 ) C [SEP]'

--- 