# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.Import the required libraries.
2.Upload the csv file and read the dataset.
3.Check for any null values using the isnull() function.

## Program:
```
Program to implement the SVM For Spam Mail Detection..
Developed by: G.Pavithra
RegisterNumber:  212221240036
```
```
import pandas as pd
data=pd.read_csv("spam.csv",encoding='latin-1')
data.head()
data.info()
data.isnull().sum()
x=data["v1"].values
y=data["v2"].values
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
from sklearn.feature_extractiaon.text import CountVectorizer
cv=CountVectorizer()
x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)
from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
```

## Output:
### DATA HEAD:
![n1](https://user-images.githubusercontent.com/93427264/173004225-a96d511c-72e4-4dda-95e7-c8ba66550ea1.png)
### DATA INFO:
![n2](https://user-images.githubusercontent.com/93427264/173004300-81d8c996-ac1e-45c8-9361-baf4217910cd.png)
### NULL SUM:
![n3](https://user-images.githubusercontent.com/93427264/173004371-c38c7c7f-d23d-4c28-9c1f-92cd3cf3cd52.png)
### PREDICTION:
![n4](https://user-images.githubusercontent.com/93427264/173004436-fb621d67-d2c8-4d0c-9d29-84d41bb1792d.png)
### ACCURACY:
![n5](https://user-images.githubusercontent.com/93427264/173004488-29601ab2-740f-4ab8-bbc5-9929e2c72bda.png)

## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
