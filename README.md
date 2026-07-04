# CodeAlpha_DiseasePrediction

**CodeAlpha Machine Learning Internship — Task 4**

## 🎯 Objective
Predict the possibility of disease from patient medical data using classification techniques.

## 🧠 Approach
- **Dataset 1: Breast Cancer Wisconsin** — real clinical dataset (30 features from cell nuclei measurements), loaded directly via `scikit-learn`.
- **Dataset 2: Heart Disease (UCI)** — attempts to fetch the real UCI dataset via OpenML; falls back to a realistic synthetic dataset with the same clinical feature schema (age, blood pressure, cholesterol, max heart rate, etc.) if offline.
- **Models compared**: Logistic Regression, SVM (RBF kernel), Random Forest, XGBoost (or Gradient Boosting if XGBoost isn't installed).
- **Evaluation**: Precision/Recall/F1 per class, ROC-AUC, and 5-fold cross-validated ROC-AUC for robustness.

## 📁 Files
| File | Description |
|---|---|
| `CodeAlpha_DiseasePrediction.ipynb` | Main Colab notebook — run top to bottom |
| `disease_prediction.py` | Standalone script version (VS Code / local run) |
| `requirements.txt` | Python dependencies |
| `roc_curves_breast_cancer.png`, `roc_curves_heart_disease.png` | ROC comparisons |
| `feature_importance_breast_cancer.png` | Top predictive clinical features |
| `breast_cancer_model_comparison.csv`, `heart_disease_model_comparison.csv` | Metric tables |

## ▶️ How to Run
**Option A — Google Colab (recommended)**
1. Upload `CodeAlpha_DiseasePrediction.ipynb` to [Google Colab](https://colab.research.google.com/).
2. Runtime → Run all.

**Option B — VS Code / Local**
```bash
pip install -r requirements.txt
python disease_prediction.py
```

## 📊 Results
On the Breast Cancer dataset, models reach **ROC-AUC ≈ 0.99** (this is a clean, well-separated real clinical dataset). The Heart Disease results vary depending on whether the real UCI dataset or the synthetic fallback loads — see the CSV outputs for your run's exact numbers.

## 👤 Author
Asad Hussain — B.E. Electrical Engineering, SEECS, NUST
[LinkedIn](https://linkedin.com/in/asad-hussain92)

*Submitted as part of the CodeAlpha Machine Learning Internship (#codealpha).*
