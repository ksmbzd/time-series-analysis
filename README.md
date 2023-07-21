# time-series-analysis

## Group Members
- Kassem Bou Zeid
- Abhinandan Aryal
- Younes Chaik

# Credit Card Fraud Detection Heuristics

This project aims to implement various heuristic methods for credit card fraud detection using a highly unbalanced dataset of credit card transactions by European cardholders in September 2013.
[Here](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud) is the link to the dataset "Credit Card Fraud Detection" on Kaggle.

## Data Overview

- The dataset consists of 284,807 transactions, out of which 492 (or 0.172%) are fraudulent. 
- The data is numerical and derived from a Principal Component Analysis (PCA) transformation. Original variables cannot be disclosed due to confidentiality reasons.
- The PCA transformed features are labeled as V1, V2, through V28.
- The response variable in this dataset is 'Class', with "1" indicating a fraudulent transaction and "0" indicating a legitimate one.
- Due to the class imbalance, it is recommended to use the Area under the Precision-Recall Curve (AUPRC) as an accuracy metric. 

## Exploratory Data Analysis

- Detailed visualizations and descriptions of transaction amounts for fraudulent vs. non-fraudulent transactions.
- Examination of the occurrence of fraudulent transactions over time.
- Analysis of individual 'V' features and their relation to fraudulence.
- Calculation of the Median Absolute Deviation (MAD) for the dataset.

## Anomaly Detection

Outliers, or anomalies, are identified using several methods, including:

1. **Median Absolute Deviation (MAD)**: It calculates the absolute deviation from the median for each point in the dataset, then identifies those points that deviate by more than a certain threshold as outliers.

2. **Z-score Method**: It transforms the data into a standard normal distribution, then identifies points that deviate from the mean by more than a certain number of standard deviations as outliers.

3. **Percentile Method**: It defines a lower and an upper threshold as percentiles of the data distribution and identifies points outside these thresholds as outliers.
4. Anomaly Detection Using Local Outlier Factor for Features V1 to V5.

All these methods are applied on each of the 'V' columns (V1 to V5) and the performance metrics (precision, recall, F1-score, and accuracy) are calculated. The results are visualized to better understand the anomaly detection performance of each method.

## Dependencies

- Python libraries: pandas, numpy, matplotlib, seaborn, sklearn, scipy

## References
1. Chandola, V., Banerjee, A., & Kumar, V. (2009). Anomaly detection: A survey. ACM Computing Surveys (CSUR), 41(3), 1-58.

2. Aggarwal, C. C. (2013). Outlier analysis. Springer Science & Business Media.
