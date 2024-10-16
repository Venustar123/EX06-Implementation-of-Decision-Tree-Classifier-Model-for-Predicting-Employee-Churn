# EX 6 Implementation of Decision Tree Classifier Model for Predicting Employee Churn
## DATE:
## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.import the employee churn dataset
   
2.if the dataset has missing values handel them using techiniques such as mean

3.convert categorical variables into numerical format using techniques such as noe_hot encoding

4.scale features if necessary using standardscaler
 

## Program:
```
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: BASHA VENU
RegisterNumber:  2305001005

import pandas as pd
from sklearn.tree import DecisionTreeClassifier,plot_tree
from sklearn.preprocessing import LabelEncoder
import matplotlib.pyplot as plt
df=pd.read_csv('/content/Employee_EX6.csv')
data = pd.read_csv('/content/Employee_EX6.csv')
data = df.copy()
data
le = LabelEncoder()
data['salary'] = le.fit_transform(data['salary'])
data
X = data.drop(['Departments','left'],axis=1)
Y = data['left']
clf = DecisionTreeClassifier()
clf.fit(X,Y)
plt.figure(figsize=(80,80))
plot_tree(clf, feature_names=X.columns,class_names=['LEFT','"NOT LEFT"'],filled=True,fontsize=14)
plt.show()
```

## Output:
![image](https://github.com/user-attachments/assets/98c3f182-fe86-4864-a526-708dd478a6ea)
![image](https://github.com/user-attachments/assets/bed64612-3eaa-4298-a962-80016f4eb623)
![image](https://github.com/user-attachments/assets/bb16f494-1013-4c15-b0c6-a74c6a1b10d3)
![Screenshot 2024-10-16 203141](https://github.com/user-attachments/assets/0cb088ac-b09a-4e23-afb8-2b865004f8fc)



## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
