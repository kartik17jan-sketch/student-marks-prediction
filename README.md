Student Marks Prediction using Linear Regression

This project predicts student exam scores based on the number of hours studied using a simple linear regression model.
The dataset contains 25 observations and is ideal for demonstrating fundamental supervised machine learning techniques.

The project includes dataset exploration, visualization, model training, evaluation, and prediction on new unseen values.

Project Structure
student-marks-prediction/
│
├── Student Marks Prediction.ipynb    # Main notebook
├── README.md                         # Documentation
├── requirements.txt                  # Dependencies          
│
└── results/                          # Plots (optional)
    ├── scatter_plot.png
    └── regression_line.png

Dataset Overview

The dataset is loaded from:

http://bit.ly/w-data



student-marks-prediction_Studen…

, the dataset has:

25 samples

2 columns:

Hours — hours studied

Scores — marks obtained

No missing values

Data types: float64 for Hours, int64 for Scores

Example rows:

Hours   Scores
2.5     21
5.1     47
3.2     27
8.5     75

Exploratory Data Analysis
✔ View dataset information
raw_data.info()

✔ Scatter Plot (page 1)

You plotted the relationship between study hours and scores:

plt.scatter(raw_data['Hours'], raw_data['Scores'])


This reveals a strong positive correlation.

Preprocessing

Extract features and labels:

x = raw_data[['Hours']].values
y = raw_data[['Scores']].values


Train–test split (page 4):

x_train, x_test, y_train, y_test = train_test_split(x, y, random_state=0)


Train size: 18 samples
Test size: 7 samples

Model — Linear Regression

Training the model (page 5):

model = LinearRegression()
model.fit(x_train, y_train)


You also plotted the best-fit regression line using Seaborn (page 5).
The line clearly shows a strong upward trend between hours studied and predicted marks.

Evaluation

Predictions on test set (page 6):

[16.84, 33.74, 75.50, 26.78, 60.58, 39.71, 20.82]

Mean Absolute Error (MAE)

MAE = 4.13
(Present in notebook output) 

student-marks-prediction_Studen…

This means predictions differ from actual marks by ~4 points on average.

Predicting New Values

Your notebook predicts scores for given hours of study:

Example 1 (page 6):
Hours = 9.25  
Predicted Score = 93.89

Example 2 (page 6):
Hours = 6.5  
Predicted Score = 66.55


These predictions follow the same linear trend.

How to Run This Project
1. Clone the repository
git clone https://github.com/<username>/student-marks-prediction.git
cd student-marks-prediction

2. Install dependencies
pip install -r requirements.txt

3. Run the notebook

Open in Google Colab or Jupyter:

Student Marks Prediction.ipynb

requirements.txt
numpy
pandas
scikit-learn
matplotlib
seaborn

Future Improvements

Add more features (study habits, sleep, environment)

Fit polynomial regression for non-linear relationships

Add R² score and residual plots

Deploy as a web app using Streamlit

Author

Kartik Rajesh
B.Tech CSE (AI/ML)
Linear Regression • Machine Learning Basics • Predictive Analytics
