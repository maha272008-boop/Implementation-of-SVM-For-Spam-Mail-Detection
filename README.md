# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import required libraries such as Pandas and sklearn.
2.Load the dataset containing email messages and labels.
3.Convert text data into numerical vectors using TF-IDF.
4.Split dataset into training and testing sets.
5.Train SVM classifier using linear kernel.
6.Predict and evaluate spam detection accuracy. 

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by:MAHALAKSHMI P 
RegisterNumber:212225100024
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.feature_extraction.text import TfidfVectorizer
from sklearn.svm import SVC
from sklearn.metrics import accuracy_score, classification_report

# Dataset
data = {
    'Message': [
        "Win free lottery now",
        "Meeting at 10 AM",
        "Claim your prize",
        "Submit your assignment",
        "You won cash reward",
        "Lunch break today"
    ],
    'Label': [1, 0, 1, 0, 1, 0]
}

df = pd.DataFrame(data)

# Input & Output
X = df['Message']
y = df['Label']

# Text to numeric conversion
vectorizer = TfidfVectorizer()
X = vectorizer.fit_transform(X)

# Train-test split
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.33, random_state=42)

# Model
model = SVC(kernel='linear')
model.fit(X_train, y_train)

# Prediction
y_pred = model.predict(X_test)

# Evaluation
print("Accuracy:", accuracy_score(y_test, y_pred))
print("\nClassification Report:\n", classification_report(y_test, y_pred)) 
*/
```

## Output:
<img width="714" height="347" alt="{D861ED26-3555-4FBE-ADC4-B838E8AFAF96}" src="https://github.com/user-attachments/assets/98d39ff5-292f-41b5-9193-9eae038dbc49" />


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
