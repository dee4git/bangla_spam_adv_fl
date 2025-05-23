# Bangla Email Spam Detection via Federated Learning

This repository contains the implementation and evaluation of a federated learning (FL) framework for spam-ham email classification in Bangla. The project addresses the scarcity of publicly available Bangla spam datasets and introduces methodological improvements for multilingual spam detection using Transformer-based architectures.

## 📌 Highlights

- ✅ Human-translated Bangla version of the Kaggle English spam dataset.
- ✅ Controlled non-IID data partitioning based on spam-ham skew.
- ✅ Evaluation of 11 BERT variants under standard FL setup.
- ✅ Enhanced FL framework using multilingual models (e.g., XLM-RoBERTa).
- ✅ Cross-validation using Bangla SMS spam dataset to assess generalizability.

## 📊 Dataset

The dataset consists of 5,726 Bangla email instances translated by expert linguists to preserve semantic fidelity.

| Label | Count  |
|-------|--------|
| Ham   | 4,358  |
| Spam  | 1,368  |
| **Total** | **5,726**  |

> For additional testing, a Bangla spam SMS dataset was used to evaluate model generalizability beyond the email domain.

## 🧠 Models Tested

- **Baseline FL**: Simple CNN, LSTM
- **Transformer Variants**: BERT, DistilBERT, RoBERTa, XLM-RoBERTa, etc.
- **Best Model**: XLM-RoBERTa selected for enhanced FL implementation.

## ⚙️ Federated Learning Setup

- FL Framework: PySyft / Flower / FedML *(depending on implementation)*
- Data Distribution: Non-IID splits simulating client-level spam skew
- Evaluation Metrics: Accuracy, Precision, Recall, F1-score

## 🧪 Reproducibility

### Requirements
```bash
pip install -r requirements.txt
