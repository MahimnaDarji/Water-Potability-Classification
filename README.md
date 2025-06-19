# 💧 Water Potability Classification

This project investigates the classification of water samples as potable (safe to drink) or non-potable based on various chemical and physical attributes. A variety of supervised learning models, interpretability techniques, and validation strategies are used to evaluate model performance and derive insights from the dataset.

---

## 🔍 Project Objectives

- Clean and prepare the water potability dataset.  
- Explore feature distributions and their relationship with water safety.  
- Train and compare multiple machine learning classifiers.  
- Use model interpretability tools (SHAP, PDP) to identify influential features.  
- Evaluate generalization through cross-validation and scenario-based analysis.

---

## 🛠 Methods and Workflow

### 1. Data Preprocessing
- Handled missing values in `ph`, `Sulfate`, and `Trihalomethanes` using median imputation.  
- Verified feature distributions and potability class balance.

### 2. Exploratory Data Analysis
- Used boxplots to explore feature behavior across potable vs. non-potable classes.  
- Generated correlation heatmaps to identify linear relationships.

### 3. Model Training
Trained the following classification models:
- Random Forest  
- Logistic Regression  
- Support Vector Machine (SVM)  
- K-Nearest Neighbors (KNN)  
- Decision Tree  
- Gradient Boosting  

Each model was evaluated on an 80/20 train-test split with classification reports and performance visualizations.

### 4. Model Interpretability
- Computed feature importance from tree-based models and logistic regression coefficients.  
- Applied **SHAP (SHapley Additive exPlanations)** for the Random Forest to understand local and global feature contributions.

### 5. Dimensionality Reduction
- Used **Principal Component Analysis (PCA)** for feature space visualization and to assess redundancy.

### 6. ROC Curve Comparison
- Plotted **ROC curves** for all classifiers to compare their ability to separate classes.

### 7. Cross-Validation
- Employed **Stratified K-Fold Cross-Validation** to evaluate model consistency across different data folds.

### 8. Custom Feature Engineering & Retraining
- Created additional feature combinations based on domain logic.  
- Retrained top-performing models on the engineered feature set for performance improvements.

### 9. Clustering and Segmentation
- Performed **Hierarchical Clustering** to detect natural groupings of water samples.  
- Used dendrograms to visualize clustering structures.

### 10. Scenario Analysis
- Developed **Scenario Comparison Plots** to analyze model predictions across edge cases and borderline instances.

### 11. Partial Dependence Plots (PDP)
- Generated **Partial Dependence Plots** to visualize marginal effects of key features on the probability of water being potable.

---

## 💡 Key Takeaways

- Tree-based models (Random Forest, Gradient Boosting) were the most interpretable and reliable classifiers.  
- Chemical properties like `Solids`, `Sulfate`, and `Organic_carbon` were the most influential in predicting potability.  
- Interpretability techniques provided actionable insights that go beyond accuracy scores.
