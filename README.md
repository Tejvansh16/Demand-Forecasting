# 🛒 Demand Forecasting for a Retail Store  

Predicting product demand using Machine Learning to optimize inventory management and reduce stock-outs.  

---

## 📌 Project Overview  
This project aims to develop a demand forecasting model for a retail store using historical sales data. By applying machine learning techniques, the model provides accurate predictions of product demand, helping in efficient inventory management and better decision-making.  

### ✅ **Key Objectives:**  
- Predict the number of units sold using historical data.  
- Improve forecasting accuracy using advanced machine learning algorithms.  
- Optimize inventory levels and reduce operational costs.  

---

## 🗂 Dataset  
- **Link:** [Store-level transactional data](https://www.kaggle.com/datasets/aswathrao/demand-forecasting?select=train_0irEZ2H.csv)  
- **Size:** 150,150 records  
- **Features:**  
  - `store_id` - Unique ID of the store  
  - `sku_id` - Product ID  
  - `total_price` - Selling price  
  - `base_price` - Original product price  
  - `is_featured_sku` - Whether the product was featured  
  - `is_display_sku` - Whether the product was on display  
  - `units_sold` - Target variable  

---

## 🛠 Tech Stack  
- **Programming Language:** Python  
- **Libraries:** Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn  
- **Algorithm:** Random Forest Regressor, XGBoost  
- **Visualization Tools:** Matplotlib, Seaborn  
- **Hyperparameter Tuning:** Grid Search with Cross-Validation  

---

## 🚀 Approach  

1. **Data Preprocessing:**  
    - Handled missing values.  
    - Removed outliers using the 99th percentile threshold.  
    - Created additional time-based features (`day`, `month`, `year`).  
    - Applied one-hot encoding to categorical data.  

2. **Feature Engineering:**  
    - Generated price-related features like `price_ratio` (`total_price / base_price`).  
    - Created lag features for better demand prediction.  
    - Incorporated cyclic encoding for temporal features.  

3. **Model Building:**  
    - Implemented a baseline **Random Forest Regressor** achieving an initial R² score of **0.77**.  
    - Improved the accuracy using hyperparameter tuning, resulting in a final R² score of **0.83**.  

4. **Hyperparameter Tuning:**  
    - Applied **Grid Search** with cross-validation to optimize model parameters.  
    - **Best Parameters:**  
      - `min_samples_split`: **3**  
      - `n_estimators`: **20**  

5. **Evaluation:**  
    - Evaluated using **Root Mean Squared Error (RMSE)** and **R² Score**.  
    - **Final Results:**  
      - **R² Score:** 0.83  
      - **RMSE:** 17.77  

---

## 📊 Results and Visualizations  

- **Feature Importance:** Visualized using bar charts to identify key contributors to sales predictions.  
- **Prediction vs Actual Plot:** Scatter plot comparing actual and predicted sales.  
- **Error Distribution:** Analyzed the error distribution using histograms for further refinement.  

---
