Automated Classification Engine: Botanical Product Taxonomy

📌 Executive Summary
This project provides an automated machine learning solution for classifying physical products based on their dimensional attributes. By leveraging ensemble learning and decision tree algorithms, this engine eliminates manual sorting processes and provides a highly accurate, scalable framework for product categorization.

The current implementation analyzes the physical measurements (length and width) of botanical variants to predict their exact taxonomic class, achieving 100% classification accuracy on test data.

🎯 Business Impact
Process Automation: Replaces manual classification with a predictive model, significantly reducing quality control time.

Scalability: The model successfully handles augmented datasets (tested on 10,000+ records) without performance degradation.

Stakeholder Transparency: In addition to a high-performance ensemble model, a pruned decision tree was developed to provide clear, human-readable business rules for how classifications are made.

🛠️ Tech Stack & Tools
Language: Python

Data Manipulation: pandas, numpy

Machine Learning: scikit-learn (BaggingClassifier, DecisionTreeClassifier)

Data Visualization: matplotlib (Tree logic visualization)

📊 Methodology
1. Data Processing & Augmentation
Ingested baseline dimensional data (sepal.length, sepal.width, petal.length, petal.width).

Performed data augmentation via random sampling with replacement to scale the dataset to 10,000 records, ensuring robust model training and stress-testing.

Partitioned data into a 70/30 Train/Test split for objective evaluation.

2. Model Development
Two distinct modeling strategies were implemented to balance raw performance with business interpretability:

Ensemble Model (Bagging Classifier): Built a forest of 100 base estimators using bootstrapping. This method reduced variance and prevented overfitting, ultimately capturing the complex dimensional relationships.

Interpretable Model (Decision Tree): Developed a single Decision Tree Classifier pruned to a max_depth of 4 using the Gini impurity criterion. This guarantees that the classification logic can be easily explained to non-technical stakeholders.

3. Performance & Evaluation
Accuracy: The Bagging Classifier achieved an exact 1.0 (100%) accuracy score on the 30% holdout test data (3,000 records).

Confusion Matrix: The model successfully categorized all three product classes with zero false positives or false negatives.

Visual Output: Generated a comprehensive decision tree plot to map out the exact conditional splits driving the predictions.
