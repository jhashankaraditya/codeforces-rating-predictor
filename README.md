### Project Title: Codeforces Ratings Prediction

---

#### Introduction

This project focuses on building a machine learning regression model to predict the new expected ratings on Codeforces, an online competitive programming platform, based on performance in the past 10 Codeforces contests. The goal is to leverage historical performance data to provide accurate predictions for users' future ratings.

---

#### Dataset

The dataset for this project was sourced from Kaggle, containing users' performance metrics across multiple Codeforces contests. Each row in the dataset represents a user, and the columns contain the ratings from the past 10 contests.

---

#### Data Cleaning

The data cleaning process was performed in the `data_cleaning.ipynb` notebook. During the analysis, two significant issues were identified and addressed:

1. **Float Values in Features**: Features 'contest4' to 'contest10' had float values which needed conversion to integers. This was essential to ensure consistency and accuracy in the model training process.
   
2. **Missing Values**: Several missing values were found in features 'contest4' to 'contest10'. These missing values were handled using appropriate imputation methods to prevent skewing the model's performance.

After cleaning the data, the refined dataset was saved into a new CSV file named `cleaned_regression_df.csv`.

---

#### Model Training

The model training process was conducted in the `model_training.ipynb` notebook. The following steps were carried out:

1. **Train-Test Split**: The cleaned dataset was split into training and testing sets to evaluate the model's performance accurately.

2. **Algorithm Selection**: Several machine learning algorithms were chosen to train the model. The performance of each algorithm was evaluated based on their accuracy scores. The algorithms used are:
   - **Linear Regression**: Achieved an accuracy of 92.08%
   - **Random Forest Regression**: Achieved an accuracy of 94.56%
   - **Support Vector Regression (SVR)**: Achieved an accuracy of 91.57%

The Random Forest Regression model outperformed the others with the highest accuracy, making it the preferred model for this project.

---

#### Conclusion

This project demonstrates the application of machine learning techniques to predict Codeforces ratings based on past performance. The data cleaning process ensured high-quality input data, and multiple regression models were evaluated to select the best-performing algorithm. The Random Forest Regression model, with an accuracy of 94.56%, was identified as the most effective model for this prediction task.

---

#### Repository Structure

- `data_cleaning.ipynb`: Jupyter notebook containing the data cleaning and preprocessing steps.
- `model_training.ipynb`: Jupyter notebook detailing the model training and evaluation process.
- `cleaned_regression_df.csv`: The cleaned dataset used for model training.

---

By accurately predicting future ratings, this project aims to assist competitive programmers in tracking their progress and setting realistic goals for improvement on the Codeforces platform.
