<div align="center">

<img src="images/banner.png" alt="ViCM Banner" width="100%"/>

# 🇻🇳 ViCM: Vietnamese Code-Mixed Dataset

**The first publicly available dataset for code-mixed Vietnamese hate speech detection**

[![Paper](https://img.shields.io/badge/📄_Paper-Springer_Nature-blue?style=for-the-badge)](https://link.springer.com/article/10.1007/s13042-025-02904-6)
[![License](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey?style=for-the-badge)](https://creativecommons.org/licenses/by/4.0/)
[![Dataset](https://img.shields.io/badge/Dataset-5415_Samples-green?style=for-the-badge)](https://github.com/tiennho2608/ViCM)
[![Journal](https://img.shields.io/badge/Journal-IJMLC_2026-orange?style=for-the-badge)](https://link.springer.com/journal/13042)

</div>

---

## 📌 Overview

**ViCM** (*Vietnamese Code-Mixed*) is the **first human-annotated dataset** for code-mixed hate speech detection in Vietnamese social media. As Vietnamese users increasingly blend Vietnamese with English and other languages in online comments, existing NLP resources have failed to capture this linguistic reality — until now.

> ⚠️ **Disclaimer:** This dataset contains real social media comments that may be considered offensive, hateful, or abusive. It is intended strictly for research purposes.

---

## 🔬 Research Context

This dataset was created as part of the paper:

> **"An Effective Convolutional Cross-Lingual Language Model for Vietnamese Online Social Media Mining"**
> Tien Minh Nguyen, Tue Minh Nguyen, Tin Van Huynh, Kiet Van Nguyen
> *International Journal of Machine Learning and Cybernetics*, Volume 17, Article 69, 2026
> 🔗 https://doi.org/10.1007/s13042-025-02904-6

Our work proposes a **cross-lingual language model with 1D-CNN layers** and a **custom loss function** to tackle class imbalance — achieving state-of-the-art performance on **VSMEC**, **VSFC**, and **ViSpam** benchmarks.

---

## 💡 Why ViCM?

| Challenge | Our Solution |
|---|---|
| No existing code-mixed Vietnamese dataset | ✅ First dataset of its kind (~5,415 samples) |
| Class imbalance in hate speech data | ✅ Custom focal loss function |
| Poor feature extraction from short comments | ✅ 1D-CNN layers for local feature capture |
| Cross-lingual complexity | ✅ XLM-R backbone with multilingual pretraining |

---

## 📂 Dataset Files

### 📁 Repository Structure

```
ViCM/
├── data/
│   ├── train.csv        ← Training split
│   ├── dev.csv          ← Validation split
│   └── test.csv         ← Test split
├── images/              ← (your preview images go here)
└── README.md
```

---

### 🗂️ `train.csv` — Training Split

> Replace the line below with your screenshot of train.csv

![train.csv preview](images/train_preview.png)

The main training data used to fit classification models. Contains the largest portion of labeled code-mixed Vietnamese social media comments.

---

### 🗂️ `dev.csv` — Validation Split

> Replace the line below with your screenshot of dev.csv

![dev.csv preview](images/dev_preview.png)

Used during training for hyperparameter tuning and early stopping. Helps prevent overfitting on the training data.

---

### 🗂️ `test.csv` — Test Split

> Replace the line below with your screenshot of test.csv

![test.csv preview](images/test_preview.png)

The held-out evaluation set. Used exclusively for final benchmarking — never seen by the model during training.

---

## 📊 Dataset Statistics

| Split | # Samples | Hate Speech | Non-Hate |
|-------|-----------|-------------|----------|
| Train | —         | —           | —        |
| Dev   | —         | —           | —        |
| Test  | —         | —           | —        |
| **Total** | **~5,415** | —       | —        |

> 📝 Fill in exact label distribution from your data.

---

## 🧾 Data Format

Each `.csv` file contains the following columns:

| Column | Type     | Description |
|--------|----------|-------------|
| `id`   | `int`    | Unique comment identifier |
| `text` | `string` | Raw social media comment (code-mixed Vietnamese) |
| `label`| `int`    | `0` = Non-hate, `1` = Hate speech |

> 📝 Adjust column names to match your actual schema if different.

**Example:**

| id | text | label |
|----|------|-------|
| 1  | "mày nói vậy là sai lắm lol" | 0 |
| 2  | "đồ ngu, get out of here"     | 1 |

---

## 🚀 Quick Start

```python
import pandas as pd

# Load splits
train_df = pd.read_csv("data/train.csv")
dev_df   = pd.read_csv("data/dev.csv")
test_df  = pd.read_csv("data/test.csv")

print(f"Train: {len(train_df)} samples")
print(f"Dev:   {len(dev_df)} samples")
print(f"Test:  {len(test_df)} samples")

# Preview
print(train_df.head())
```

---

## 📝 Citation

If you use the **ViCM** dataset in your research, please cite our paper:

```bibtex
@article{nguyen2026vicm,
  title     = {An effective convolutional cross-lingual language model for Vietnamese online social media mining},
  author    = {Nguyen, Tien Minh and Nguyen, Tue Minh and Huynh, Tin Van and Nguyen, Kiet Van},
  journal   = {International Journal of Machine Learning and Cybernetics},
  volume    = {17},
  pages     = {69},
  year      = {2026},
  publisher = {Springer},
  doi       = {10.1007/s13042-025-02904-6},
  url       = {https://link.springer.com/article/10.1007/s13042-025-02904-6}
}
```

---

## 📜 License

This dataset is released under the
[Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/) license.

You are free to share and adapt the material for any purpose, provided appropriate credit is given.

---

## 👥 Authors

| Name | Affiliation |
|------|-------------|
| **Tien Minh Nguyen** | University of Information Technology, VNUHCM |
| **Tue Minh Nguyen**  | University of Information Technology, VNUHCM |
| **Tin Van Huynh**    | University of Information Technology, VNUHCM |
| **Kiet Van Nguyen**  | University of Information Technology, VNUHCM |

📧 Contact: tiennm26082002@gmail.com

---

## 🙏 Acknowledgements

This research was supported by **The VNUHCM-University of Information Technology's Scientific Research Support Fund**.

---

<div align="center">
  <sub>Made with ❤️ for the Vietnamese NLP community</sub>
</div>
