# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the libraries and read the data frame using pandas.

2. Calculate the null values from dataframe and apply label encoder.

3. Apply decision tree classifier on the dataframe.

4. obtain the value of accuracy and data prediction.
## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: NAVEEN KUMAR B
RegisterNumber:  212222230091


import pandas as pd
data=pd.read_csv("Employee.csv")
data.head()
data.info()
data.isnull().sum()
data["left"].value_counts()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["salary"]=le.fit_transform(data["salary"])
data.head()
x=data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]
x.head()
y=data["left"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
dt.predict([[0.5,0.8,9,260,6,0,1,2]])
*/
```

## Output:
Initial dataset:
![image](https://github.com/mrnaviz/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/123350791/7de1f10c-b615-44c7-a365-db2bd961741c)

Data info:
![image](https://github.com/mrnaviz/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/123350791/4b0d419a-9dd8-42e8-be0b-e4cf1b6ff8c0)

Null values:
![image](https://github.com/mrnaviz/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/123350791/e623d1ae-7832-439d-b9a7-e75944ec2f1c)

Assignment of x and y values:
![image](https://github.com/mrnaviz/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/123350791/c54ee7ec-cdfb-44f2-9caf-1a7b4ae8012a)

![image](https://github.com/mrnaviz/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/123350791/a6308d1e-d81c-432e-b542-ff58bd0cccb5)

Converting string literals to numerical values using label encoder:
![image](https://github.com/mrnaviz/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/123350791/a37a95f1-714c-4979-950f-fe84cca75e84)

Accuracy:
![image](https://github.com/mrnaviz/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/123350791/0b6c0924-2e5c-41c3-a711-c3aa0f55f60c)

Prediction:
![image](https://github.com/mrnaviz/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/123350791/44f53c9b-1cb5-4609-b6d2-adf6cfee9b5e)




## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
