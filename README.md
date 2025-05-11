# Brain Stroke Detection using Machine Learning

## Overview
A stroke (cerebrovascular accident or CVA) occurs when the blood flow to a part of the brain is interrupted. Depending on the duration and severity, it can cause irreversible damage or even death. Each year, approximately **15 million people worldwide suffer a stroke** (Clément et al., 2017), with around 5 million deaths and 5 million more left with severe disabilities. According to the World Health Organization, a stroke occurs somewhere in the world every **5 seconds**.

This project applies **machine learning techniques** to predict the occurrence of a stroke based on various patient parameters. It is a **binary classification problem**, where the goal is to predict:

- `1` if a person has suffered a stroke  
- `0` otherwise

---

## Problem Motivation
Several risk factors contribute to the likelihood of a stroke, including:

- High blood pressure  
- Diabetes  
- Obesity  
- Smoking  
- High cholesterol  
*(CDC, 2017)*

Early prediction of strokes can support preventive medical decisions and save lives.

---

## Model Training & Evaluation

Different machine learning models were evaluated, and **Random Forest** proved to be the most effective. Key observations:

- **Highest number of correct predictions** in the confusion matrix  
- **Best average performance** in precision, recall, and F1-score  
- **ROC curve** with the highest AUC (closest to 1)

The model was fine-tuned using **hyperparameter optimization**, initially with Halving Random Search. It became evident that poorly selected parameters could degrade performance. A more informed selection was made based on [Breiman's Random Forest paper (2001)](https://www.stat.berkeley.edu/~breiman/randomforest2001.pdf).

---

## Final Results

After hyperparameter tuning (e.g., `max_depth`, `n_estimators`, `min_samples_split`), the final model achieved:

- ✅ **Accuracy: 96%**  
- 📈 **ROC AUC: 0.99**  
- 📊 **Improved confusion matrix results**  
- 🔁 **2–3% increase** in precision, F1-score, and recall  

---

## Conclusion

The objective of predicting stroke occurrence from patient data was successfully met.

### Key Insights:
- A good classification algorithm like **Random Forest** is effective, but **data quality and preparation are equally important**.
- It was essential to balance the dataset and handle missing values, as about 30% of the entries contained gaps.
- **Tuning hyperparameters** significantly improved model performance.

---

## 📁 Technologies Used

- Python  
- Scikit-learn  
- Pandas / NumPy  
- Matplotlib / Seaborn  
- Jupyter Notebook

---

## References

- Clément, M.E., et al. (2017)  
- CDC (2017)  
- [Breiman, L. (2001) - Random Forests](https://www.stat.berkeley.edu/~breiman/randomforest2001.pdf)

