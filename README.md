# HMM POS Tagging and Text Generation

A Natural Language Processing project exploring **Hidden Markov Models (HMMs)** for **Part-of-Speech (POS) tagging** and **text generation** using the NLTK Brown Corpus.

The project compares supervised, unsupervised, and semi-supervised HMM training approaches and also uses a trained HMM to generate text with temperature-controlled sampling.

## Overview

This project focuses on two main NLP tasks:

1. **Part-of-Speech Tagging**
   - Supervised HMM
   - Unsupervised HMM using Baum-Welch
   - Semi-supervised HMM

2. **HMM-based Text Generation**
   - POS-state transition sampling
   - Word emission sampling
   - Temperature-controlled generation

The Brown Corpus with the Universal POS tagset is used for training and evaluation.

## Features

- Hidden Markov Model based POS tagging
- Supervised HMM training
- Unsupervised HMM training with Baum-Welch
- Semi-supervised learning using labeled and unlabeled data
- 5-fold cross-validation
- Per-tag accuracy analysis
- Overall POS tagging accuracy comparison
- Brown Corpus integration
- Universal POS tagset
- HMM-based text generation
- Temperature-controlled state sampling
- Temperature-controlled word sampling
- Reproducible experiments using fixed random seeds

## POS Tagging Models

### Supervised HMM

The supervised model is trained using fully labeled `(word, POS-tag)` sentence pairs from the Brown Corpus.

### Unsupervised HMM

The unsupervised model removes the POS labels from the training data and learns HMM parameters using the **Baum-Welch algorithm**.

### Semi-Supervised HMM

The semi-supervised approach first trains an HMM using a smaller labeled portion of the training data and then refines the model using unlabeled data with Baum-Welch.

In the current experiment, the semi-supervised model uses **10% labeled data** before unsupervised refinement.

## Evaluation

The three approaches were evaluated using **5-fold cross-validation**.

| Model | Overall Accuracy |
|---|---:|
| Unsupervised HMM | 22.61% |
| Semi-Supervised HMM | 50.81% |
| Supervised HMM | 59.00% |

The supervised model achieved the highest overall POS-tagging accuracy in the experiment.

The project also analyzes accuracy for individual POS tags such as:

- NOUN
- VERB
- ADJ
- ADV
- DET
- PRON
- ADP
- CONJ
- NUM
- PRT

## Example POS Tagging

Example sentence:

```text
Today is a good day .
