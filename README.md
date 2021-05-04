# Unit 11—Risky Business
*by Arzu Isik Topbas*

In this assignment, I built and evaluated several machine-learning models to predict credit risk using free data from LendingClub. Credit risk is an inherently imbalanced classification problem , so I used different techniques for training and evaluating models with imbalanced classes. I used the imbalanced-learn and Scikit-learn libraries to build and evaluate models using resampling and ensembling learning techniques.

---

## 1 - Resampling

I used the *imbalanced learn* library to resample the LendingClub data and built and evaluated logistic regression classifiers using the resampled data.

### 1.1 - Oversample

In this section, you compared two oversampling algorithms to determine which algorithm results in the best performance. You will oversample the data using **the Naive Random Oversampling** algorithm and **the SMOTE Oversampling** algorithm. 

#### 1.1.1 - Naive Random Oversampling 

* balanced accuracy score = 0.65
* recall score            = 0.65
* geometric mean score    = 0.65

#### 1.1.2 - SMOTE Oversampling 

* balanced accuracy score = 0.64
* recall score            = 0.57
* geometric mean score    = 0.63

### 1.2 - Undersample 

In this section, I tested an undersampling algorithms - **the Cluster Centroids algorithm** - to determine which algorithm results in the best performance compared to the oversampling algorithms above.

#### 1.2.1 - Cluster Centroids algorithm

* balanced accuracy score = 0.78
* recall score            = 0.77
* geometric mean score    = 0.78

### 1.3 - Combination (Over and Under) Sampling

In this section, I tested a **combination Over- and Under-Sampling** algorithm to determine if the algorithm results in the best performance compared to the other sampling algorithms above by using **the SMOTEENN** algorithm 

#### 1.3.1 - SMOTEENN

* balanced accuracy score = 0.49
* recall score            = 0.01
* geometric mean score    = 0.08

---

> Which model had the best balanced accuracy score?
* The Cluster Centroids algorithm has the best balanced accuracy score(0.78).
> Which model had the best recall score?
* The Cluster Centroids algorithm has the best recall score(0.77).
> Which model had the best geometric mean score?
* The Cluster Centroids algorithm has the best geometric mean score(0.78).

----

## 2 - Ensemble Learning

I compared two different *ensemble classifiers* to predict loan risk and evaluate each model. I used **the Balanced Random Forest Classifier** and **the Easy Ensemble Classifier**.

### 2.1 - Balanced Random Forest Classifier

* balanced accuracy score = 0.79
* recall score            = 0.91
* geometric mean score    = 0.78
* the top three features  = total_rec_prncp (0.073767), total_rec_int (0.063903), total_pymnt_inv (0.060733)

### 2.1 - Easy Ensemble Classifier

* balanced accuracy score = 0.93
* recall score            = 0.94
* geometric mean score    = 0.93

----
> Which model had the best balanced accuracy score?
* The Easy Ensemble Classifier has the best balanced accuracy score(0.93).
> Which model had the best recall score?
* The Easy Ensemble Classifier has the best recall score(0.94).
> Which model had the best geometric mean score?
* The Easy Ensemble Classifier has the best geometric mean score(0.93).
> What are the top three features?
* total_rec_prncp (0.073767)
* total_rec_int (0.063903)
* total_pymnt_inv (0.060733)
---

