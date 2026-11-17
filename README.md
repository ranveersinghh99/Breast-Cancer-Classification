# Breast Cancer Classification

## Project Overview
This project uses machine learning to classify breast cancer tumors as **Malignant** or **Benign** using features from the Breast Cancer dataset. It trains and evaluates a Logistic Regression model with Python.

## Project Structure

```text
Breast-Cancer-Classification/
│
├── data/
│   └── Breast_Cancer.csv
│
├── notebooks/
│   └── BREAST_CANCER_CLASSIFICATION_PROJECT.ipynb
│
├── images/
│
├── README.md
├── requirements.txt
└── .gitignore
```

## Technologies Used
- Python
- Pandas
- NumPy
- Scikit-learn
- Jupyter Notebook

## Dataset
The project uses `Breast_Cancer.csv`, containing 569 records. The notebook removes the `id` and `Unnamed: 32` columns before training.

The target column is `diagnosis`:
- `M` is mapped to `0` (Malignant).
- `B` is mapped to `1` (Benign).

The remaining 30 numerical columns are used as input features.

## Project Workflow
1. Import the required libraries.
2. Load and inspect the dataset.
3. Check for missing values.
4. Remove unnecessary columns.
5. Convert diagnosis labels to numeric values.
6. Separate features (`X`) and target (`y`).
7. Split the data into training and testing sets (80% / 20%).
8. Train a Logistic Regression model.
9. Evaluate accuracy on the training and testing data.
10. Use the trained model to predict the diagnosis for a sample input.

## Model
**Algorithm:** Logistic Regression

The notebook uses Scikit-learn's `LogisticRegression` with `max_iter=10000`.

## Getting Started

### 1. Clone the repository
```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd Breast-Cancer-Classification
```
Replace `YOUR_GITHUB_REPOSITORY_URL` with your GitHub repository URL.

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Run the notebook
```bash
jupyter notebook
```

Open `notebooks/BREAST_CANCER_CLASSIFICATION_PROJECT.ipynb` and run the cells.

**Dataset path:** Since the notebook is inside `notebooks/` and the CSV is inside `data/`, load it with:
```python
df = pd.read_csv("../data/Breast_Cancer.csv")
```

## Future Improvements
- Add exploratory data analysis and visualizations.
- Evaluate using a confusion matrix, precision, recall, and F1-score.
- Compare Logistic Regression with other classification algorithms.
- Add cross-validation and hyperparameter tuning.

## Disclaimer
This project is for educational purposes only. It is not intended for medical advice or real-world medical diagnosis.
