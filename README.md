# Student Performance Prediction 📊

## Overview

This project uses Machine Learning to predict students' final mathematics grades based on academic, demographic, and behavioral features.

The goal is to explore student performance data, train regression models, and compare their performance using appropriate evaluation metrics.

## Project Highlights

- Perform Exploratory Data Analysis (EDA) using Python.
- Investigate relationships between student features and final grades.
- Train and compare three Machine Learning regression models.
- Evaluate model performance using MAE and R² Score.
- Analyze model results, limitations, and potential improvements.

## Objectives

- Explore and analyze student performance data.
- Identify relationships between student features and final grades.
- Build and evaluate Machine Learning regression models.
- Compare different algorithms and understand their strengths and limitations.
- Practice data analysis, model training, and model evaluation using Python.

## Dataset

This project uses the [Student Performance dataset](https://archive.ics.uci.edu/dataset/320/student+performance) from the UCI Machine Learning Repository.

The dataset contains information about students from two Portuguese schools, including study time, previous grades, absences, and other demographic and academic features.

This project uses the mathematics dataset: `student-mat.csv`.

The target variable is `G3`, which represents the final mathematics grade.

## Technologies Used

- Python
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Project Structure

```text
student-performance-prediction/
├── data_analysis.ipynb
├── model_comparison.ipynb
├── student-mat.csv
├── requirements.txt
├── .gitignore
└── README.md
```

## Methodology

### 1. Data Analysis

- Load and inspect the dataset.
- Check for missing values and duplicate records.
- Calculate descriptive statistics.
- Visualize the distribution of final grades.
- Explore relationships between student features and final grades.

### 2. Data Preparation

- Select relevant input features.
- Define `G3` as the target variable.
- Split the dataset into training and testing sets.

### 3. Model Training

Three regression algorithms are evaluated:

- **Linear Regression:** A baseline model that estimates relationships between input features and the target variable.
- **Decision Tree Regressor:** A tree-based model that learns decision rules from the training data.
- **Random Forest Regressor:** An ensemble model that combines predictions from multiple decision trees.

### 4. Model Evaluation

The models are evaluated using the following metrics:

- **Mean Absolute Error (MAE):** Measures the average absolute difference between actual and predicted grades. Lower values indicate better performance.
- **R² Score:** Measures how well the model explains the variation in the target variable. Higher values generally indicate better performance.

All models are compared using the same training and testing split.

## Results

The following results were obtained in the experiment:

### Random Forest Regressor

- **MAE:** `1.051`
- **R² Score:** `0.872`

### Decision Tree Regressor

- **MAE:** `1.199`
- **R² Score:** `0.813`

### Linear Regression

- **MAE:** `1.339`
- **R² Score:** `0.782`

### Findings

- Random Forest achieved the lowest MAE and the highest R² Score among the three evaluated models.
- Decision Tree performed better than Linear Regression according to both evaluation metrics.
- Random Forest reduced MAE by approximately 21.5% compared with Linear Regression.

These results are based on a single train-test split and should not be interpreted as a guarantee of performance on unseen data or in other educational settings.

## Limitations

- The dataset comes from two Portuguese schools and may not represent all educational settings.
- Model predictions are estimates and are not guaranteed to match students' actual grades.
- Previous grades (`G1` and `G2`) may provide strong predictive information about the final grade (`G3`).
- Observed relationships and feature importance do not establish causation.
- Model performance may vary depending on the train-test split and the selected features.

## Future Improvements

- Compare model performance with and without previous grades (`G1` and `G2`).
- Tune hyperparameters using cross-validation.
- Visualize actual versus predicted grades.
- Evaluate model stability using additional validation methods.
- Explore additional regression algorithms.
- Develop a simple web interface for interactive predictions.

## How to Run the Project

### 1. Clone the Repository

```bash
git clone YOUR_REPOSITORY_URL
cd student-performance-prediction
```

Replace `YOUR_REPOSITORY_URL` with your GitHub repository URL.

### 2. Install Dependencies

```bash
python -m pip install -r requirements.txt
```

### 3. Launch Jupyter Notebook

```bash
jupyter notebook
```

Run `data_analysis.ipynb` first, followed by `model_comparison.ipynb`.

Make sure `student-mat.csv` is located in the project root directory.


