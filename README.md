# Employee Promotion Prediction
This project focuses on predicting whether an employee will be promoted based on various personal, professional, and performance-related attributes. The goal is to analyse factors that influence promotions and build machine learning models which can predict promotion of employees. The steps involved include data cleaning, exploratory data analysis, testing of independence of attributes, feature engineering , machine learning modeling and evaluating model performance.

## Dataset Description
The link of the Kaggle dataset utilised for the project is - https://www.kaggle.com/datasets/muhammadimran112233/employees-evaluation-for-promotion/data.
The description of the columns is as follows:
1. employee_id: Unique ID for the employee
2. department: Department of employee
3. region: Region of employment 
4. education: Education Level
5. gender: Gender of Employee
6. recruitment_channel: Channel of recruitment for employee
7. no_ of_ trainings: no of other trainings completed in the previous year on soft skills, technical skills, etc.
8. age: Age of Employee
9. previous_ year_ rating: Employee Rating for the previous year
10. length_ of_ service: Length of service in years
11. awards_ won: if awards won during the previous year then 1 else 0
12. avg_ training_ score: Average score in current training evaluations
13. is_promoted (Target): Recommended for promotion or not

The dataset contains 54,808 records.

## Data Preprocessing
Missing values in education,previous year rating and average training score columns were handled using appropriate methods. Outliers were detected in age and length columns using boxplots and were treated using suitable approaches.

## Testing of independence of attributes
The chi-square test of independence of attributes reveals that all the feature columns are independent of each other. Therefore, all the features can be included in the model.

## Encoding of categorical features
Gender and Region were encoded using Label encoding while Department, Education, Recruitment channel and Previous year rating columns were encoded using One-Hot encoding.

## Machine Learning models
Models based on Decision Tree, Random Forest and XGBoost were trained. XGBoost achieved the best overall performance among the models.

## Handling class imbalance
As majority of the records belonged to not promoted class, SMOTE (Synthetic Minority Oversampling Technique) was applied to balance the classes and to create a balanced dataset that helps improve model performance and generalization.

Post the usage of SMOTE, the models were evaluated on the basis of Recall and F-score and the XGBoost model performed best overall.







