# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm:

1. Start the program.
2. Import the required libraries such as NumPy, Matplotlib and Scikit-learn.
3. Initialize the input data (study hours) and output data (student marks).
4. Create a Simple Linear Regression model.
5. Train the model using the given input and output data.
6. Calculate the slope and intercept of the regression line.
7. Predict the marks based on the study hours.
8. Display the predicted marks.
9. Plot the actual data points and the regression line.
10. Predict the marks for new study hours.
11. Stop the program.


## Program:
```
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: Krisha Princy N S
RegisterNumber: 212224060126


# 1. Import libraries
import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression

# 2. Input data
hours = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9]).reshape(-1, 1)
marks = np.array([20, 25, 35, 40, 50, 55, 65, 75, 85])

# 3. Create Linear Regression model
model = LinearRegression()

# 4. Train the model
model.fit(hours, marks)

# 5. Predict marks
predicted_marks = model.predict(hours)

print("Slope:", model.coef_[0])
print("Intercept:", model.intercept_)
print("Predicted marks:", predicted_marks)

# 6. Predict marks for new study hours
new_hours = np.array([[5.5]])
prediction = model.predict(new_hours)

print("Study Hours:", new_hours[0][0])
print("Predicted Marks:", prediction[0])

# 7. Plot the results
plt.scatter(hours, marks, color="blue", label="Actual Marks")
plt.plot(hours, predicted_marks, color="red",
         label="Regression Line")

plt.xlabel("Study Hours")
plt.ylabel("Marks")
plt.title("Student Marks Prediction")
plt.legend()
plt.grid(True)
plt.show()

```

## Output:
<img width="1138" height="732" alt="image" src="https://github.com/user-attachments/assets/64822273-b796-4f8a-9cea-2fbb4cf2c7b0" />



## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
