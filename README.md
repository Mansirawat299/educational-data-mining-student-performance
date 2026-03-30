# 🎓 Educational Data Mining - Early Student Performance Prediction

**Early prediction of final grades (A–F) using only behavioral and demographic features — before any mid-term exams.**

This project develops a complete, actionable early-warning system that helps teachers identify at-risk students and provide personalized recommendations using only early-semester data.

---

## ✨ Key Features

- **Truly Early Prediction**: No mid-term or subject scores used
- **Six-Class Grading System**: Predicts fine-grained grades **A, B, C, D, E, F**
- **Feature Engineering**: `effective_study_time = study_hours × (attendance_percentage / 100)`
- **Student Clustering**: KMeans with silhouette score optimization
- **Advanced Modeling**: Global Ensemble Regression (RF + GB + XGBoost) → Hybrid Classifier → Ordinal Probability Boosting
- **Practical Dashboard**: Risk levels (High/Medium/Low) + personalized actionable recommendations
- **Strong Results**: **84.60% hold-out test accuracy** with macro F1 = 0.85 and excellent F-grade recall (0.87)

---

## 📊 Results

| Model                                      | Accuracy (%) | Macro F1-score |
|--------------------------------------------|--------------|----------------|
| Logistic Regression (Baseline)             | 95.00        | 0.94           |
| K-Nearest Neighbors (Baseline)             | 78.03        | 0.77           |
| Random Forest (Baseline)                   | 99.57        | 0.99           |
| Global Ensemble Regression                 | 77.34        | 0.77           |
| Tuned Hybrid Classifier                    | 91.07        | 0.90           |
| **Ordinal-Probability Boosted Hybrid**     | **84.60**    | **0.85**       |

**Final Model**: 84.60% accuracy on unseen test set (most reliable metric)

---

## 📁 Dataset

- **Name**: `Student_Performance.csv`
- **Records**: 15,000 (after cleaning)
- **Features**: Age, gender, school_type, parent_education, study_hours, attendance_percentage, internet_access, travel_time, extra_activities, study_method
- **Target**: `overall_score` (continuous) → mapped to **A–F grades**

---

## 🛠️ Technologies Used

- Python 3
- scikit-learn
- pandas, numpy
- XGBoost
- mord (Ordinal Logistic Regression)
- matplotlib, seaborn
- Jupyter Notebook

---

