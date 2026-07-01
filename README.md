# Salary Prediction Using Ensemble Learning

An internship project that predicts employee salary from years of professional experience, comparing a **Decision Tree Regressor** against a **Random Forest Regressor** (Ensemble Learning) to demonstrate how bagging reduces overfitting and improves generalisation.

| | |
|---|---|
| **Intern** | Pratibha Rathore |
| **Roll Number** | 2434015 |
| **Department** | Generative AI |
| **Organisation** | IBM NASSCOM |
| **Internship Duration** | 18 May – 18 June 2026 |
| **College** | S. S. Jain Subodh PG Autonomous College |
| **University** | Rajasthan University |
| **Academic Session** | 2025–2026 |

---

## 📁 Project Files

| File | Description |
|---|---|
| `Salary_Prediction_Report.docx` | Full 34-page university-style project report (cover page, certificate, declaration, acknowledgement, preface, abstract, TOC, 9 chapters, references, appendix, viva questions) |
| `Salary_Prediction_Notebook.ipynb` | Jupyter notebook with the complete, executed ML pipeline — EDA, model training, evaluation, and plots |
| `Salary_Data.csv` | Dataset used (30 records: Years of Experience vs Salary) |
| `README.md` | This file |

---

## 🎯 Objective

Build a regression model that predicts an employee's salary based on their years of experience, and determine whether an Ensemble Learning approach (Random Forest) outperforms a single Decision Tree.

## 📊 Dataset

- **File:** `Salary_Data.csv`
- **Records:** 30
- **Columns:** `YearsExperience` (float), `Salary` (int)
- **Missing values:** 0
- **Duplicate rows:** 0
- **Target variable:** `Salary`
- **Independent variable:** `YearsExperience`

## 🔁 Workflow

```
Salary Dataset
   ↓
Data Collection
   ↓
Data Preprocessing
   ↓
Exploratory Data Analysis (EDA)
   ↓
Feature Selection
   ↓
Train-Test Split (80:20)
   ↓
Decision Tree Regressor
   ↓
Random Forest Regressor
   ↓
Model Evaluation
   ↓
Salary Prediction
   ↓
Conclusion
```

## 🛠️ Tech Stack

- Python 3
- pandas, numpy — data handling
- matplotlib — visualisation
- scikit-learn — `DecisionTreeRegressor`, `RandomForestRegressor`, `train_test_split`, evaluation metrics
- Jupyter Notebook

## ▶️ How to Run

1. Make sure `Salary_Data.csv` is in the same folder as the notebook.
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib scikit-learn jupyter
   ```
3. Launch the notebook:
   ```bash
   jupyter notebook Salary_Prediction_Notebook.ipynb
   ```
4. Run all cells (`Kernel → Restart & Run All`). The notebook already contains saved outputs, so you can also just open and read it without re-running anything.

## 📈 Results

Both models were trained on an 80:20 train-test split (24 training / 6 testing records) and evaluated on the held-out test set:

| Metric | Decision Tree Regressor | Random Forest Regressor |
|---|---|---|
| MAE | ₹8,640.17 | **₹6,872.01** |
| MSE | 101,047,709.83 | **63,721,129.71** |
| RMSE | ₹10,052.25 | **₹7,982.55** |
| R² Score | 0.8022 | **0.8753** |

**Conclusion:** The Random Forest Regressor outperforms the Decision Tree Regressor across every metric. By aggregating predictions from 100 Decision Trees trained on bootstrap samples, Random Forest reduces variance and overfitting, producing more accurate and generalisable salary predictions.

## 🚀 Future Scope

- Incorporate additional features: Education, Job Role, Skills, Location
- Deploy the model as a web app using Flask or Streamlit
- Train on a larger, more diverse real-world salary dataset
- Explore Gradient Boosting and XGBoost for further accuracy gains

## 📚 References

- Aurélien Géron, *Hands-On Machine Learning with Scikit-Learn, Keras & TensorFlow*, O'Reilly Media
- Christopher M. Bishop, *Pattern Recognition and Machine Learning*, Springer
- [Scikit-learn Documentation](https://scikit-learn.org/stable/documentation.html)
- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [NumPy Documentation](https://numpy.org/doc/)
- [Matplotlib Documentation](https://matplotlib.org/stable/contents.html)
- IBM SkillsBuild Learning Resources
- Breiman, L. (2001). *Random Forests*. Machine Learning, 45, 5–32.

---

*Prepared as part of the IBM NASSCOM Internship Programme, Department of Generative AI.*
