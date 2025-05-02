# 🚀 CPE393-model-monitoring
Student ID:64070501005 - CPE393 MLOps assignment for monitoring model performance and data drift on airline delay dataset using EvidentlyAI. Includes Random Forest model, prediction simulation (Q1 vs Q2), and automated report generation.

This report compares the model performance between **reference period (Q1)** and **current period (Q2)** using the EvidentlyAI framework.

# ✈️ Discussion
## 📊 Model Performance Summary

| Metric     | Reference (Q1) | Current (Q2) | Change |
|------------|----------------|--------------|--------|
| Accuracy   | 0.835          | 0.834        | ⬇️ -0.001 |
| Precision  | 0.893          | 0.895        | ⬆️ +0.002 |
| Recall     | 0.846          | 0.835        | ⬇️ -0.011 |
| F1 Score   | 0.869          | 0.864        | ⬇️ -0.005 |
| ROC AUC    | 0.911          | 0.910        | ⬇️ -0.001 |
| Log Loss   | 0.356          | 0.361        | ⬆️ +0.005 |

🔹 **Observation**: The model shows consistent performance across quarters with slight variations. The recall dropped slightly, suggesting fewer delayed flights were correctly identified in Q2.

## 🧩 Classification Quality by Label

| Metric     | Label 1 (Delayed) - Q1 | Label 1 (Delayed) - Q2 |
|------------|------------------------|-------------------------|
| Precision  | 0.893                  | 0.895                   |
| Recall     | 0.846                  | 0.835                   |
| F1 Score   | 0.869                  | 0.864                   |

✅ High precision means the model rarely triggers false alarms.  
⚠️ Slight decrease in recall suggests a minor drop in sensitivity.



## 🔍 Confusion Matrix Highlights

- False Positives increased in the current period.
- True Positives decreased slightly.
- The model continues to favor precision over recall.



## 📈 Precision-Recall Curve Insights

At top 10% of prediction confidence:
- Precision is **99.9%**
- Recall is **~15%**
- This confirms the model is well-calibrated and effective for **early warning systems** (e.g., flagging high-probability delays).



## 📌 Summary

- Model remains stable across Q1 and Q2.
- Minor degradation in recall and log loss.
- Slight trade-off between recall and log loss may imply changes in data distribution or class imbalance in Q2.
- Still highly usable for production

