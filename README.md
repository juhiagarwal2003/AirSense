# 🌍 AirSense: Predicting Air Quality with Regression Techniques 🌿

Welcome to **AirSense**—a project that explores the relationship between pollutant levels and sensor readings using Lasso and Ridge Regression! Predict air quality and compare different regression techniques to find the best model! 🚀✨

## 📚 Table of Contents

1. [Overview](#overview)
2. [Dataset](#dataset)
3. [Google Colab Setup](#google-colab-setup)
4. [Usage](#usage)
5. [Implementation Details](#implementation-details)
6. [Results](#results)
7. [Contributing](#contributing)
8. [Acknowledgements](#acknowledgements)

## 🌟 Overview

**AirSense** leverages Lasso, Ridge, and SVR models to predict air quality based on pollutant levels. By preprocessing and scaling the dataset, we create regression models that analyze sensor data to predict CO levels. We then compare the performance of these models using the R² score.

## 📊 Dataset

The [Air Quality Dataset](https://archive.ics.uci.edu/ml/datasets/Air+Quality) contains 9358 hourly averaged responses from sensors. Key columns include:

- **Independent Variables**: Various sensor readings like NO2, C6H6, NMHC, etc.
- **Dependent Variable**: `CO(GT)`—the target pollutant we want to predict.

## 🚀 Google Colab Setup

Follow these steps to set up the project in Google Colab:

1. **Open the Colab Notebook**:
   - Click on [this link](https://colab.research.google.com/) to create a new notebook or open an existing one.

2. **Clone the Repository**:
   To work with the code and dataset, run the following code cell:
   ```python
   !git clone https://github.com/juhiagarwal2003/AirSense.git
   ```

3. **Install Required Libraries**:
   Run the following code to install any missing libraries:
   ```python
   !pip install -r AirSense/requirements.txt
   ```

> Ensure your dataset is uploaded to the Colab environment, or use the provided file link to load it using pandas.

## 🎉 Usage

Once your environment is set up, you can dive into AirSense:

1. **Load the dataset** using pandas.
2. **Preprocess** the data (handle missing values, scale features).
3. **Train the models** (Ridge, Lasso, SVR) and evaluate performance.

## ✨ Implementation Details

Here’s how the project works:

1. **Data Preprocessing**:
   - Handle missing values using mean imputation.
   - Drop categorical columns like `Date` and `Time`.
   - Scale numerical features using `StandardScaler`.

2. **Model Training**:
   - Train Ridge and Lasso regression models with `alpha=12`.
   - Compare the performance with an SVR model.

3. **Performance Evaluation**:
   - Use the R² score to evaluate and compare the models.

### 🔑 Key Functions

- `Ridge(alpha=12)`: Build a Ridge regression model.
- `Lasso(alpha=12)`: Build a Lasso regression model.
- `SVR(kernel='linear')`: Build an SVR model with a linear kernel.
- `r2_score(y_test, y_pred)`: Evaluate model performance using the R² score.

## 🎨 Results

- **Ridge Regression**: R² score = 0.515
- **Lasso Regression**: R² score = 0.457
- **SVR**: R² score = 0.481

The Ridge regression model performed best, followed by SVR and Lasso.

## 📝 Contributing

We welcome contributions! Feel free to submit a pull request or open an issue to improve AirSense. Let's make air quality predictions even better together! 🌍

## 🎉 Acknowledgements

A big thank you to the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Air+Quality) for providing the dataset and the open-source community for their invaluable tools and resources!

---

Now, let's predict air quality and breathe easy! 💨🌱

--- 
