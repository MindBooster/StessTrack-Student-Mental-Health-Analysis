# **StressTrack: Student Mental Health Analysis Using Hybrid Modeling (FCM & KNN)**

## **Project Overview**
StressTrack is a machine learning project aimed at analyzing and predicting student mental health patterns using a hybrid approach. By combining **Fuzzy C-Means (FCM) clustering** and **K-Nearest Neighbors (KNN) classification**, the project identifies students who are likely to seek specialist mental health treatment based on their attributes such as **age**, **CGPA**, and mental health indicators (e.g., depression, anxiety, panic attacks).

The project leverages clustering to derive valuable insights into student groups (e.g., high-risk, moderate-risk clusters) and uses these insights as enriched features in the classification model, significantly improving predictive accuracy.

---

## **Objective**
1. Analyze student mental health patterns to group them into clusters based on mental health characteristics.
2. Predict whether a student seeks specialist treatment using enriched features derived from cluster memberships.
3. Provide actionable insights to stakeholders, such as universities and counselors, to identify at-risk students and allocate resources effectively.

---

## **Methodology**
The project is divided into the following key steps:

### 1. **Data Preprocessing**
- Handled missing values and imbalanced classes.
- Normalized numerical features (e.g., `Age`, `CGPA`) using MinMaxScaler.
- Encoded categorical variables using Label Encoding and One-Hot Encoding.

### 2. **Fuzzy C-Means Clustering (FCM)**
- Clustered students into groups based on mental health indicators (e.g., depression, anxiety, panic attacks).
- Derived soft cluster memberships for each student, indicating the degree of belonging to each cluster.

### 3. **Feature Enrichment**
- Incorporated FCM membership values into the dataset as additional features to enhance the classification model.

### 4. **K-Nearest Neighbors (KNN) Classification**
- Trained the KNN model on the enriched dataset to predict whether students sought specialist treatment.
- Used GridSearchCV with cross-validation to find the optimal `k` value for the KNN model.

### 5. **Evaluation**
- Compared model performance with and without cluster membership features.
- Evaluated using metrics such as **precision**, **recall**, **F1-score**, and **accuracy**.

### 6. **Visualization**
- Visualized cluster membership and predictions using scatterplots.
- Analyzed cluster risk levels with radar charts to understand the impact of mental health characteristics.

---

## **Results**
1. **Improved Model Performance**:
   - Adding FCM membership values as features significantly improved the prediction for the minority class (students seeking treatment).
   - Accuracy improved from **87%** (without cluster memberships) to **97%** (with cluster memberships).

2. **Cluster Insights**:
   - Identified high-risk clusters with high levels of depression, anxiety, and panic attacks.
   - Students in high-risk clusters were more likely to seek specialist treatment.

3. **Actionable Insights**:
   - Highlighted patterns in student behavior and provided a framework for targeted mental health interventions.

---

## **Technologies Used**
- **Programming Language**: Python
- **Libraries**:
  - `scikit-learn`: For preprocessing, model building, and evaluation.
  - `scikit-fuzzy`: For Fuzzy C-Means clustering.
  - `pandas`: For data manipulation.
  - `matplotlib` and `seaborn`: For data visualization.
  - `NumPy`: For numerical operations.

---

## **How to Use**
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/StressTrack.git
   ```
2. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```
3. **Run the Code**:
   - Open the Jupyter Notebook or Python script.
   - Execute the code step-by-step to preprocess data, train the model, and visualize results.

4. **Customize**:
   - Replace the dataset (`Student Mental Health.csv`) with your own data for similar analyses.
   - Modify the clustering and classification parameters to experiment with different configurations.

---

## **Folder Structure**
```
StessTrack-Student-Mental-Health-Analysis/
|
├── StressTrack_SMHA_Project.ipynb  # Jupyter Notebook with code
├── Student Mental Health.csv   # Dataset used in the project         
├── StressTrack_ Student Mental Health Analysis.pptx   # Presentation ppt of the project
├── requirements.txt               # Python dependencies
└── README.md                      # Project documentation
```

---

## **Key Features**
- **Hybrid Model**:
  - Combines clustering (FCM) with classification (KNN) for enhanced performance.
- **Cluster Risk Analysis**:
  - Identifies high-risk groups and visualizes their mental health profiles.
- **Predictive Insights**:
  - Accurately predicts students likely to seek specialist treatment, aiding early intervention.

---

## **Future Scope**
1. **Dynamic Recommendations**:
   - Build a recommendation system for personalized mental health support.
2. **Additional Features**:
   - Include external factors (e.g., socioeconomic data, lifestyle habits) for more robust predictions.
3. **Scalable Models**:
   - Implement the model on larger datasets to generalize insights across institutions.

---

## **Contributors**
- [Sanjana Das](https://github.com/MindBooster)

Feel free to contribute or raise issues for further enhancements!
