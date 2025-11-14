# GODO-assignment

# Bitcoin Trader Sentiment Dashboard  
**AI-Powered Financial Sentiment Analysis on 2021 Bitcoin Tweets**

## Overview

This project **analyzes real trader sentiment on Bitcoin in 2021** using **9,508 real tweets** and **state-of-the-art NLP**.

We go beyond basic models:
- Fine-tune **FinBERT** (finance-specialized) and **RoBERTa-base**
- Run a **6-model hyperparameter search** (3 configs × 2 models)
- **Automatically select the best model** by **weighted F1 score**
- Deliver an **interactive Plotly dashboard** + **AI-generated insight**

---

## Key Results

| Metric | Value |
|-------|-------|
| **Best Model** | **RoBERTa (Aggressive Config)** |
| **F1 Score** | **0.8260** |
| **Accuracy** | **0.8232** |
| **Tweets Analyzed** | **9,508** |
| **Time Period** | **Jan 1 – Dec 31, 2021** |

> **Surprising result**: RoBERTa with **aggressive training** outperformed FinBERT!

---

## Hyperparameter Search (6 Models)

| Rank | Model + Config | F1 Score | Accuracy | LR | Batch | Epochs |
|------|----------------|----------|----------|----|-------|--------|
| 1 | **RoBERTa (Aggressive)** | **0.8260** | **0.8232** | 3.0e-5 | 32 | 3 |
| 2 | RoBERTa (Conservative) | 0.8204 | 0.8180 | 1.0e-5 | 16 | 5 |
| 3 | FinBERT (Conservative) | 0.8167 | 0.8137 | 1.0e-5 | 16 | 5 |
| 4 | FinBERT (Balanced) | 0.8128 | 0.8189 | 1.5e-5 | 32 | 4 |
| 5 | FinBERT (Aggressive) | 0.8097 | 0.8249 | 3.0e-5 | 32 | 3 |
| 6 | RoBERTa (Balanced) | 0.8058 | 0.8052 | 1.5e-5 | 32 | 4 |

> **Best model auto-selected and used in final analysis**

---

## Dashboard Preview



- **Left**: Sentiment % (Pie Chart)  
- **Right**: Daily Net Sentiment (Line Chart)  
  - Positive = +1, Negative = -1, Neutral = 0

---


## How to Run

1. Open in GODO-asignment.ipynb 
2. **Runtime → Change runtime type → GPU (T4) if available **
3. Click **"Run all"**
4. provide kaggle autentication json 
5. Done in **~15–20 minutes**

> No setup. No cost. No API keys.

---

## Tech Stack

| Component | Tool |
|---------|------|
| Language | Python |
| NLP Framework | Hugging Face Transformers |
| Data | Kaggle (CC0) |
| Training | GPU (Colab T4) |
| Visualization | Plotly |


---

