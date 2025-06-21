# 📦 Demand Forecasting for Perishable Goods – ML Capstone Project

Forecasting demand for fresh foods to reduce waste, optimize inventory, and improve customer satisfaction.

---

## 📌 Project Overview

Fresh food demand is unpredictable due to:

- 🥬 Short shelf life  
- 🎨 Visual appeal  
- 🍂 Seasonal trends  
- 🚚 Specialized logistics  

Over 2.5 billion tons of food are wasted annually.  
This project builds an ML-based forecasting model to improve prediction accuracy and inventory efficiency.

---

## 🎯 Objectives

- Build a regression-based forecasting model  
- Understand which features impact units sold  
- Visualize trends and store/sku performance  
- Minimize error in predicting demand for perishables

---

## 📁 Dataset

- **Source**: Kaggle (External)  
- **Features**:  
  - `record_id`, `week`, `store_id`, `sku_id`, `total_price`, `base_price`, `is_featured_sku`, `is_display_sku`, `units_sold`

- Engineered:
  - `year`, `month`, `day`, `revenue` (from price × units_sold)

---

## 🧼 Data Cleaning

- Converted week column to datetime  
- Extracted day, month, year  
- Created revenue feature  
- Removed unused/duplicate features  
- One-hot encoded categorical features like `sku_id`, `store_id`

---

## 📊 Exploratory Analysis

- ✅ Strong correlation between `units_sold` and `revenue`  
- 🔍 Top-performing stores: 9845, 9823, 8869  
- 📉 Outliers observed in price and display features  
- 📦 August shows least sales; February peaks

---

## 🧠 ML Models Used

| Model               | MAE     | RMSE     | R² Score |
|--------------------|---------|----------|----------|
| Linear Regression   | 30.83   | —        | 0.22     |
| XGBoost Regressor   | 13.96   | 34.96    | —        |
| ✅ Random Forest     | **13.44** | —        | Best     |

- **Final Model**: Random Forest Regressor  
- Hyperparameter tuning via `GridSearchCV`  
- Most important features: `total_price`, `sku_id`, `store_id`, `month`, `day`

---

## 📈 Visualizations

- Correlation heatmap  
- Feature importance bar plot  
- Scatterplot of actual vs predicted units sold  
- Revenue trends over months and SKUs

---

## 🔍 Recommendations

- Add external factors (e.g., holidays, promotions)  
- Track economic & environmental indicators  
- Focus on SKUs: `219009`, `222087`, `216418`  
- Prioritize stores: `9845`, `8023`, `9112`  
- Periodically retrain the model with fresh data

---

## 🛠 Tech Stack

- Python  
- Pandas, NumPy  
- Scikit-learn, XGBoost  
- Matplotlib, Seaborn  
- Jupyter Notebook / Streamlit (optional UI)

---

## 🚀 Impact

By applying this model, grocers and retailers can:

- 📉 Reduce food waste  
- 📦 Optimize shelf space  
- 🧾 Improve operational efficiency  
- 🛍️ Enhance the customer shopping experience

---
## 👩‍💻 Author

**Swati Sharma**  
📫 [LinkedIn](https://www.linkedin.com/in/swati-sharma-17s50s01/)
📬 _Let’s connect if you’d like to collaborate on AI + Retail!_
