# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
```
1.Import the libraries and read the data frame using pandas.

2.Calculate the null values present in the dataset and apply label encoder.

3.Determine test and training data set and apply decison tree regression in dataset.

4.calculate Mean square error,data prediction and r2.
``` 

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: gokul prakash
RegisterNumber: 212223240041
*/
import pandas as pd
data=pd.read_csv("C:\\Users\\admin\\Downloads\\Salary (1).csv")
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
r2
dt.predict([[5,6]])
```

## Output:
![image](https://github.com/user-attachments/assets/3ec2b3b4-cba2-4faf-ae1b-75383f848a2f)

![image](https://github.com/user-attachments/assets/1d79fa63-7375-4a5d-8b4f-09052e2a35c3)

![image](https://github.com/user-attachments/assets/b5d84801-7158-425a-aba0-ac9e8d2dbbad)

![image](https://github.com/user-attachments/assets/9f4d10f9-74e7-45ea-8e32-3c57e7058f77)

![image](https://github.com/user-attachments/assets/f9dbd113-2fcf-4c4b-a608-76b234e21a09)

![image](https://github.com/user-attachments/assets/b8a106ad-9946-45d4-852c-6798ebb60294)



## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
