# 🧠 Fundus Image Classification using Self-Supervised Learning (SimSiam)

## 📌 Overview

This project presents a Self-Supervised Learning (SSL) approach for retinal fundus image classification.
It leverages **SimSiam** to learn feature representations without labels and applies a downstream classifier using a **frozen ResNet-18 encoder**.

The work focuses on handling:

* Limited labeled data
* Class imbalance in medical imaging

---

## 🚀 Methodology

### 🔹 Self-Supervised Learning (SSL)

* Framework: **SimSiam**
* Backbone: **ResNet-18**
* Objective: Learn meaningful visual representations without labels

### 🔹 Downstream Classification

* Frozen encoder (feature extractor)
* Linear classifier trained on labeled data

---

## 📂 Dataset

* Retinal Fundus Image Dataset (Kaggle)
* CSV-based annotations
* Training / Validation split

---

## ⚙️ Training Details

* Input Size: 224 × 224
* Optimizer: Adam
* Loss Function: CrossEntropyLoss
* Encoder: Frozen during classification

---

## 📊 Results

| Metric              | Value   |
| ------------------- | ------- |
| Training Accuracy   | ~88–89% |
| Validation Accuracy | ~77–80% |

### 📈 Training Progress (Sample)

Epoch [1/30]  → Acc: 80.68% | Val Acc: 77.34%
Epoch [10/30] → Acc: 87.40% | Val Acc: 79.22%
Epoch [30/30] → Acc: 87.76% | Val Acc: 77.81%

---

## 📊 Visualizations

(Add your screenshots in `/outputs` folder)

* Accuracy vs Epoch
* Loss vs Epoch
* ROC Curve
* Confusion Matrix
* t-SNE Embeddings

---

## 🧠 Key Insights

* SSL effectively learns robust features without requiring labels
* Frozen encoder generalizes well on medical datasets
* Stable validation accuracy (~78–80%) indicates good generalization

---

## 🛠️ How to Run

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the notebook:

```
notebooks/fundus_ssl_training.ipynb
```

---

## 🔮 Future Work

* Multi-label classification using full RFMiD annotations
* Fine-tuning encoder instead of freezing
* Exploring advanced SSL methods (VICReg, SwAV)

---

## 📜 License

This project is licensed under the **MIT License**.

---

## 👨‍💻 Author

**Mohan Panduri**
