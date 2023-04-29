# Census_Data
Which Feature indicates to higher Income level (>50k)
Conclusion : 
According to our data, if you want to make more than $50,000 annually, your age, hours worked
each week, and qualifications all matter. Contrarily, the importance of the working class is little. In general, if you
work hard enough, you will be given equal opportunities regardless of the type of job you do.

Data Quality:-
1. Missing values - In this data missing values are represented by ?. So, firstly we need to collect more data or
One approach to handle missing data is to impute the missing values with appropriate values beacuse it is
In [86]: sns.boxplot(x=df.hours_per_week,y=df.occupation, hue=df.income)
plt.legend(bbox_to_anchor=(1.02, 1),loc='upper left', title = 'Income Distribution');
categorical varaibles we can use mode method to fill the missing values(Baheti, P. (2023, February 2)).
2. Outliers - Using the boxplot we found the range of the numerical variables any values goes beyond that
should either be trimmed or we need to use models which are not affected by extreme values or replacing
extreme values with the next highest or lowest value in the distribution(Baheti, P. (2023, February 2)).
3. bias data - from the above analysis it is clear that dataset is biased in categories like sex, native_country and
race. so to fix this bias is to collect more data in order to balance out biases or we can use data
augmentation technique where we increase the diversity of the dataset by introducing new examples for
under represented groups.
4. Reducing the sub-categoiries in the variable to reduce the complexity of the data and to get better
visualisation.
5. Encoding categorical variables like '<=50k' & '>50k' to 0 & 1.
6. Data Completeness - if the dataset had more feature which could give better indication on income level
such as number of years of experience, health condition or Postal code and etc.
Model which could best fit this dataset:
Our dataset has target variable which means we can apply supervised machine learning model.
As our independent variable is not linear to the independent variable we can not apply linear regression model.
But, beacuse our Target variable contains only two categories like '<=50k' & '>50k' which makes it suitable for
logistic regression.
But before applying logistic regression, we need to first check for multicolinearity between the variables.
If there is any strong correlations between the variables our model will be greatly impacted.

Referencing:
A. (2021, July 4). Adult Income Dataset | From Scratch. Kaggle.
https://www.kaggle.com/code/aditimulye/adult-income-dataset-from-scratch
P. (2020, March 4). EDA + Logistic Regression + PCA. Kaggle. https://www.kaggle.com/code/prashant111/edalogistic-regression-pca
I. (2017, July 24). Income Prediction (84.369% Accuracy). Kaggle. https://www.kaggle.com/code/ipbyrne/incomeprediction-84-369-accuracy
A. (2023, February 13). Eda📊|Feature_Engineering|📈Logistic_Regression. Kaggle.
https://www.kaggle.com/code/abhi011097/eda-feature-engineering-logistic-regression#1-|-Preprocessing-Steps
Baheti, P. (2023, February 2). A Simple Guide to Data Preprocessing in Machine Learning. V7.
https://www.v7labs.com/blog/data-preprocessing-guide
