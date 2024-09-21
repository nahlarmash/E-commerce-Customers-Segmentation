<h1 align="center">
E-commerce-Customers-Segmentation-Project
<h1 align="center">

## Table of Contents
- [Overview](#Overview)
- [Dataset Overview](#Dataset-Overview)
- [Project Approach](#Project-Approach)
- [Model Approach](#Model-Approach)
- [Evaluation Metrics](#Evaluation-Metrics)
- [Key Findings](#Key-Findings)
- [Key Insights](#Key-Insights)



## Overview
The customer segmentation project utilizing unsupervised machine learning techniques to analyze customer demographics and transactional behavior. The project aims to group customers into segments that can be used to create targeted strategies, such as personalized coupon offerings.

## Dataset Overview
The dataset used in this project consists of several tables related to customer demographics and transactional history. The key tables are:
- **Customers:** Contains information about the customers, including their ID, join date, city, and gender.
- **Genders:** Stores the gender data.
- **Cities:** Holds information on the cities where customers are located.
- **Transactions:** Logs customer transactions, including transaction status, coupon usage, and the branches where transactions took place.
- **Branches:** Information on the branches related to the transactions.
- **Merchants:** Contains details about the merchants associated with the branches.

## Project Approach
- **Data Merging:** Various tables were merged to create a consolidated dataset for analysis.
- **Data Preprocessing:** Missing values were handled, and relevant features were engineered to be used in the clustering algorithm.
- **Clustering:** The k-means clustering algorithm was applied to group customers into different segments based on their coupon usage behavior.
- **Evaluation:** Silhouette score was used to evaluate the effectiveness of the clustering model.
- **Analysis of Segments:** Key insights from each customer segment were analyzed to propose marketing strategies.

## Model Approach
### K-Means Clustering
- **Feature Selection:** Coupon usage frequency, burned coupon count, gender, and city were used to cluster the customers.
- **Scaling:** Numerical features were scaled to ensure that no feature dominates the clustering process.
- **K-Means Algorithm:** The algorithm grouped the customers into three distinct clusters. The optimal number of clusters was determined using the elbow method.

## Evaluation Metrics:
**silhuette score**: This metric was used to evaluate the clustering performance. It measures how similar an object is to its own cluster compared to other clusters. The score is `0.4017` and suggests that the clusters are somewhat distinct, but there is still room for improvement. It indicates that the clustering is moderately effective but may require further tuning or exploration of other features or clustering methods to improve cluster separation.

## Key Findings:
1. **Cluster 0:**
- High coupon usage frequency and burned coupon count.
- Predominantly male from Port Said.
- Recommendation: Provide additional loyalty rewards or exclusive coupons.

2. **Cluster 1:**
- Low coupon usage frequency and burned coupon count.
- Predominantly male from Damanhur.
- Recommendation: Targeted promotional campaigns or re-engagement strategies.

3. **Cluster 2:**
- Moderate coupon usage frequency and burned coupon count.
- Predominantly female from Giza.
- Recommendation: Retention-focused offers such as time-limited discounts or combo offers.

## Key Insights:
The segmentation revealed valuable insights into customer behavior:
- **Cluster 0:** Represents loyal and engaged customers, who may benefit from enhanced loyalty programs.
- **Cluster 1:** Represents disengaged customers, suggesting the need for strategies to re-engage this segment.
- **Cluster 2:** Represents moderately engaged customers, where retention efforts could yield positive results.
