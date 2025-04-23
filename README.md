# Leukemia Detection Using Random Forest (Tabular Data)
This project builds a machine learning model using Random Forest to detect leukemia based on blood cell data. It uses a tabular dataset (not image-based) and aims to achieve more than 90 percent accuracy.

What This Project Does
This project:

Uses a balanced synthetic dataset (same number of leukemia and non-leukemia samples)

Preprocesses the data (scaling, train-test split)

Uses Random Forest for classification

Tunes the model using Grid Search to find the best hyperparameters

Evaluates the model using accuracy, confusion matrix, and classification report

Shows which features are most important using a feature importance chart

Step-by-Step Process
1. Load the Dataset
We load the dataset named balanced_leukemia_dataset.csv into a pandas DataFrame.

2. Prepare Features and Labels
We separate the features (X) from the label (y), where Leukemia is the target column.

3. Split the Data
We split the data into training and testing sets:

75 percent for training

25 percent for testing

stratify=y ensures equal distribution of classes in both sets

4. Standardize the Features
We use StandardScaler to scale the features so that all values have a similar range. This is important for many models to perform well.

5. Train a Random Forest Model
We use RandomForestClassifier, which is a group of decision trees. It works well for classification problems.

6. Hyperparameter Tuning with Grid Search
We use GridSearchCV to try different combinations of parameters. For example:

Try 100 trees with max depth of 5 and min split of 2

Try 200 trees with max depth of 10 and min split of 5

It tries many such combinations and picks the best one

These are the parameters we tune:

n_estimators: Number of trees

max_depth: How deep the trees can go

min_samples_split: Minimum number of samples required to split a node

7. Evaluate the Model
We evaluate the final model using:

Accuracy score: How often the model is correct

Confusion matrix: Shows how many 0s and 1s were predicted correctly or wrongly

Classification report: Includes precision, recall, and F1-score

8. Feature Importance
We visualize which features had the most influence in making predictions.
