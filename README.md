# NT-M5-H1 Smoking Prediction Competition

This repository contains a solution to the **NT-M5-H1 Smoking Prediction Competition**, which focuses on predicting smoking status using health-related data. This project employs machine learning models, primarily using Python and various data science libraries, to create accurate predictions based on provided datasets.

## Project Overview

The goal of this project is to predict whether an individual is a smoker based on several health indicators. The dataset includes various attributes related to age, height, weight, cholesterol levels, blood pressure, and other health metrics.

### Key Features
- **Data Analysis and Visualization**: Initial data exploration and visualizations to understand feature distributions and relationships.
- **Feature Engineering**: Creation of new, relevant features to enhance model performance.
- **Modeling**: Implementation of multiple classifiers, including logistic regression, decision trees, ensemble methods, and more.
- **Hyperparameter Tuning**: Finding optimal model parameters using techniques like cross-validation and grid search.
- **Evaluation**: Assessing model performance using metrics such as ROC-AUC and accuracy.

## Repository Structure

```
NT-M5-H1-Smoking-Cmpetition/
├── notebooks/               # Jupyter notebooks for data analysis and modeling
├── data/                    # datasets for usage model
├── requirements.txt         # List of required libraries and dependencies
├── smoking_model.joblib     # Finla model for prediction
└── README.md                # Project documentation
```
  
## Installation

To run this project locally, follow these steps:

1. Clone this repository:
   ```bash
   git clone https://github.com/UznetDev/NT-M5-H1-Smoking-Cmpetition.git
   ```
2. Navigate to the project directory:
   ```bash
   cd NT-M5-H1-Smoking-Cmpetition
   ```
3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

### Usage

To load and use the model for prediction, follow these steps:

```python
from joblib import load

# Load the model
model = load('smoking_model.joblib')

# Define input data (X) for prediction
# Example input data for one individual
X_new = []  # Replace with actual input values

# Predict smoking status
prediction = model.predict(X_new)

# Display the result
if prediction[0] == 1:
    print("This individual is likely a smoker.")
else:
    print("This individual is likely a non-smoker.")
```

### Model Details

The `smoking_model.joblib` file contains a pre-trained model created with `scikit-learn`. You can use the `predict` function to determine smoking status based on input health measurements.

**Note:** The example input (`X_new`) should be replaced with real data according to your project requirements.

## Dataset

The dataset consists of several features related to individuals' health, including:
- **Basic Attributes**: Age, height, weight, waist circumference, eyesight, and hearing levels.
- **Blood Pressure**: Systolic and diastolic blood pressure.
- **Blood Metrics**: Cholesterol, triglyceride, HDL, LDL, and hemoglobin levels.
- **Additional Health Indicators**: Serum creatinine, AST, ALT, Gtp, and urine protein.
- **Target**: A binary column indicating whether an individual is a smoker (1 for smoker, 0 for non-smoker).

### Feature Engineering

The following new features have been engineered to enhance the model's predictive power:
- **BMI** (Body Mass Index)
- **Waist-to-Height Ratio**
- **Cholesterol Ratio** (Total Cholesterol/HDL)
- **Liver Enzyme Ratio** (ALT/AST)

## Models Used

The project explores multiple machine learning algorithms for classification:
- **Linear Models**: Logistic Regression, Ridge Classifier, SGD Classifier
- **Naive Bayes Classifiers**: GaussianNB, MultinomialNB, BernoulliNB
- **Support Vector Machines**: SVC, LinearSVC, NuSVC
- **Decision Trees and Ensembles**: Decision Tree, RandomForest, Gradient Boosting, AdaBoost, Extra Trees
- **Discriminant Analysis**: Linear Discriminant Analysis, Quadratic Discriminant Analysis

### Hyperparameter Tuning

To find the best parameters for the models, this project utilizes optuna and cross-validation methods, specifically focusing on maximizing ROC-AUC scores to improve model performance.

## Evaluation

The models are evaluated based on the following metrics:
- **ROC-AUC Score**: Primary metric to assess model performance in terms of distinguishing between smokers and non-smokers.

## Usage

1. **Exploratory Data Analysis (EDA)**: Start with EDA notebooks in the `notebooks/` folder to understand the dataset and visualize patterns.
2. **Model Training**: Run the scripts or notebooks to train the models and evaluate their performance.
3. **Hyperparameter Tuning**: Use the scripts for hyperparameter tuning to improve model accuracy.
4. **Save nodel**: save model in 'model.joblib.



## Contributing

Contributions are welcome! If you'd like to improve this project, please fork the repository and make a pull request.

1. Fork the repository.
2. Create a new branch for your feature or bug fix:
   ```bash
   git checkout -b feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add a new feature"
   ```
4. Push to your branch:
   ```bash
   git push origin feature-name
   ```
5. Open a pull request.

## License

This project is licensed under the [MIT](LICENCE) License.

## Contact's

If you have any questions or suggestions, please contact:
- Email: uznetdev@gmail.com
- GitHub Issues: [Issues section](https://github.com/UznetDev/NT-M5-H1-Smoking-Cmpetition/issues)
- GitHub Profile: [UznetDev](https://github.com/UznetDev/)
- Telegram: [UZNet_Dev](https://t.me/UZNet_Dev)
- Linkedin: [Abdurakhmon Niyozaliev](https://www.linkedin.com/in/abdurakhmon-niyozaliyev-%F0%9F%87%B5%F0%9F%87%B8-66545222a/)

---

Thank you for your interest in this project. We hope it helps in your journey to understand and predict smoking habits using data science!
