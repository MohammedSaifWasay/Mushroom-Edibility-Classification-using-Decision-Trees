# 🍄 Mushroom Edibility Classification using Decision Trees

This project explores the classification of mushrooms as **edible** or **poisonous** using decision tree algorithms. Using a dataset of various physical and biological mushroom characteristics, we implemented classification models in R, evaluated their performance, and provided insights into feature importance to improve safe foraging decisions.

---

## 📌 Objective

To develop a machine learning model that can accurately classify mushrooms based on physical features such as cap shape, color, odor, and gill attachment.

---

## 📂 Dataset Overview

- **Observations**: Multiple records of mushrooms
- **Target Variable**: `class` (Edible or Poisonous)
- **Features**: Categorical variables such as:
  - `cap.shape`, `cap.color`, `odor`
  - `gill.attachment`, `spore.print.color`
  - And several other morphological traits

---

## 🧪 Methodology

### 1. 📥 Data Collection and Preparation
- Imported the dataset using `readxl`
- Removed redundant columns (e.g., `veil.type`)
- Ensured dataset was clean (no missing values)
- Converted appropriate features for analysis

### 2. 📊 Exploratory Data Analysis (EDA)
- Cross-tabulated features against class labels
- Visualized relationships between features and edibility using `ggplot2`
- Key Findings:
  - Odor is a strong predictor of edibility
  - Cap color and shape showed distinct trends for certain classes
  - Gill attachment had notable distribution differences

### 3. 🌲 Model Building (Decision Tree)
- Used `rpart` for recursive partitioning
- Applied a **penalty matrix** to emphasize false negatives (classifying poisonous mushrooms as edible)
- Performed model pruning using optimal CP value
- Visualized decision tree with `rpart.plot`

### 4. ✅ Model Evaluation
- Created confusion matrix to measure accuracy
- Evaluated ROC Curve and AUC score
- Key metrics:
  - High accuracy
  - Good balance between precision and recall

---

## 📈 Key Insights

| Feature         | Insight                                                                 |
|----------------|-------------------------------------------------------------------------|
| `odor`         | Absence of odor strongly linked with edibility                         |
| `cap.shape`    | Certain shapes more likely found in edible species                     |
| `cap.color`    | Red/purple found only in edible, while brown/white common to both      |
| `gill.attachment` | Attached gills were more common in edible mushrooms                  |

---

## 🔮 Future Work

- 🔁 Implement k-fold cross-validation for generalization
- 🤖 Try additional models: Random Forest, SVM, Gradient Boosting
- 🧪 Hyperparameter tuning via grid search
- 📊 Add environmental data for richer feature context (e.g., soil type, moisture)

---

## 📚 References

- [An Introduction to R - CRAN Documentation](https://cran.r-project.org/doc/manuals/r-release/R-intro.html)
- [Mastering R Visualizations (Albusairi, 2023)](https://www.linkedin.com/pulse/mastering-simple-r-visualizations-from-scatterplots-heat-albusairi/)

---

## 🧠 Author
**Mohammed Saif Wasay**  
*Data Analytics Graduate — Northeastern University*  
*Machine Learning Enthusiast | Passionate about turning data into insights*

🔗 [Connect with me on LinkedIn](https://www.linkedin.com/in/mohammed-saif-wasay-4b3b64199/)
