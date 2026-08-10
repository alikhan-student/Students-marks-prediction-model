# Student Marks Predictor — Simple Linear Regression

A beginner-friendly machine learning project that predicts a student's exam score based on the number of hours they studied, using **Simple Linear Regression**.

## 📌 Overview

This project demonstrates the full workflow of building a simple linear regression model with `scikit-learn`:
- Loading and exploring a dataset
- Visualizing the relationship between study hours and exam scores
- Training a linear regression model
- Making predictions
- Evaluating model performance
- Visualizing the regression line against actual data

## 📂 Dataset

The dataset (`linear_regression_data.csv`) contains 98 records with two columns:

| Column | Description |
|---|---|
| `hours_studied` | Number of hours a student studied |
| `exam_score` | The score the student achieved on the exam |

## 🛠️ Tech Stack

- **Python 3**
- **NumPy** — numerical operations
- **Pandas** — data loading and manipulation
- **Matplotlib** — data visualization
- **Scikit-learn** — linear regression model

## 🚀 Workflow

1. **Import libraries** — numpy, pandas, matplotlib, sklearn
2. **Load the dataset** using `pd.read_csv()`
3. **Visualize the raw data** with a scatter plot (`hours_studied` vs `exam_score`)
4. **Train the model**:
   ```python
   lr = linear_model.LinearRegression()
   lr.fit(df[['hours_studied']], df.exam_score)
   ```
5. **Make a prediction** for a new value (e.g., predicting the score for a student who studied 9 hours):
   ```python
   lr.predict([[9]])
   ```
6. **Evaluate the model** using the R² score:
   ```python
   lr.score(df[['hours_studied']], df.exam_score)
   ```
7. **Visualize the fit** by plotting the regression line over the scatter data.

## 📊 Results

- **R² Score:** ~0.958 — the model explains about 95.8% of the variance in exam scores based on hours studied, indicating a strong linear relationship.
- **Example Prediction:** A student who studies 9 hours is predicted to score approximately **31.6**.

## 📈 Visualization

The final plot overlays the fitted regression line (red) on the actual data points (blue), showing how well the linear model captures the trend between study hours and exam performance.

## ▶️ How to Run

1. Clone or download this repository.
2. Make sure the dataset `linear_regression_data.csv` is in the correct path.
3. Install dependencies:
   ```bash
   pip install numpy pandas matplotlib scikit-learn
   ```
4. Open `student_marks_regression.ipynb` in Jupyter Notebook and run all cells.

## 🔮 Possible Improvements

- Add train/test split to evaluate generalization instead of scoring on the full dataset.
- Try polynomial regression if the relationship isn't perfectly linear at the extremes.
- Add residual plots to check for patterns in prediction errors.

## 👤 Author

Waqas ali khan student of AI at university of Peshawer
