# POS Tagging using Hidden Markov Models and Viterbi Algorithm
Implementation of a Part-of-Speech tagger using Hidden Markov Models and the Viterbi algorithm from scratch.

This repository contains an implementation of a **Part-of-Speech (POS) tagging system**
using a **Hidden Markov Model (HMM)** and the **Viterbi decoding algorithm**, developed
entirely from scratch as part of an academic assignment.

No pre-built POS taggers, HMM libraries, or sequence decoding frameworks were used.

---

## 📘 Project Overview

The goal of this project is to predict the most probable sequence of POS tags for a given
sentence by modeling POS tagging as a **sequence labeling problem**.

- Observations: Words in a sentence  
- Hidden states: POS tags  
- Model: First-order Hidden Markov Model  
- Decoding: Viterbi dynamic programming algorithm  

The model explicitly constructs both the **Viterbi probability matrix** and the
**backpointer matrix** to recover the optimal tag sequence.

---

## 📂 Dataset

- **Universal Dependencies English Web Treebank (UD-EWT)**
- Gold-annotated corpus with Universal POS (UPOS) tags
- Training and test sets provided in CoNLL-U format

---

## ⚙️ Methodology

### HMM Parameter Estimation
The following probabilities are estimated using Maximum Likelihood Estimation (MLE):

- Initial probabilities  
- Transition probabilities  
- Emission probabilities  

### Unknown Word Handling
- Rare words in the training set are replaced with a special `<UNK>` token
- This enables the model to handle unseen words during testing

### Viterbi Algorithm
- Explicit construction of:
  - Viterbi matrix (dynamic programming table)
  - Backpointer matrix (for path reconstruction)
- Backtracking is used to recover the most probable POS tag sequence

---

## 📊 Evaluation

- Metric: **Tag-level accuracy**
- The model achieves competitive accuracy on the test set
- A confusion matrix is used for error analysis and qualitative evaluation

---

## 🛠️ Libraries Used

- Python
- NumPy
- Pandas
- collections (Counter, defaultdict)

(As per assignment constraints, no external NLP or HMM libraries were used.)

---

## 📁 Repository Structure


