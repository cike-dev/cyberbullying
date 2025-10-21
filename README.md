# DistilBERT vs Gemma-3-270M for Mobile Cyberbullying Detection

## Overview 
This study compares two lightweight transformer models — DistilBERT and Gemma-3 270M — for on-device cyberbullying detection on mobile platforms.
It explores quantization strategies (PTQ & QAT), latency, memory, and energy efficiency to support sustainable, privacy-preserving AI in smart-city contexts.

## Requirements
- Nvidia L4 GPU
- 22 GB VRAM
- CUDA 8.9

find the dataset here: https://huggingface.co/cike-dev/en_toxic_set

Finetuned Gemma model: https://huggingface.co/cike-dev/Gemma3ToxicTextClassifier

GGUF Gemma model: https://huggingface.co/cike-dev/Gemma3ToxicTextClassifier-Q8_0-GGUF

Finetuned DistilBERT model: https://huggingface.co/cike-dev/distilbert_toxic

DistilBERT PTE format: ...integrated in the apk

## Quick Start
### 1. Clone repo
git clone https://github.com/cike-dev/DistilBERT-vs-Gemma3-270M.git
cd DistilBERT-vs-Gemma3-270M

### 2. Install dependencies
pip install -r requirements.txt

### 3. Run training and evaluation
Run noteboks in a jupyter environment, e.g. google colab

## Reproducibility
- Random seeds: 42 / 2025 / 3045
- Dataset split: 70 % train – 20 % test – 10 % validation
- Quantization: DistilBERT (PTQ, ExecuTorch) | Gemma-3 (QAT, GGUF)
- Mobile test device: Android 11, 4 GB RAM, Helio G85
All configurations and checkpoints are open for verification.

## Datasets
 Public corpora used:
- Twitter Hate Speech (ICWSM 2017)
- OLID (NAACL 2019)
- Stormfront (ALW2 2018)
- Gab Hate Corpus (2022)
- HateXplain (AAAI 2021)
