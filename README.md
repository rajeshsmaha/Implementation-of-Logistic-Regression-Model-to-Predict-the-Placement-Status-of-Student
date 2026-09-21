# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required Python libraries and create the student dataset.
2. Separate the input features and the placement status as input and output.
3. Create and train the Logistic Regression model using the training data.
4. Give the student's details as input and predict the placement status.

## Program:
```
/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by: Aashif Ahamed S
RegisterNumber:  212225040004

import pandas as pd
import numpy as np
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
from sklearn.linear_model import LogisticRegression
from sklearn.metrics import accuracy_score, confusion_matrix, classification_report
data = pd.read_csv("placement.csv")
data['status'] = data['status'].map({
    'Placed': 1,
    'Not Placed': 0
})
X = data[['ssc_p', 'mba_p']]
y = data['status']
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)
scaler = StandardScaler()
X_train = scaler.fit_transform(X_train)
X_test = scaler.transform(X_test)
model = LogisticRegression()
model.fit(X_train, y_train)
y_pred = model.predict(X_test)
print("Accuracy:", accuracy_score(y_test, y_pred))
print("\nConfusion Matrix:")
print(confusion_matrix(y_test, y_pred))
print("\nClassification Report:")
print(classification_report(y_test, y_pred))
new_student = np.array([[70, 75]])

new_student_scaled = scaler.transform(new_student)

prediction = model.predict(new_student_scaled)

print("\nPredicted Placement Status:",
      "Placed" if prediction[0] == 1 else "Not Placed")
*/
```

## Output:
![the Logistic Regression Model to Predict the Placement Status of Student](sam.png)
<img width="807" height="527" alt="image" src="https://github.com/user-attachments/assets/eb015318-98fd-4c82-9710-0114bc5d3947" />



## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
