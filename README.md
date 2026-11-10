# Heart Disease Prediction

A machine learning project that predicts whether a patient has heart disease
from 13 clinical measurements.

## Problem
Heart disease screening needs tools that catch sick patients early.
I built a classification model to predict heart disease (Yes or No).

## Data
303 patients, 13 features (age, chest pain type, cholesterol, max heart rate, and more).
The target is balanced: 54% No and 46% Yes.

## Steps
1. Data cleaning: handled missing values in Ca and Thal
2. Exploratory analysis: compared patients with and without heart disease
3. Preparation: train/test split, encoding, scaling inside a pipeline
4. Modelling: logistic regression vs random forest with 5-fold cross-validation
5. Evaluation: accuracy, confusion matrix, precision and recall
6. Tuning: [best C value] and saved the final model

## Results
| Model | Cross-validated AUC |
|---|---|
| Logistic Regression | 0.899 |
| Random Forest | 0.890 |

On 61 unseen patients, the logistic regression model reached about 87% accuracy.
It found 26 of 28 patients with heart disease (recall 93%)
and raised 6 false alarms (precision 81%).

## Key findings
- The strongest signals were [Ca], [ChestPain_asymptomatic] and [Thal_reversable].
- Lower max heart rate went with higher risk of heart disease.
- Cholesterol and fasting blood sugar were weak predictors on their own.

## Limitations
- Small dataset, so results are only an estimate.
- For learning only. Not for real medical decisions.

## How to run
1. Clone this repository
2. Install: `pip install pandas scikit-learn matplotlib seaborn joblib`
3. Open `heart_disease_prediction.ipynb` and run all cells

## Tools
Python, pandas, scikit-learn, matplotlib, seaborn

## Author
Kefentse Malatji
