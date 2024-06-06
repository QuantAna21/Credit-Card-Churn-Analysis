# Credit Card Churn Analysis

### Table of Contents
1. [Executive Summary](#executive-summary)
2. [Objectives](#objectives)
3. [Dataset Description](#dataset-description)
4. [Tools Used](#tools-used)
5. [Data Analysis Approach](#data-analysis-approach)
6. [Recommendations](#recommendations)
7. [References](#references)

### Executive Summary
Credit card churn, which occurs when customers open accounts primarily to earn welcome bonuses, rewards, and benefits, is a significant concern for banks and financial institutions. The objective of this project is to analyze credit card churn patterns, identify the factors contributing to customer attrition, and provide actionable insights for developing effective customer retention strategies.

### Objectives
- Visualize Differences: Compare attributes of attrited and existing customers.
- Predict Attrition: Develop a predictive model for customer attrition based on customer attributes.
- Segment Customers: Segment customers using demographic, financial, and behavioral data.

### Dataset Description
- Observations: 10,000 customer profiles.
- Columns: 23 initial features.
- Response Variable: Attrition_Flag.
- Data Balance: Moderately imbalanced.
- Source: Kaggle Dataset.

### Tools Used
- Python (Jupyter Notebook)
- Python Libraries: NumPy, Pandas, Matplotlib, Seaborn, Scikit-learn, SciPy, Statsmodels, Imblearn.
- Excel (PivotChart)

### Data Analysis Approach
#### *Data Preparation Steps*
- Creation of Dummy Variables.
- Standardization.
- Feature Engineering.
- Reduction of irrelevant variables.
- Data Aggregation.

#### *Data Visualization*
- Utilized Python (Matplotlib and Seaborn) to create visual representations of key features and their relationships with customer churn.
- Used Excel to visualize customer cluster attributes.

![Number of Contacts and Total Transaction Amount by Card Category in the last 12 months](https://github.com/QuantAna21/Credit-Card-Churn-Analysis/assets/171746795/d7748ea9-644b-4020-8e77-a2aaf5de236d)


#### *Machine Learning Algorithms*
-	Applied logistic regression to predict customer attrition, using Synthetic Minority Over-sampling Technique for Nominal and Continuous variables to address class imbalance.
```Python
smotenc = SMOTENC([1,2,3,4,5,6,7,8,9,10,11,12,13], random_state = 1)
x_oversample, y_oversample = smotenc.fit_resample(x_train, y_train)
```
-	K-means Clustering: Segmented customers into distinct groups based on their demographic, financial, and behavioral attributes.
```Python
optimal_k_means(dropcol1, 10)
kmeans = KMeans(n_clusters = 3, random_state=1)
```
### Key Insights
#### *Visualizations*
- Overall customer churn rate is 16%.
- Attrited customers aged 20-29 have significantly higher total revolving balances.
- Most attrited and existing customers have incomes below $40K.
- Churn typically occurs after 3 months of inactivity.
- Attrited customers averaged 3 contacts with the bank.
- The majority of customers hold the “Blue” card category.

#### *Logistic Regression*
- Odds of churn increase with more inactive months and contacts with the bank.
- Odds of churn decrease with more products held and higher transaction amounts.

#### *Clustering*
Three distinct customer clusters identified. The third cluster has the highest churn rate, characterized by:
- Longest relationship with the bank.
- Highest average age and number of inactive months.
- Most interactions with the bank.
- Lowest average transaction amount and total revolving balance.
  
### Recommendations
Based on the insights derived from analyzing the data related to credit card churn, here are several recommendations that can help mitigate customer churn and enhance customer retention:
- Implement targeted engagement for young customers (20-29 age group) and for customers in the third cluster.
- Create tailored retention strategies for low-income customers.
- Implement proactive measures to prevent inactivity.
- Optimize the quality of customer interactions.
- Incentivize higher transaction volumes.

### References
1. [Kaggle](https://www.kaggle.com/datasets/sakshigoyal7/credit-card-customers)
2. [Stack Overflow](https://stackoverflow.com/)
3. [DataCamp](https://www.datacamp.com/)
4. [Forbes](https://www.forbes.com/advisor/credit-cards/what-is-credit-card-churning/)
5. [Image by Freepik](www.freepik.com)











