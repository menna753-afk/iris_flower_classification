# Iris Flower Classification

A machine learning project that classifies iris flowers into three species (Iris-setosa, Iris-versicolor, Iris-virginica) from four measurements: sepal length, sepal width, petal length and petal width.

## Dataset
[Iris Species (UCI ML) on Kaggle](https://www.kaggle.com/datasets/uciml/iris): 150 samples, 3 balanced classes, no missing values. The `Id` column was dropped before training.

## Workflow
1. Load and explore the data
2. Visualize with a pairplot and a correlation heatmap
3. Stratified 80/20 train/test split and feature scaling
4. Train and compare four models: Logistic Regression, KNN, Decision Tree, SVM
5. Cross-validate (5-fold) and evaluate the best model with a classification report and confusion matrix

## Results
| Model | Test accuracy | 5-fold CV accuracy |
|---|---|---|
| SVM | 0.967 | 0.967 |
| Logistic Regression | 0.933 | 0.960 |
| KNN | 0.933 | 0.960 |
| Decision Tree | 0.900 | 0.953 |

SVM performed best. Setosa is perfectly separated, and the few errors come from Versicolor vs Virginica, which overlap.

## Tools
Python, pandas, NumPy, scikit-learn, Matplotlib, Seaborn

## Run it
```bash
pip install pandas numpy scikit-learn matplotlib seaborn
jupyter notebook iris_flower_classification.ipynb
```
Keep `Iris.csv` in the same folder as the notebook.
