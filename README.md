Machine Learning Project  
Comparative Analysis of Linear Regression and K-Nearest Neighbors (KNN) for Rock VS Mine Classification

### 1. Introduction

This project looks at the Rock vs Mine Classification Problem using sonar signal reflections. The aim is to determine if an object detected by sonar sound waves is a **Rock (R)** or a **Mine (M)**. This is a classic supervised machine learning problem.

This study compares two machine learning algorithms, **Linear Regression** and **K-Nearest Neighbors (KNN)**, using the same dataset. Both algorithms undergo identical preprocessing and evaluation steps to allow for a fair comparison. The project examines how they differ in behavior, accuracy, ease of understanding, computational cost, and their suitability for real-world classification tasks.

This analysis shows how two different supervised learning methods perform on the same non-linear signal dataset and identifies when to use each algorithm.

### 1.1 Dataset Source  
Dataset: **Sonar Target Classification Dataset (Rock vs Mine)**  
Link: **https://www.kaggle.com/datasets/mahmudulhaqueshawon/sonar-data**

This dataset has 208 samples. Each sample includes **60 sonar frequency energy values** obtained from bouncing sonar signals off a surface. The label indicates if the response pattern is a **Rock (R)** or a **Metal Mine (M)**. This dataset is valuable for evaluating binary classification.

### 1.2 Steps to Implement Linear Regression (Normal Method)
- Import libraries and load dataset  
- Perform basic preprocessing and label conversion  
- Split data into train and test sets  
- Fit the Linear Regression model  
- Make predictions using the test data  
- Evaluate the model using MSE, MAE, and RMSE  
- Plot the ROC Curve and Confusion Matrix  
- Interpret linear fitting in relation to dataset complexity

### 1.3 Steps to Implement K-Nearest Neighbors (KNN)
- Import libraries and load dataset  
- Preprocess the data and apply Feature Scaling  
- Split data into train and test sets  
- Choose K value for tuning  
- Train the KNN Model  
- Make predictions using the test data  
- Evaluate using Accuracy, Precision, Recall, and F1 Score  
- Plot the Decision Boundary, Confusion Matrix, and Accuracy vs K  
- Analyze the effect of neighborhood and non-linearity
  
---

### 2. Objective

The aim of this project is to:
- Build and evaluate Linear Regression and KNN models.
- Assess their performance using accuracy as the main measure.
- Visualize model behavior with graphical representations.
- Form conclusions and offer suggestions based on the findings.

---

### 3. Model 1: Linear Regression

Linear Regression is a parametric supervised learning algorithm that predicts a continuous outcome based on one or more independent variables. It assumes a straight-line relationship between the input features and the output variable.

Key Points:
- Model Type: Supervised (Regression)
- Nature: Parametric and Analytical
- Learning Approach: Minimizes the sum of squared differences to find the best fitting line.
- Accuracy Achieved: 88 percent

Performance Summary:
- Works well when data shows a clear linear trend.
- Quick in training and making predictions.
- Easy to understand and mathematically clear.
- Lacks flexibility in capturing non-linear relationships.

Visualization Summary:
-Confusion Matrix showing how correct and incorrect predictions are spread across classes.
-ROC Curve illustrating the balance between sensitivity and specificity.
-AUC Score indicating the overall classification performance of the model.
<img width="683" height="547" alt="download (4)" src="https://github.com/user-attachments/assets/6605449f-2db0-47ca-8a27-5b47ab0e1423" />
<img width="578" height="455" alt="download (5)" src="https://github.com/user-attachments/assets/a4851215-6204-4ae2-953d-ee5843044d8c" />

---

### 4. Model 2: K-Nearest Neighbors (KNN)

KNN is a non-parametric, instance-based learning algorithm used for classification and regression. It predicts the output based on the similarities between feature points in the training data, measured by distances like Euclidean distance.

Key Points:
- Model Type: Supervised (Classification/Regression)
- Nature: Non-parametric, Lazy Learning
- Learning Approach: Predicts outcomes based on the majority or average of nearest neighbors.
- Accuracy Achieved: 95 percent

Performance Summary:
- Works well with non-linear and complex datasets.
- Requires proper feature scaling.
- Can be slow with large datasets.
- Sensitive to the choice of 'k' and noise in the data.

Visualization Summary:
- Decision Boundary Plot showing how the algorithm divides the feature space.
- Confusion Matrix displaying true and false predictions.
- Accuracy vs K Plot illustrating how accuracy changes with different neighbor values.
  <img width="855" height="547" alt="download (6)" src="https://github.com/user-attachments/assets/1eed87f6-e438-4130-a4e8-5414522f0110" />
  <img width="653" height="547" alt="download (7)" src="https://github.com/user-attachments/assets/b6175841-21d0-485c-9d49-d6a3ffbb44db" />



---

### 5. Comparative Analysis

| Aspect                    | Linear Regression        | K-Nearest Neighbors |
|--------                   |-------------------       |---------------------|
| Model Type                | Parametric               | Non-parametric |
| Learning Style            | Analytical               | Instance-based |
| Accuracy                  | 88%                      | 95% |
| Best Suited For           | Linear data              | Non-linear data |
| Training Speed            | Very fast                | Slower |
| Prediction Speed          | Very fast                | Slower due to distance calculation |
| Interpretability          | High                     | Moderate |
| Scalability               | High                     | Moderate |
| Overfitting Risk          | Moderate                 | High for small k |
| Feature Scaling Dependency| Low                      | High |
| Complexity                | O(n)                     | O(n × k) |
| Visualization Simplicity  | Simple regression line   | Complex decision boundary |

---

### 6. Results and Discussion

The analysis shows that both algorithms have strengths depending on the dataset.

Linear Regression reached an accuracy of 88 percent. It trained efficiently, is easy to interpret, and performed consistently on linear datasets. However, it struggles with complex non-linear data where the relationship between features and the target variable isn't strictly linear.

K-Nearest Neighbors achieved an accuracy of 95 percent. It performed better than Linear Regression because it effectively models non-linear relationships. Still, its computational demands and sensitivity to the value of k make it less suitable for very large datasets unless optimized.

The comparative visualizations and metrics show that KNN provides better prediction accuracy, while Linear Regression is faster and easier to understand.

---

### 7. Visualization and Insights

Model 1: Linear Regression  
- Confusion Matrix showing how correct and incorrect predictions are spread across classes.
- ROC Curve illustrating the balance between sensitivity and specificity.
- AUC Score indicating the overall classification performance of the model.

Model 2: K-Nearest Neighbors  
- Decision boundary plot illustrating neighborhood influence.  
- Confusion matrix to show classification performance.  
- Accuracy vs K graph showing how model tuning affects accuracy.

These visualizations help illustrate model bias, variance, and overall reliability. The KNN plots reveal adaptable decision boundaries, while regression plots focus on linear relationships.

---

### 8. Extended Comparative Analysis with Metrics

 Linear Regression Metrics
- Mean Squared Error (MSE): 0.1190  
- Mean Absolute Error (MAE): 0.1190  
- Root Mean Squared Error (RMSE): 0.3450  
 K-Nearest Neighbors Metrics
- Accuracy: 0.9524  
- F1 Score: 0.9521  
- Precision: 0.9563  
- Recall: 0.9524  

Interpretation
The quantitative comparison confirms that KNN outperforms Linear Regression in terms of predictive accuracy and overall classification capability.  
While Linear Regression maintains lower continuous error values (MSE/MAE), KNN demonstrates superior F1 Score, Precision, and Recall, making it more reliable for final classification predictions.  

Linear Regression is preferable when simplicity, interpretability, and fast computation are required.  
KNN is ideal for datasets with non-linear relationships and achieves higher accuracy when tuned properly.


---

### 9. Conclusion

This study concludes that both Linear Regression and KNN are effective algorithms with unique strengths.

Linear Regression, with an accuracy of 88 percent, stands out for its simplicity, speed, and interpretability. It works best for datasets that show linear patterns.

KNN, with an accuracy of 95 percent, better adapts to complex and non-linear data. However, it requires more computational power and careful tuning.

KNN outperforms Linear Regression by 7 percent in overall accuracy, which stresses the importance of matching the chosen model to the data's nature and complexity rather than just its popularity.

---

### 10. Project Structure(sonar.csv)
├── ML_FINAL_PRJ.ipynb -> Model 1: Linear Regression
├── ML_PRJ_MODEL2.ipynb -> Model 2: K-Nearest Neighbors
└── README.md -> Report and Comparative Documentation
  
### 11. Future Enhancements

- Include cross-validation techniques to improve accuracy evaluation.
- Use feature selection and dimensionality reduction methods (PCA, LDA).
- Expand the study to include Random Forest, SVM, and Neural Networks.
- Create a Streamlit-based web interface for interactive visualization and prediction.
- Improve KNN using KD-Tree or Ball-Tree implementation for large datasets.

### 12. Author Details

Name: Vedant Lokhande  
Organization: Symbiosis Institute of Technology  
Location: Nagpur, Maharashtra, India  
Field of Work: Artificial Intelligence, Data Science, IoT, Financial Engineering  
Date: October 2025  

### 13. Final Remark

The comparative analysis shows that no single algorithm is universally better. The effectiveness of a model depends on the problem structure, dataset characteristics, and computational limits. A balanced evaluation of accuracy, interpretability, and scalability is important for choosing the best model for real-world applications.
