# Binary_classification_model_for_a_mobile_carrier
## Introduction to Machine Learning course project from Practicum by Yandex

### Goal

Develop a binary classification model for Megaline, a mobile carrier, that would analyze subscribers' behavior and recommend one of Megaline's newer plans: Smart or Ultra.

### This project's repo includes the following files:

- The project's jupyter notebook (Binary_classification_model_for_a_mobile_carrier.ipynb);
- A pdf format of the notebook (Binary_classification_model_for_a_mobile_carrier.pdf);
- Input data (users_behavior.csv);
- Project description from Practicum (Intro_to_ML_project_description.pdf).

### This project includes the following steps:

1. Descriptive statistics;
2. Data Preprocessing: missing values and duplicates check;
3. EDA: outliers and target variable analysis;
4. Splitting data into train, validation and test sets;
5. Features standard scaling;
6. Models' hyperparameters tuning;
7. Model selection;
8. Retrain the best tuned model on the whole training set and test it on the test set;
9.  Sanity check.

### Based on the analysis we have come to the following conclusions:

- The number of outliers is not significant. We decided to keep the data as is and if necessary revisit this section after modeling;
- Most features' distribution is  close to normal, there is only slight deviation from it (except for `messages`). We tried to correct this by applying standard scaling before modeling;
- We noticed that our target classes are imbalanced: there are at least twice as many observations for the "Smart" than for the "Ultra" plan. Imbalanced classifications pose a challenge for predictive modeling as most of the machine learning algorithms used for classification were designed around the assumption of an equal number of examples for each class. We have tried to correct this issue in the later sections by using the `stratify` parameter. It makes a split so that the proportion of values in the sample produced will be the same as the proportion of values in the target variable. 

In the next step we have **tuned 3 learning algorithms to achieve the highest possible validation accuracy** and thus select the best model. **Random Forest model** showed the highest score (76.89). Then we have retrained this model on the whole training set (including validation set) and tested it with the test set that our model didn't see before. We have reached **81.34% accuracy on the test set**. 

Finally, we have checked our model for **sanity** by comparing the final score to the baseline accuracy. The final accuracy of our model is much higher (12.5%) than the baseline accuracy that we would get if instead of classifying we simply predicted majority class target value for each new observation.

### The logbook of this project can be found [here](https://docs.google.com/spreadsheets/d/1SrGdReexaSEomJGS6yR6cRwJtHA_XqpprnLaE7B6Ayg/edit#gid=100076621) (Intro to ML tab).
Total time spent on the project: 6.7 hours with a daily average of 2.17 hours working for 4 days.
