# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.Import pandas library to read csv or excel file.

2.Import LabelEncoder using sklearn.preprocessing library.

3.Transform the data's using LabelEncoder.

4.Import decision tree classifier from sklearn.tree library to predict 5.5.the values.

6.Find accuracy.

7.Predict the values.

8.End of the program.

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by:P.SYAM TEJ
RegisterNumber:212221240056 
*/
import matplotlib.pyplot as plt
import numpy as np
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
dt.predict([[0.5,0.8,9,260,6,0,1,2]])
```

## Output:

![5 1](https://user-images.githubusercontent.com/93427224/172995024-9cffbfe6-9d88-493c-a6a0-6656f524b2be.png)

![5 2](https://user-images.githubusercontent.com/93427224/172995034-9c30a695-e76a-42db-bcf0-79ee063a3070.png)

![5 3](https://user-images.githubusercontent.com/93427224/172995045-92167372-12a3-4cb2-8f6c-1fa6ef2e58ca.png)

![5 4](https://user-images.githubusercontent.com/93427224/172995080-18efabdf-ae6d-4c43-be49-e4ebcf628970.png)

![5 5](https://user-images.githubusercontent.com/93427224/172995100-8fc6717a-ad42-4fc0-a31c-f0511dfa4849.png)

![5 6](https://user-images.githubusercontent.com/93427224/172995121-9a59446b-6dec-4c3c-ab3b-853d0325147d.png)

![5 7](https://user-images.githubusercontent.com/93427224/172995135-d1ef6398-66cf-47aa-84f3-3e6283cf18d9.png)

![5 8](https://user-images.githubusercontent.com/93427224/172995157-294d0d4c-159f-4cfe-b9a2-b9c900d2218a.png)

![5 9](https://user-images.githubusercontent.com/93427224/172995173-5b179103-a2f3-4ecb-b81a-f5d8b914e14e.png)

## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
