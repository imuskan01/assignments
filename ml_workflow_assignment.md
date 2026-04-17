ML Workflow Assignment
Task 1: Identifying Label and Data Leakage

Label Column:
repeat_purchase_flag

This column acts as the target variable because it clearly represents the outcome we are trying to predict — whether a customer makes a repeat purchase within 30 days. Since the entire goal of the model is to understand and predict customer behavior, this column naturally becomes the label.

Column Causing Data Leakage:
discount_used_on_repeat_order

This column can lead to data leakage because it contains information about the discount applied on a repeat purchase, which is only known after the repeat purchase has already occurred. Including such a feature during training would give the model access to future information, making its predictions unrealistically accurate and unreliable in real-world scenarios.

Task 2: Important Steps Before Model Training

Before directly jumping into training a gradient boosting model, it is important to follow a structured machine learning workflow:

1. Exploratory Data Analysis (EDA):

EDA is a crucial first step as it helps in understanding the dataset in depth. By analyzing distributions, checking for missing values, and identifying patterns or anomalies, we gain insights into how different features relate to each other and to the target variable. Skipping this step can lead to poor model choices and overlooked data issues.

2. Data Preprocessing and Feature Engineering:

Raw data is rarely clean or ready for modeling. This step involves handling missing values, correcting inconsistencies, scaling numerical features, and transforming variables if needed. Proper preprocessing ensures that the data fed into the model is meaningful and structured, which directly improves model performance and stability.