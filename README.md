# student-marks-predictor
Simple Machine Learning project using Linear Regression to predict student marks from study hours (Python, scikit-learn)
import numpy as np
from sklearn.linear_model import LinearRegression

# Study hours vs marks
hours = np.array([[1], [2], [3], [4], [5], [6], [7], [8]])
marks = np.array([20, 30, 40, 50, 58, 68, 77, 85])

model = LinearRegression()
model.fit(hours, marks)

h = float(input("Enter study hours: "))
print("Predicted marks:", round(model.predict([[h]])[0], 2))
