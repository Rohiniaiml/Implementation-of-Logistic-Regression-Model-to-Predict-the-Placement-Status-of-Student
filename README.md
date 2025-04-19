# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
 1.Import the required packages and print the present data.
 
 2.Print the placement data and salary data. 
 
 3.Find the null and duplicate values.
 
 4.Using logistic regression find the predicted values of accuracy , confusion matrices. 
 
 5.Display the results.

## Program:
```
/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by: Rohini R 
RegisterNumber:212224240138

import pandas as pd
data=pd.read_csv(r"C:\Users\admin\Desktop\Placement_Data.csv")
data.head()
data1=data.copy()
data1=data1.drop(["sl_no","salary"],axis=1)
data1.head()
data1.isnull().sum()
data1.duplicated().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data1["gender"]=le.fit_transform(data1["gender"])
data1["ssc_b"]=le.fit_transform(data1["ssc_b"])
data1["hsc_b"]=le.fit_transform(data1["hsc_b"])
data1["hsc_s"]=le.fit_transform(data1["hsc_s"])
data1["degree_t"]=le.fit_transform(data1["degree_t"])
data1["workex"]=le.fit_transform(data1["workex"])
data1["specialisation"]=le.fit_transform(data1["specialisation"])
data1["status"]=le.fit_transform(data1["status"])
data1
x=data1.iloc[:,:-1]
x
y=data1["status"]
y
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
from sklearn.linear_model import LogisticRegression
lr=LogisticRegression(solver="liblinear")
lr.fit(x_train,y_train)
y_pred=lr.predict(x_test)
print(y_pred)
print()
from sklearn.metrics import accuracy_score
accuracy=accuracy_score(y_test,y_pred)
print(accuracy)
print()
from sklearn.metrics import confusion_matrix
confusion=confusion_matrix(y_test,y_pred)
print(confusion)
print()
from sklearn.metrics import classification_report
classification_report1=classification_report(y_test,y_pred)
print(classification_report1)
lr.predict([[1,80,1,90,1,1,90,1,0,85,1,85]])


```

## Output:
![image](https://github.com/user-attachments/assets/038f6d08-f57f-44fa-a4fc-0664ab15dde6)
![image](https://github.com/user-attachments/assets/80e0086f-101d-43fa-8d06-6e71f203860e)
![image](https://github.com/user-attachments/assets/c864b611-58b7-4b5c-a04a-03a732db3469)
![image](https://github.com/user-attachments/assets/8afe59a9-fd4c-44bc-8054-a3afef2284d6)
![image](https://github.com/user-attachments/assets/acbba675-b25a-4d63-bee1-acbc703a5a5a)
![image](https://github.com/user-attachments/assets/0c39e3bb-906c-47e9-8065-f3a9a3fb0de5)
![image](https://github.com/user-attachments/assets/0068a21b-d6c2-4e38-918f-95af5e326fd0)
![image](https://github.com/user-attachments/assets/3bb4c25c-4677-4a46-b53f-baa6b2c165a2)




## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
