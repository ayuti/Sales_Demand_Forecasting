# E-commerce Sales & Demand Forecasting 📈

A robust time-series forecasting solution designed to predict daily sales and category-level demand for an e-commerce platform. This project leverages statistical models and machine learning to optimize inventory management and operational efficiency.

## 📌 Project Overview
Accurate forecasting is the backbone of supply chain optimization. This project aims to:
*   **Predict daily sales** at the platform level.
*   **Forecast daily demand** across diverse product categories.

By utilizing the **Brazilian E-commerce Public Dataset (Olist)**, this solution provides actionable insights to reduce stockouts and minimize operational overhead.

---

## 💼 Business Impact
*   **Inventory Optimization:** Maintain lean stock levels while avoiding under-stocking.
*   **Operational Efficiency:** Lower storage and shipping costs by aligning logistics with demand.
*   **Marketing Insights:** Quantify the uplift from promotional campaigns and holiday seasons.
*   **Customer Satisfaction:** Boost CSAT scores by ensuring product availability and timely delivery.

### Key Metrics
| Metric | Purpose |
| :--- | :--- |
| **Inventory Turnover Rate** | Measure how quickly stock is sold and replaced. |
| **Stockout Rate** | Minimize the frequency of unavailable items. |
| **Operational Costs** | Control expenditures related to storage and handling. |
| **CSAT** | Ensure customer loyalty through reliable fulfillment. |

---

## 🛠️ Methodology & Technical Stack

### Data Preprocessing
*   **Cleaning:** Filtered for `delivered` status; handled duplicates and missing values.
*   **Integration:** Merged datasets spanning orders, products, and category translations.
*   **Feature Engineering:** 
    *   Temporal features (Day of week, month, year).
    *   Lag features & Rolling Statistics (Moving averages).
    *   Exogenous variables (Holidays/special events).

### Modeling Approach
1.  **SARIMAX:** A statistical seasonal ARIMA model incorporating exogenous holiday data.
2.  **XGBoost:** A gradient-boosted decision tree approach utilized for both platform-wide sales and category-specific demand.
3.  **Global Demand Model:** A unified XGBoost model trained across all categories to simplify deployment and capture cross-category patterns.

---

## 📊 Results & Insights

The machine learning approach significantly outperformed traditional statistical modeling for this dataset.

| Task | Model | RMSE (Lower is better) |
| :--- | :--- | :--- |
| **Daily Sales** | SARIMAX | ~14,000 |
| **Daily Sales** | **XGBoost** | **~3,000** |
| **Category Demand** | Global XGBoost | High accuracy across major categories |

> **Key Takeaway:** While SARIMAX captures broad seasonality, **XGBoost** is far more effective at handling complex, non-linear patterns and the high granularity of daily e-commerce fluctuations.

---

## 📂 Dataset
The project uses the [Brazilian E-commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) available on Kaggle. It contains 100k orders from 2016 to 2018.

---
