# 🎓 Branching Toward Success: Predicting Student Dropout with Decision Trees

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python&logoColor=white)

This project uses a Decision Tree classifier to predict whether a student will drop out or graduate, based on academic, demographic, and socio-economic data. It is part of a broader effort to explore student retention strategies through data science and machine learning.

## 📌 Project Objective

To develop and evaluate a Decision Tree model capable of predicting student dropout, with the goal of:

- Identifying students at high risk of dropping out
- Understanding which features most influence graduation outcomes
- Supporting early intervention through interpretable machine learning

## 📊 Dataset

- **Source**: [Kaggle: Higher Education Predictors of Student Retention](https://www.kaggle.com/datasets/thedevastator/higher-education-predictors-of-student-retention)
- **Records**: 4,424 students
- **Target**: Dropout, Graduate, Enrolled *(Enrolled students were removed for binary classification)*
- **Features**: 34 academic, financial, and demographic variables

## 🧹 Preprocessing

- Removed “Enrolled” students
- One-hot encoded categorical features
- Handled duplicates and cleaned nulls
- Split data: 70% training, 30% testing

## 🌲 Model: Decision Tree Classifier

- **Algorithm**: Scikit-learn `DecisionTreeClassifier`
- **Tuning**: GridSearchCV (5-fold cross-validation)
- **Best Parameters**:
  - `criterion='gini'`
  - `max_depth=5`
  - `min_samples_split=2`
  - `min_samples_leaf=4`

## ✅ Results

| Metric         | Graduate | Dropout |
|----------------|----------|---------|
| **Precision**  | 92%      | 89%     |
| **Recall**     | 81%      | 95%     |
| **F1 Score**   | 86%      | 92%     |

- **Accuracy**: 90%
- **AUC Score**: 0.92
- High recall for Dropout class = valuable for early intervention
- Low false negative rate = fewer missed at-risk students

## 📈 Key Visuals

- Confusion matrix heatmap
- ROC curve
- Top 10 feature importances

> Academic performance (semester grades), tuition payment status, and scholarship indicators were the top predictors of dropout risk.

## 🔍 Limitations & Future Work

- Time-series data would improve trajectory modeling
- Exploring other models: Random Forests, XGBoost
- Including psychological/engagement data could deepen insights
- Extend to multiclass classification with “Enrolled” status
- Test model with real-time or cross-institutional data

## 📁 File Structure
decision-tree/
├── decision_tree_model.ipynb # Jupyter notebook with full analysis, preprocessing, and model
├── README.md # This file – project overview and documentation
├── README.docx # Full report with visuals and extended explanations
├── data/ # Dataset folder (cleaned or raw CSVs go here)
│ └── student_data.csv
├── charts/ # Visual outputs (confusion matrix, ROC curve, etc.)
│ ├── confusion_matrix.png
│ ├── roc_curve.png
│ └── feature_importance.png

## ▶️ How to Run

1. Open `decision_tree_model.ipynb` in Jupyter or VS Code
2. Run all cells to reproduce the preprocessing, model training, and evaluation
3. Visual outputs will be saved in the `charts/` folder

## 🧠 Author

**Toshia Lockhart**  
Aspiring Data Scientist | Passionate about education analytics and machine learning

🔗 [LinkedIn](https://www.linkedin.com/in/toshialockhart)  
📂 [GitHub: tbear13](https://github.com/tbear13)

## 📚 References

- National Center for Education Statistics. (2023). [Undergraduate retention and graduation rates](https://nces.ed.gov/programs/coe/indicator_ctr.asp)
- [Kaggle Dataset](https://www.kaggle.com/datasets/thedevastator/higher-education-predictors-of-student-retention)
