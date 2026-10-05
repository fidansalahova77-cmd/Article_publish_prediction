# Article Publish Prediction

A machine learning project that predicts whether an article will be **published or not**. Three classification models are built and compared: Logistic Regression, Random Forest, and LightGBM.

## Project Overview

The goal of this project is to build a binary classifier that estimates the likelihood of an article being published. The workflow covers data exploration, preprocessing, model training, and evaluation, with a baseline model first and progressively stronger models afterwards.

## Target Variable

- **Target:** whether the article was published or not (binary classification)

## Workflow

1. **Data exploration:** getting familiar with the dataset, its columns, missing values, and distributions
2. **Train/test split:** splitting the data into training and test sets
3. **Feature scaling:** scaling the features to a common range (fitted on the training set only to avoid data leakage)
4. **Modeling:**
   - Logistic Regression (baseline)
   - Random Forest
   - LightGBM (Light Gradient Boosting Machine)
5. **Evaluation:** comparing the models on the test set using Accuracy and ROC-AUC

## Results

| Model               | Accuracy | ROC-AUC |
|---------------------|----------|---------|
| Logistic Regression | 0.5587   | -       |
| Random Forest       | 0.6623   | 0.7198  |
| **LightGBM**        | **0.6726** | **0.7297** |

**Key takeaways:**
- LightGBM achieved the best performance on both Accuracy and ROC-AUC.
- Random Forest came close behind, and both tree-based models clearly outperformed the Logistic Regression baseline.
- The gap between the linear baseline and the tree-based models suggests the relationship between the features and the target is non-linear.

## Tech Stack

- Python
- pandas, NumPy
- scikit-learn
- LightGBM
- Jupyter Notebook

## Getting Started

```bash
# Clone the repository
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>

# Install dependencies
pip install -r requirements.txt

# Launch the notebook
jupyter notebook
```

## Project Structure

```
├── data/              # Dataset
├── notebooks/         # Jupyter notebooks with the analysis and models
├── requirements.txt   # Python dependencies
└── README.md
```

## Future Improvements

- Hyperparameter tuning (e.g., GridSearchCV or Optuna)
- Cross-validation for more robust evaluation
- Additional metrics (Precision, Recall, F1-score, confusion matrix)
- Feature importance analysis and additional feature engineering

## Author

**Your Name**
https://www.linkedin.com/in/fidan-salahova-2b581a314/?isSelfProfile=true
