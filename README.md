# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import pandas

2.Import Decision tree classifier

3.Fit the data in the model

4.Find the accuracy score

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: GOKUL S
RegisterNumber: 212224230075
*/
```
```
import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()
data.info()
data.isnull().sum()
```
```
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
```
```
x=data[["Position","Level"]]
x.head()
y=data["Salary"]
y.head()
```
```
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
```
```
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
y_pred
from sklearn.metrics import r2_score
r2=r2_score(y_test,y_pred)
```

## Output:
<img width="445" height="326" alt="image" src="https://github.com/user-attachments/assets/8b9bc6c5-cd9d-4859-ad79-0edbaceb5012" />
<img width="318" height="211" alt="image" src="https://github.com/user-attachments/assets/a7471bbd-6f26-4231-bdc4-b8c566621d50" />
<img width="547" height="244" alt="image" src="https://github.com/user-attachments/assets/29f6b018-eca9-4585-9d15-4cf8df48ebc6" />
<img width="318" height="47" alt="image" src="https://github.com/user-attachments/assets/87745e23-6157-4c29-811a-98cccd759559" />
<img width="1383" height="73" alt="image" src="https://github.com/user-attachments/assets/7b8c3a53-4c3d-481a-bd52-10975553706c" />



## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
