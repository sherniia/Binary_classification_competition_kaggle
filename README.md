# Kaggle Competition: Playground Series - Season 3, Episode 23
## Binary Classification with a Software Defects Dataset
### Project By: Aiastan Sherniiazov
### Special Thanks: Ambrosm for the exemplary notebook and guidance

---

## 🌐 Introduction

This repository contains my implementation and findings for one of my first Kaggle competitions. The challenge involved binary classification with a software defects dataset. The competition provided an excellent learning curve for mastering machine learning algorithms, ensemble methods, and effective cross-validation techniques.

---

## 🛠️ Technologies Used

- Python
- scikit-learn
- LightGBM
- CatBoost
- XGBoost
- StratifiedKFold for cross-validation

---

## 📚 Dataset

- **Number of Rows**: 101,763
- **Features**: All numerical
- **Missing Values**: None
- **Duplicates**: None
- **Class Imbalance**: Present but managed through StratifiedKFold

---

## 🔍 Exploratory Data Analysis (EDA)

The dataset required minimal cleaning, having no missing values or duplicate rows. The EDA confirmed an imbalance in the target class distribution. Initially, SMOTE was considered for upsampling the minority class but ultimately deemed unnecessary due to the sufficient dataset size and the use of StratifiedKFold for cross-validation.

---

## 🎛️ Hyperparameter Tuning

Key hyperparameters for HistGradientBoostingClassifier, LGBClassifier, CatBoost, ETClassifier, and XGB were finely tuned for better performance.

---

## 🤖 Model Ensemble

The final ensemble model comprised the following six classifiers:

1. HistGradientBoostingClassifier
2. LGBClassifier
3. CatBoost
4. ETClassifier
5. XGB
6. Logistic Regression with Kernel Approximation

---

## 📊 Results & Observations

- Adding Random Forest to the ensemble had a negligible impact on performance.
- Incorporating CatBoost improved the model's AUC score by 0.007—a considerable increase.
- The highest-performing individual model (XGB) during training received the lowest weight in the ensemble, while the lowest-performing model (Logistic Regression) surprisingly received the highest weight.

---

## 🏆 Competition Performance

- **Final AUC Score on Test Data**: 0.79356
- **Ranking**: 299 out of 1702 teams
- **Percentile**: Top 20%

---

## 👏 Acknowledgements

Huge thanks to Ambrosm for sharing his code and providing invaluable guidance. His contributions significantly enhanced my understanding of ensemble modeling.

---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

---
