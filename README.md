## Fraud Detection: Model Performance Summary

### **1. AUC on the Test Set: 0.9641**
- The model achieved an AUC of 0.9641, indicating a strong capability to distinguish between fraudulent and non-fraudulent transactions. Although slightly lower than previous results, the AUC reflects effective performance in separating these classes within the Fraud Detection dataset.

### **2. Precision, Recall, and F1-Score for Class 0 (Non-Fraud):**
- **Precision:** 1.00 (100%)
- **Recall:** 1.00 (100%)
- **F1-Score:** 1.00 (100%)
- The model demonstrates perfect accuracy in identifying non-fraudulent transactions. Given the significant imbalance in the Fraud Detection dataset, where the majority of transactions are non-fraudulent, this result is expected.

### **3. Precision, Recall, and F1-Score for Class 1 (Fraud):**
- **Precision:** 0.87 (87%)
  - Precision improved to 87%, indicating that 87% of transactions predicted as fraudulent were indeed fraudulent. This improvement is crucial in reducing false positives within the Fraud Detection system, thereby minimizing unnecessary investigations.
- **Recall:** 0.84 (84%)
  - Recall remains robust at 84%, meaning the model correctly identifies 84% of fraudulent transactions. This slight decrease in recall reflects a trade-off, as precision has increased, but the model continues to capture the majority of fraud cases.
- **F1-Score:** 0.85 (85%)
  - The F1-Score improved to 0.85, reflecting a better balance between precision and recall. This balance is critical for the Fraud Detection model, ensuring reliable identification of fraudulent transactions while minimizing false positives.

### **4. Global Metrics:**
- **Accuracy:** 1.00 (100%)
  - Overall accuracy remains very high, which is expected given the imbalance in the Fraud Detection dataset. However, the model's performance on the minority class (fraud) provides a more meaningful assessment of its effectiveness.
- **Macro Avg and Weighted Avg:**
  - The macro and weighted averages indicate an improved balance in performance across both classes. The high values in these metrics confirm that the model is effectively handling both majority and minority classes within the Fraud Detection context.

### **Conclusions and Considerations:**

- The updated model in the Fraud Detection project shows a significant improvement in balancing precision and recall for fraud detection. The enhanced precision reduces the number of false positives, which is vital for the operational efficiency of the Fraud Detection system.
- The new hyperparameters, including a deeper tree structure and a slightly higher learning rate, have contributed to these improvements. The model now benefits from more complex decision boundaries and stronger regularization.
- These results indicate that the model is well-suited for real-world fraud detection applications, where minimizing false alarms and accurately capturing fraudulent transactions are essential.
- While the current model performs strongly, further exploration of advanced techniques, such as ensemble methods or additional feature engineering, could lead to even better results in the Fraud Detection project.

### Dataset Information

The data used in this project can be downloaded from the following link on Kaggle: [Credit Card Fraud Detection Dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud).

This dataset contains transactions made by credit cards in September 2013 by European cardholders. The dataset presents a highly imbalanced class distribution, with only a small percentage of transactions labeled as fraudulent.

### **Best Hyperparameters:**
```json
{
    'n_estimators': 463,
    'learning_rate': 0.03173132760152346,
    'max_depth': 10,
    'subsample': 0.9451586859466636,
    'colsample_bytree': 0.5477628758346557,
    'gamma': 3.1188250719555723
}

