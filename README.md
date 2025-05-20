
# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Load the Dataset

2.Create a Copy of the Original Data

3.Drop Irrelevant Columns (sl_no, salary)

4.Check for Missing Values

5.Check for Duplicate Rows

6.Encode Categorical Features using Label Encoding

7.Split Data into Features (X) and Target (y)

8.Split Data into Training and Testing Sets

9.Initialize and Train Logistic Regression Model

10.Make Predictions on Test Set

11.Evaluate Model using Accuracy Score

12.Generate and Display Confusion Matrix

13.Generate and Display Classification Report

14.Make Prediction on a New Sample Input 

## Program:
```
/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by: MUSFIRA MAHJABEEN M
RegisterNumber:  212223230130

import pandas as pd
pf=pd.read_csv("Placement_Data.csv")
pf.head()
pf1=pf.copy()
pf1=pf1.drop(['sl_no','salary'],axis=1)
pf1.head()
pf1.isnull().sum()
pf1.duplicated().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
pf1["gender"]=le.fit_transform(pf1["gender"])
pf1["ssc_b"]=le.fit_transform(pf1["ssc_b"])
pf1["hsc_b"]=le.fit_transform(pf1["hsc_b"])
pf1["hsc_s"]=le.fit_transform(pf1["hsc_s"])
pf1["degree_t"]=le.fit_transform(pf1["degree_t"])
pf1["workex"]=le.fit_transform(pf1["workex"])
pf1["specialisation"]=le.fit_transform(pf1["specialisation"])
pf1["status"]=le.fit_transform(pf1["status"])
pf1
x=pf1.iloc[:,:-1]
x
y=pf1["status"]
y
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
from sklearn.metrics import accuracy_score,confusion_matrix,classification_report
accuracy=accuracy_score(y_test,y_pred)
accuracy
confusion=confusion_matrix(y_test,y_pred)
confusion
classification=classification_report(y_test,y_pred)
print(classification)
lr.predict([[1,80,1,9,1,1,90,1,0,85,1,85]])
*/
```

## Output:
### pf.head()
![image](https://github.com/user-attachments/assets/0df222b2-7ebb-4226-9f2e-cd2bb7e16f6c)


### pf1.head()
![Screenshot 2025-03-28 123613](https://github.com/user-attachments/assets/06c61909-785e-4b2d-9ffe-cbd8bd3e33d8)
### pf1.isnull().sum()
![Screenshot 2025-03-28 123622](https://github.com/user-attachments/assets/63b43a33-c8a2-416c-bc0b-3fd5b8e377b9)
### pf1.duplicated().sum()
![Screenshot 2025-03-28 123635](https://github.com/user-attachments/assets/be43ef31-1dc7-4ecc-9798-f58dea38af50)

### pf1
![Screenshot 2025-03-28 123733](https://github.com/user-attachments/assets/50cf020a-1aaf-43cf-beae-3641d03f9832)
### Value of x
![Screenshot 2025-03-28 123747](https://github.com/user-attachments/assets/16248e05-b308-4a94-a8fb-811bac016623)

### Value of y
![Screenshot 2025-03-28 123801](https://github.com/user-attachments/assets/9d393d35-b6dd-423e-801a-9d671f836402)

### Value of y_pred,accuracy,confusion_matrix,classification
![Screenshot 2025-03-28 123815](https://github.com/user-attachments/assets/00a09ca2-c40f-493f-8bab-3ea562c03213)


![image](https://github.com/user-attachments/assets/f16a0e23-2951-4eca-b48b-11db90a36f31)









## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
