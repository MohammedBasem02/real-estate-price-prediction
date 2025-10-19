<p align="center">
  <img src="https://github.com/MohammedBasem02/real-estate-price-prediction/assets/your-image-id" width="600">
</p>

# 🏠 Real Estate Price Prediction (Jordan)

---

# Real Estate Demand Prediction (Professional Edition)

**Author:** Mohammed Nasrallah  
**Email:** mohammednasrallah82@gmail.com  

---

## 1. Overview
This project builds a complete end-to-end machine learning pipeline to **predict real estate transaction amounts** using multiple datasets related to land, housing, and sector-level indicators.  
It is inspired by the "China Real Estate Demand Prediction" Kaggle competition.

The goal is to create a clean, interpretable, and professional pipeline ready for both educational and practical applications.

---

## 2. Key Features
- Organized pipeline with seven clear stages:
  1. **Setup & Data Loading** — Import and prepare all CSV files.
  2. **Cleaning & Standardization** — Normalize column names and handle missing values.
  3. **Merging Datasets** — Join multiple sources (land, housing, POI, etc.) into one dataframe.
  4. **Feature Engineering** — Extract time-based and categorical features.
  5. **Model Training** — LightGBM regression model with validation split.
  6. **Evaluation** — Compute MAE, RMSE, and MAPE metrics.
  7. **Submission Generation** — Create the final prediction file.

---

## 3. Data Sources
All datasets come from the Kaggle competition repository:
- `new_house_transactions.csv`
- `pre_owned_house_transactions.csv`
- `land_transactions.csv`
- `sector_POI.csv`
- `... and their _nearby versions`

Each dataset contains monthly data per sector between 2019 and 2023.

---

## 4. Model Details
The model used is **LightGBM Regressor**, chosen for its high accuracy and speed.

**Main hyperparameters:**
- `learning_rate = 0.05`
- `num_leaves = 31`
- `feature_fraction = 0.8`
- `bagging_fraction = 0.8`
- `bagging_freq = 5`
- `n_estimators = 1000`
- `objective = regression`

**Training strategy:**
- Time-based split (80% train, 20% validation)
- Early stopping to prevent overfitting

---

## 5. Performance
| Metric | Score |
|:--|--:|
| MAE  | ~1363.27 |
| RMSE | ~3864.57 |
| MAPE | ~0.136 |

These results demonstrate solid predictive performance on unseen months.

---

## 6. How to Run
1. Upload all competition CSV files to the `/content` directory (if using Google Colab).  
2. Open the notebook `real_estate_demand_prediction.ipynb`.  
3. Run all cells sequentially from top to bottom.  
4. The final submission file will be saved as:

