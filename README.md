# 🏠 Housing Price Data Analysis
### Comprehensive Exploratory Data Analysis and Machine Learning with Model Interpretability

**Author:** Muhammad Osama  
**Student Number:** 1288056  
**Course:** Data Visualization for Machine Learning  

---

## 📁 Project Structure

```
Housing_Price_Analysis/
│
├── 📄 README.md                        <- Project overview and documentation  
├── 📊 Housing_Price_Data.csv           <- Original dataset (Kaggle)  
│
├── 📓 Housing_Price_Analysis.ipynb     <- Main Jupyter Notebook (EDA + ML + SHAP + LIME)  
│
├── 📈 Housing_Price_Dashboard.py       <- Optional Dash app for interactive SHAP visualization  
│
├── 📘 Project_Report.pdf               <- Final report summarizing workflow, results, and insights  
├── 🖼️ Project_Presentation.pptx        <- Summary slides for academic submission  
│
├── 🧩 requirements.txt                 <- Python dependencies  
│
└── 📂 assets/                          <- Saved charts or exported SHAP/LIME visuals  
    ├── shap_summary.png  
    ├── feature_importance.png  
    └── correlation_heatmap.png
```

---

## 📘 Overview
This project implements a **complete machine learning workflow** for predicting housing prices using a dataset from Kaggle.  
It includes **EDA**, **feature engineering**, and **model interpretability** using **SHAP** and **LIME** to explain predictions transparently.  

---

## 🧩 Dataset
- **Source:** [Kaggle – Housing Price Dataset](https://www.kaggle.com/datasets/saurabhbadole/housing-price-data)  
- **Records:** 545  
- **Features:** 13  
- **Target:** `price`  
- **Feature Types:**  
  - **Numeric:** `area`, `bedrooms`, `bathrooms`, `stories`, `parking`  
  - **Binary:** `mainroad`, `guestroom`, `basement`, `airconditioning`, `prefarea`  
  - **Categorical:** `furnishingstatus` (unfurnished, semi-furnished, furnished)

---

## 🤖 Model Development
| Model | Type | Highlights |
|--------|------|------------|
| Linear Regression | Baseline | Fast, interpretable benchmark |
| Ridge Regression | Regularized | Handles multicollinearity |
| Random Forest | Ensemble | Handles non-linearity and interactions |
| Gradient Boosting | Ensemble | Best accuracy and generalization |

✅ **Gradient Boosting Regressor** achieved the best overall test performance.

---

## 🧠 Model Interpretability

### 🟦 SHAP (SHapley Additive exPlanations)
- Explains **global** and **local** feature impacts  
- Visualized with summary, bar, and waterfall plots  
- Interactive **Plotly + Dash Dashboard** for:  
  - Dynamic feature importance  
  - Dependence and interaction plots  
  - Instance-level interpretability  

### 🟩 LIME (Local Interpretable Model-agnostic Explanations)
- Explains **individual predictions**  
- Shows how each feature affects model output locally  
- Aggregated feature influence comparison  

### 🟧 SHAP vs LIME Comparison
- High correlation (~0.7) between global and local importance  
- Top features: `area`, `bathrooms`, `prefarea`, `furnishingstatus`, `parking`

---

## 📈 Key Insights
- **Area** is the strongest predictor of housing prices  
- **Bathrooms and bedrooms** have high positive impact  
- **Furnished homes** and **parking** increase property value  
- SHAP & LIME confirm model transparency  

---

## 🧰 Tech Stack
**Languages:** Python  
**Libraries:**  
`pandas`, `numpy`, `matplotlib`, `seaborn`, `plotly`, `scikit-learn`, `shap`, `lime`, `dash`, `dash-bootstrap-components`  

---

## 🚀 Run Instructions
### 1️⃣ Install dependencies
```bash
pip install -r requirements.txt
```
### 2️⃣ Run Jupyter Notebook
```bash
jupyter notebook Housing_Price_Analysis.ipynb
```
### 3️⃣ Launch Dashboard
```bash
python Housing_Price_Dashboard.py
```
or within the notebook:
```python
shap_dashboard_app.run_server(debug=True, port=8050)
```

---

## 📜 License
Dataset available under **CC BY-NC-SA 4.0 International License**.  
© 2025 Muhammad Osama — Academic and educational use only.
