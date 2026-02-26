# 📘 Feature Engineering Playbook

A comprehensive, interview-ready reference notebook covering all major feature engineering techniques used in real-world Machine Learning pipelines.

---

## 📌 About

This repository is a **single, detailed playbook** that documents every important feature engineering technique with:
- ✅ What the technique does
- ✅ When to use it (and when NOT to)
- ✅ Why we use it
- ✅ Fully commented code implementation
- ✅ Interview tips and warnings

---

## 📂 Notebook

| Notebook | Description |
|---|---|
| `Feature_Engineering_Playbook_Detailed.ipynb` | End-to-end feature engineering reference covering Encoding, Transformations, Scaling, Cyclical Encoding, and Feature Interaction techniques |

---

## 🧪 Techniques Covered

### 🔹 Encoding Techniques

| Technique | Use When | Avoid When |
|---|---|---|
| **One-Hot Encoding** | Nominal categorical data, small number of categories | High-cardinality features (1000+ categories) |
| **Ordinal Encoding** | Ordered categories (Low < Medium < High) | Nominal (unordered) categories |
| **Frequency Encoding** | High-cardinality features (City, Pincode), large datasets | When target relationship needs to be preserved |

### 🔹 Transformations

| Technique | Use When |
|---|---|
| **Log Transformation** | Right-skewed data (Income, Population); use `log1p` when zeros exist |
| **Power Transformation (Yeo-Johnson)** | Highly skewed data, linear regression assumptions required |
| **Polynomial Features** | When feature-target relationship is curved/nonlinear |

### 🔹 Scaling Techniques

| Technique | Use When |
|---|---|
| **Standard Scaling** | Logistic Regression, Neural Networks, SVM |
| **MinMax Scaling** | Neural Networks, Image data |
| **Robust Scaling** | Dataset has many outliers |

### 🔹 Other Techniques

- **Cyclical Encoding** — Sine/cosine encoding for repeating cycles like day of week, month, hour, angles
- **Feature Interaction & Ratios** — Creating new features from combinations (e.g. `area_per_room = area / rooms`)

---

## 🎯 Interview Quick Reference

- Always **split data before fitting** any transformer — prevents data leakage
- Use **One-Hot** for nominal, **Ordinal** for ordered categories
- Use **Frequency / Target Encoding** for high-cardinality features
- **Scaling is required** for gradient-based models (Logistic Regression, SVM, Neural Networks)
- **Tree-based models** (Random Forest, XGBoost) are less sensitive to scaling
- Feature engineering often has **more impact than model selection**

---

## 🚀 Getting Started

### Prerequisites
```bash
pip install pandas numpy scikit-learn
```

### Clone the Repo
```bash
git clone https://github.com/sachinmasti/feature-engineering-playbook.git
cd feature-engineering-playbook
```

### Run Notebook
Open `Feature_Engineering_Playbook_Detailed.ipynb` in **Jupyter Notebook** or **VS Code**.

---

## 📊 Sample Datasets Used

```python
# Encoding
df = pd.DataFrame({'color': ['Red', 'Blue', 'Green', 'Blue']})
df = pd.DataFrame({'education': ['Low', 'Medium', 'High']})
df = pd.DataFrame({'city': ['Mumbai', 'Delhi', 'Mumbai', 'Pune']})

# Transformations
df = pd.DataFrame({'income': [1000, 5000, 10000, 50000]})

# Feature Interaction
df = pd.DataFrame({'area': [1000, 1500, 2000], 'rooms': [2, 3, 4]})
```

---

## 🤝 Contributing
Feel free to open a PR if you want to add more techniques or improve existing implementations!

---

## 📬 Connect
- GitHub: [@sachinmasti](https://github.com/sachinmasti)

---

⭐ **If this repo helped you, please give it a star!**
