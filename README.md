# Cervical Cancer Risk Factor Analysis & Prediction with XGBoost

## 📌 Project Overview
This project focuses on **data cleaning, exploratory data analysis (EDA), feature preprocessing, and classification** of cervical cancer risk factors.  
Using the `risk_factors_cervical_cancer.csv` dataset, the pipeline cleans missing data, performs statistical analysis, visualizes correlations, and trains an **XGBoost Classifier** to predict the likelihood of a **positive biopsy** result.

---

## 📂 Dataset
The dataset contains multiple medical and behavioral risk factors for cervical cancer, including:
- Age, number of pregnancies, smoking history
- Sexually transmitted diseases (STDs)
- HPV infection status
- Cytology and Schiller test results  
- **Target Variable:** `Biopsy` (1 = positive, 0 = negative)

📄 **File:** `risk_factors_cervical_cancer.csv`  
🔗 **Source:** [UCI Machine Learning Repository – Cervical Cancer Risk Factors](https://archive.ics.uci.edu/ml/datasets/Cervical+cancer+%28Risk+Factors%29)

---

## ⚙️ Installation & Requirements
To run the project, ensure you have the following dependencies installed:

```bash
pip install numpy pandas seaborn matplotlib plotly jupyterthemes scikit-learn xgboost joblib
```

---

## 🛠 Workflow
### 1️⃣ **Data Loading & Inspection**
- Loaded dataset using `pandas`
- Checked data types, null values, and statistical summaries

### 2️⃣ **Data Cleaning**
- Replaced `?` with `NaN`
- Dropped columns with excessive missing values:
  - `STDs: Time since first diagnosis`
  - `STDs: Time since last diagnosis`
- Converted object columns to numeric
- Filled missing values with **column means**

### 3️⃣ **Exploratory Data Analysis (EDA)**
- Heatmaps for missing data & correlations
- Histograms for feature distribution
- Correlation matrix visualization

### 4️⃣ **Feature Selection & Scaling**
- Target variable: `Biopsy`
- Standardized features using `StandardScaler`

### 5️⃣ **Model Training**
- Split data into **train (80%)**, **test (10%)**, and **validation (10%)**
- Trained an **XGBoost Classifier** with:
  - `learning_rate = 0.1`
  - `max_depth = 50`
  - `n_estimators = 100`

### 6️⃣ **Model Evaluation**
- Accuracy on training & test sets
- **Classification Report** (Precision, Recall, F1-score)
- Confusion Matrix heatmap

### 7️⃣ **Model Saving**
- Saved trained model as `cervical_cancer_xgb_model.pkl` using `joblib`

---

## 📊 Results
Example performance metrics:
- **Training Accuracy:** ~XX%
- **Test Accuracy:** ~XX%
- **Precision / Recall / F1-score:** See classification report output

---

## 📸 Visualizations
- **Missing Data Heatmaps**
- **Correlation Matrix Heatmap**
- **Histograms** for all features
- **Confusion Matrix** for predictions

---

## ▶️ How to Run
1. Place `risk_factors_cervical_cancer.csv` in the project directory.
2. Run the Python script or Jupyter Notebook.
3. The cleaned dataset, visualizations, and trained model will be generated.
4. The trained model is saved as:
   ```
   cervical_cancer_xgb_model.pkl
   ```

---

## 📁 File Structure
```
├── risk_factors_cervical_cancer.csv    # Dataset
├── cervical_cancer_analysis.py         # Main script
├── cervical_cancer_xgb_model.pkl       # Saved model
└── README.md                           # Project documentation
```

---

## 📌 Future Improvements
- Hyperparameter tuning for better accuracy
- Feature importance visualization
- Integration with a web app for real-time predictions
- Cross-validation for robust performance estimation

---

## 📜 License
This project is for **educational and research purposes** only.  
Not intended for medical diagnosis.
