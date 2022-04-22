# Classifying Creditworthiness of Borrowers

*Module 12 Challenge Assignment*

---

## Overview of the Analysis
---
  In order to classify the creditworthiness of borrowers and potential borrowers, this logistic regression model makes predictions using two versions of a dataset. We compare the predictions made using original imbalenced dataset, which is made up of of historical lending activity from a peer-to-peer lending services company, and one that we have altered from the original using the RandomOversampler module from the imbalanced-learn library to be balanced. The original dataset is imbalanced becuase healthy loans greatly outnumber risky loans. The model was tested on both datasets to see if the imbalance changes the model's predictions on whether or not a potential borrower will default on their loan. 

  First the data was seperated in to "labels" and "features". The label is the variable we are interested in making predictions about, in this case, loan status. The features are the remianing categories of information in the dataset. A logistic regression model was created using the LogisticRegression module from the scikit-learn library to make predictions on new data about potential borrowers. It was tested on historical data so that its accuracy may be assessed. The testing data was then resampled using the RandomOversampler module from the imbalanced-learn library, and the model was fit to that new dataset. The model again made predictions, this time on the resampled data, and the accuracy of those predictions was assessed. 


## Results
---
Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models.

* Machine Learning Model 1 - trained on the original dataset:
  * The model's accuracy was assessed to be 95%, the average precision was 99%, and the average recall was 99%.
  * Precision for healthy loans was 100%, and for unhealthy loans it was 85%.
  * Recall for healthy loans was 99%, and for unhealthy loans it was 91%.
    

* Machine Learning Model 2 - trained on the resampled dataset:
  * The model's accuracy was assessed to be 99%, the average precision was 99%, and the average recall was 99%.
  * Precision for healthy loans was 100%, and for unhealthy loans it was 84%.
  * Recall for healthy loans was 99%, and for unhealthy loans it was also 99%.
    

## Summary
---
Given the improvement in all but one category, I would recommend that Model #2 be used. It showed improvement in its accuarcy score, and maintained its recall score. The precision for unhealthy loans only dropped by 1% compared to Model #1, while the accuracy score improved by 4%. While it is most important to accurately predict which loans will become unhealthy loans, I don't beleive that the 1% drop in precision for unhealthy loans is reason enough to disregard the improvement in overall accuracy for Model #2 as compared to Model #1.


![lr_model](/Images/lr_model.jpg)
![original results](/Images/original_results.jpg)
![oversampler](/Images/oversampler.jpg)
![resampled results](/Images/resampled_results.jpg)


---

## Technologies

The application is written in Python using Pandas
The following packages are used:

Pandas - to write and run the program [Pandas documentation](https://pandas.pydata.org/docs/)

NumPy - for mathematical functions [NumPy documentation](https://numpy.org/doc/)

Pathlib - to create file paths [Pathlib documentation](https://docs.python.org/3/library/pathlib.html)

SciKit-Learn (Metrics) - to generate accuracy scores and confusion matrices [SciKit Learn documentation](https://scikit-learn.org/stable/modules/model_evaluation.html)

Imbalanced-Learn (Metrics) - to genewrate classification reports - [Imbalanced-Learn documentation](https://imbalanced-learn.org/stable/)

datetime - to standardize the format of dates - [datetime documentation](https://docs.python.org/3/library/datetime.html)


---

## Installation Guide

Install the Pandas package using the following command: 'import pandas as pd'

Install the numpy library using the following command: 'import numpy as np'

Install the Pathlib module using the following command: 'from pathlib import Path'

Install the SciKit-Learn metrics libraries using the following commands: 'from sklearn.metrics import balanced_accuracy_score',
'from sklearn.metrics import confusion_matrix'

Install the Imbalanced-Learn library using the following command: 'from imblearn.metrics import classification_report_imbalanced'

Install the warnings library using the following commands: 'import warnings', 'warnings.filterwarnings('ignore')'




--- 

## Usage

To run this program, clone the repository onto your computer, navigate to its source folder in your terminal and launch it using the command 'jupyter lab' then either run the entire program at once, or run the cells individually (in order) as you move through the file.

---

## Contributors
Susannah Slocum 
suzyslocum@gmail.com

---

## License

None
