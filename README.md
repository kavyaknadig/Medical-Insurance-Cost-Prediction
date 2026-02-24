# Medical-Insurance-Cost-Prediction
In this project, we predict medical insurance costs using ML models trained on demographic and lifestyle features such as age, BMI, smoking status, and plan type. We apply regression to estimate exact annual costs and classification to assign individuals to quartile-based cost categories.

1. Problem & Data 
Our task is to predict an individual’s annual medical insurance costs based on demographic and health-related features, helping insurance providers assess risk and set premiums accurately.

We have two ways to approach this. Regression, where we predict the exact amount of medical cost. Classification, where we predict which cost category the person belongs to. We evaluate regression using MAE and  R² Score, and for classification using Accuracy and Confusion Matrix.
 
We used the public Medical Insurance Cost Prediction dataset from Kaggle, which contains 100,000 rows and 54 numerical and categorical features covering demographic, medical, and financial information. The target variable, annual medical cost, is strongly right-skewed, with most individuals incurring low expenses and a small number showing very high costs. Because the dataset is cross-sectional rather than time-series, issues such as stationarity do not apply.

link to dataset : https://www.kaggle.com/datasets/mohankrishnathalla/medical-insurance-cost-prediction

2. Analysis & Discussion 
The different models identified some of the features to be highly influential in predicting the cost of insurance. For instance, lifestyle and demographic factors such as BMI, type of plan and network tire were strongly contributing to higher predicted medical costs. This agrees with real-life insurance logic that riskier profiles will have high premiums.
However, there are few limitations: If there were detailed medical history, it would greatly enhance our prediction accuracy, but was not included in this dataset.
Regarding the ROC curves, the issues stem from splitting the target into quartiles. Because the cost variable is right-skewed, classifiers struggle with the overlapping middle ranges but perform better at the extremes. Using fixed cost thresholds might improve interpretability, but would introduce severe class imbalance and likely reduce overall performance.
The results of the project make sense, but there is still room to improve both the fairness and accuracy by using more balanced real-world data.

3. Ethical & Legal Considerations
The dataset contains health-related information, so privacy and fairness must be considered. All data is fully anonymized with no personal identifiers, and its public, educational use is legally permitted. However, the models may still introduce bias so any real-world deployment would require fairness checks and responsible decision-making.
