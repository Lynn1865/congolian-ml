# Optimizing Supply Chain Efficiency: Predicting Late Deliveries and Analyzing Performance Patterns

## Project Summary

This project analyzes shipment data from a fictional e-commerce company, **Congolian**, to identify causes of late deliveries and recommend optimization strategies. Using machine learning models and geospatial analysis, our team investigated 180,000+ shipment records to uncover performance inefficiencies and delivery risk patterns across regions.

**Team Members:**  
- Alex Cundall (Team Lead)  
- Isaac Doescher  
- Yaling Wang  
- Arjun Agrawal  

## Research Questions

1. **What are the most significant predictors of late delivery?**  
   → We identified top predictors using classification models (Random Forest, XGBoost, Logistic Regression).

2. **Which regions experience the highest late delivery rates?**  
   → Geospatial clustering and statistical tests (Chi-Square, Kruskal-Wallis) highlighted regional inefficiencies.

## Dataset

- Source: [Kaggle - DataCo Smart Supply Chain for Big Data Analysis](https://www.kaggle.com/datasets)  
- Size: 180,519 rows × 53 variables  
- Key columns used:
  - `late_delivery_risk` (target)
  - `shipping_mode`, `order_region`, `delivery_distance`, `delivery_delay`, etc.

## Methodology

- **Exploratory Data Analysis:** Visualizations, feature engineering (e.g., delivery distance & delay), outlier detection.
- **Predictive Modeling:** 
  - Models: Random Forest, XGBoost, Logistic Regression, KNN
  - Evaluation: Confusion matrix, F1-score, AUC/ROC, SHAP values
- **Clustering:** K-Means and Hierarchical Clustering for identifying underperforming stores.
- **Geospatial Analysis:** Heatmaps, store distribution maps, and delivery trend visualizations.
- **Statistical Testing:** Chi-Square, T-Test, Kruskal-Wallis to test regional performance differences.

## 🔑 Key Findings

- **Top Delay Predictors:** `days_for_shipment_scheduled`, `shipping_day_of_week`, `order_day_of_week`
- **Highest Risk Regions:** Central America and Western Europe
- **Best Model:** XGBoost (Accuracy: 97.5%)
- **Cluster Insights:**
  - Cluster 0: Slow shipping, high delay risk
  - Cluster 1: On-time, efficient operations
  - Cluster 2: Fast shipping but minor delays
- **Shipping Distance:** Found **not** to be a statistically significant predictor of delays.

## Visual Outputs

- Correlation matrices
- Feature importance rankings
- SHAP value plots
- Cluster scatterplots & boxplots
- Regional heatmaps
- Delivery time trend lines

## Ethical Considerations

- **Data Privacy:** Sensitive info was removed (emails, passwords).
- **Environmental Impact:** Highlighted how fast shipping increases emissions and costs.
- **Regulatory Compliance:** Recommends transparency and sustainability in logistics.

## Tools & Technologies

- Python (Pandas, NumPy, Scikit-learn, XGBoost, Matplotlib, Seaborn, Plotly)
- Tableau (for advanced visualizations)

## Files Included

- `notebooks/` - Jupyter notebooks for EDA, modeling, and clustering
- `Final.pdf` - Full project report
- `README.md` - This file
