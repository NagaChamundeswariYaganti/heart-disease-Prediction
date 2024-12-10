# Heart Disease Prediction Project

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.3+-green.svg)](https://scikit-learn.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

A comprehensive machine learning project for predicting heart disease in patients using ensemble and linear classification models. This project implements a complete ML pipeline including data preprocessing, model training, hyperparameter optimization, evaluation, and model interpretation.

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Project Structure](#project-structure)
- [Technologies Used](#technologies-used)
- [Contributing](#contributing)
- [License](#license)

## 🎯 Overview

This project implements a binary classification system to predict the presence of heart disease in patients based on clinical features. The analysis compares two machine learning algorithms:

- **Random Forest Classifier**: An ensemble method that aggregates predictions from multiple decision trees
- **Logistic Regression**: A linear classifier with L2 regularization

The project includes comprehensive model evaluation metrics and uses SHAP (SHapley Additive exPlanations) values for model interpretability, providing insights into which clinical features are most predictive of heart disease.

## ✨ Features

- **Data Preprocessing**: Automated data cleaning, merging, and feature scaling
- **Hyperparameter Optimization**: GridSearchCV with 5-fold cross-validation
- **Model Comparison**: Comprehensive evaluation with accuracy, classification reports, and confusion matrices
- **Model Interpretability**: SHAP value analysis for feature importance visualization
- **Stratified Splitting**: Ensures balanced train/test distributions
- **Professional Documentation**: Clean, well-commented code with detailed explanations

## 📊 Dataset

The project uses two heart disease datasets:
- `heart.csv`: Primary dataset with clinical features
- `hd.csv`: Secondary dataset that is preprocessed and merged with the primary dataset

**Final Dataset Characteristics:**
- **Samples**: 1,324 patients
- **Features**: 13 clinical features
- **Target**: Binary classification (0 = No heart disease, 1 = Heart disease present)

## 🔬 Methodology

### 1. Data Preprocessing
- Load and merge multiple datasets
- Handle missing values and data type conversions
- Create target variable from clinical indicators
- Remove unnecessary columns

### 2. Feature Engineering
- StandardScaler normalization for optimal model performance
- Stratified train-test split (80/20) to maintain class distribution

### 3. Model Training
- **Random Forest**: Hyperparameter tuning for `n_estimators` and `max_depth`
- **Logistic Regression**: Hyperparameter tuning for regularization parameter `C`
- 5-fold cross-validation for robust parameter selection

### 4. Model Evaluation
- Test set accuracy comparison
- Classification reports (precision, recall, F1-score)
- Confusion matrix analysis
- Visual performance comparison

### 5. Model Interpretation
- SHAP value computation for Random Forest model
- Feature importance visualization
- Risk factor analysis

## 🚀 Installation

### Prerequisites

- Python 3.8 or higher
- pip package manager

### Setup

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd Heart_Disease
   ```

2. **Create a virtual environment (recommended)**
   ```bash
   python -m venv venv
   
   # On Windows
   venv\Scripts\activate
   
   # On macOS/Linux
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

## 💻 Usage

1. **Launch Jupyter Notebook**
   ```bash
   jupyter notebook
   ```

2. **Open and run the notebook**
   - Open `heart.ipynb`
   - Execute cells sequentially (Cell → Run All)
   - Ensure data files (`heart.csv` and `hd.csv`) are in the same directory

3. **View Results**
   - Model accuracy comparisons
   - Classification reports
   - SHAP feature importance plots

## 📈 Results

### Model Performance

The optimized models achieve the following test set accuracies:

- **Random Forest**: ~99% accuracy
- **Logistic Regression**: ~82% accuracy

The Random Forest model demonstrates superior performance and is selected as the final model for heart disease prediction.

### Key Insights

SHAP analysis reveals the most important clinical features contributing to heart disease prediction, enabling healthcare professionals to understand which factors are most critical in risk assessment.

## 📁 Project Structure

```
Heart_Disease/
│
├── heart.ipynb              # Main Jupyter notebook with complete analysis
├── heart.csv                # Primary heart disease dataset
├── hd.csv                   # Secondary heart disease dataset
├── requirements.txt         # Python package dependencies
├── .gitignore              # Git ignore file
└── README.md               # Project documentation
```

## 🛠️ Technologies Used

- **Python**: Core programming language
- **pandas**: Data manipulation and analysis
- **numpy**: Numerical computations
- **scikit-learn**: Machine learning algorithms and utilities
- **matplotlib**: Data visualization
- **seaborn**: Statistical data visualization
- **SHAP**: Model interpretability and explainability
- **Jupyter**: Interactive notebook environment

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- UCI Machine Learning Repository for heart disease datasets
- SHAP library developers for model interpretability tools
- scikit-learn community for comprehensive ML tools

---

**Note**: This project is for educational and research purposes. Always consult healthcare professionals for medical decisions.
