# SVM Parameter Tuning Project

## Assignment Goal

The goal of this assignment is to find the best SVM (Support Vector Machine) model for classifying data from the Wine dataset. We try different values for the SVM parameters and compare how well they work.

---

## Dataset Used

- **Name:** Wine Dataset  
- **Source:** UCI Machine Learning Repository  
- **Total Samples:** 178  
- **Features:** 13 numeric features  
- **Target Classes:** 3 different wine types  

---

## Steps Followed

1. The dataset is split into training and testing sets using 10 different random seeds.  
2. For each sample:
   - 70% of the data is used for training, and 30% for testing.
   - We try different values for these SVM parameters:
     - **kernel:** linear, rbf, poly, sigmoid
     - **C:** 0.1, 1, 10
     - **gamma:** scale, auto
   - We use **GridSearchCV** to test all combinations and pick the best one.
3. We record the best accuracy and the best parameters for each sample.
4. For the sample with the highest accuracy, we also show how the model improved during training using a convergence graph.

---

## Results Table

| Sample # | Best Accuracy (%) | Best SVM Parameters (Kernel, C, Gamma) |
|----------|-------------------|----------------------------------------|
| S1       | 96.30             | linear, C=0.1, gamma=scale             |
| S2       | 96.30             | linear, C=1, gamma=scale               |
| S3       | 88.89             | linear, C=0.1, gamma=scale             |
| S4       | 98.15             | linear, C=0.1, gamma=scale             |
| S5       | 92.59             | linear, C=0.1, gamma=scale             |
| S6       | 98.15             | poly, C=0.1, gamma=auto                |
| S7       | 96.30             | linear, C=0.1, gamma=scale             |
| S8       | 94.44             | linear, C=0.1, gamma=scale             |
| S9       | 98.15             | linear, C=1, gamma=scale               |
| S10      | 85.19             | linear, C=0.1, gamma=scale             |

---

## Convergence Graph

We also created a graph that shows how the model's accuracy changed while it was testing different parameter combinations.  
This graph is for the sample that gave the highest accuracy.




