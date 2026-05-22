# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the standard libraries from python. 

2.Upload the dataset and check for any null values using .isnull() function.

3.Import LabelEncoder and encode the dataset. 

4.Import DecisionTreeRegressor from sklearn and apply to the model from the dataset. 

5.Predict the values of the arrays. 

6.Import metrics from sklearn and calculate the MSE and R2 of the model from the dataset. 

7.Predict the values of array 

8.Apply it to the new unknown values

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: GOPIKA S
RegisterNumber:212225230082
/*
import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
x=data[["Position","Level"]]
x.head()
y=data["Salary"]
y.head()
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
y_pred
from sklearn.metrics import r2_score
r2=r2_score(y_test,y_pred)
dt.predict([[5,6]])
*/
```

## Output:
<img width="1384" height="665" alt="Screenshot 2026-05-22 135121" src="https://github.com/user-attachments/assets/99ec344f-518f-4167-ae2b-e751a45589e9" />


<img width="1400" height="818" alt="Screenshot 2026-05-22 135212" src="https://github.com/user-attachments/assets/f34bb08c-62d4-445d-a41d-a0bedecc2348" />


<img width="1415" height="878" alt="Screenshot 2026-05-22 135405" src="https://github.com/user-attachments/assets/e59ac98b-2244-4b8c-9a32-4bfead1c5bb3" />


<img width="1507" height="411" alt="Screenshot 2026-05-22 135457" src="https://github.com/user-attachments/assets/d6727737-dc9c-48a4-894b-b862634018d7" />




## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
