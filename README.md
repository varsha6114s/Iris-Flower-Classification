# Iris Flower Classification - GrowthLink Internship Assignment

## Project Overview
This project is a complete machine learning pipeline that classifies Iris flowers into one of three species (“setosa”, “versicolor”, or “virginica”) based on their petal and sepal measurements. The model is trained using the provided `IRIS.csv` dataset.

---

## Dataset
- **Filename:** `IRIS.csv`
- **Features:**
  - sepal_length
  - sepal_width
  - petal_length
  - petal_width
- **Target:**
  - species (Iris-setosa, Iris-versicolor, Iris-virginica)

---

## Workflow

### 1. Data Loading
- The dataset is loaded using `pandas.read_csv()`.
- Target labels are cleaned to remove the "Iris-" prefix for simplicity.

### 2. Exploratory Data Analysis (EDA)
- Dataset structure and class distribution are analyzed.
- Pairplots, histograms, boxplots, and a correlation heatmap are plotted to understand feature relationships.

### 3. Feature Engineering
- Feature importance is evaluated using ANOVA F-value.
- New features (`sepal_ratio` and `petal_ratio`) are created to enhance model performance.

### 4. Data Preprocessing
- The dataset is split into training and testing sets.
- Features are standardized using `StandardScaler` for better model convergence.

### 5. Model Training
- Five models are trained:
  - Logistic Regression
  - K-Nearest Neighbors
  - Support Vector Machine
  - Decision Tree
  - Random Forest
- Cross-validation is performed to evaluate stability.

### 6. Model Selection
- The best-performing model is selected based on test accuracy.
- Model performance is compared visually using a bar plot.

### 7. Hyperparameter Tuning
- Grid Search Cross Validation (`GridSearchCV`) is used to optimize hyperparameters for the best model.

### 8. Final Evaluation
- The tuned model is evaluated on the test set.
- A confusion matrix and classification report are generated.

---

## Key Results
- Best model identified with tuned hyperparameters.
- Final test set accuracy reported.
- Most important features identified.

---

## Requirements

### Libraries Used
- numpy
- pandas
- matplotlib
- seaborn
- scikit-learn

Install them using:
```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

---

## How to Run
1. Place `IRIS.csv` in the working directory.
2. Run the Python script.
3. All outputs (EDA plots, model performance, etc.) will be generated step-by-step.

---

## Author
**Varsha S**

---

## Notes
- Dataset was standardized for better model performance.
- Feature engineering boosted the model's ability to differentiate between species.
- The model is ready for real-world deployment and prediction tasks.

---

## Sample Prediction Code
You can use the following function to predict new samples:
```python
def predict_iris_species(sepal_length, sepal_width, petal_length, petal_width):
    # Prepare input data
    # ... (see full code for details)
    return predicted_species
```

---

## License
This project is for academic purposes under the GrowthLink Internship Assignment.

