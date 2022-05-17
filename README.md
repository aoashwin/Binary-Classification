### EX NO: 2
### DATE: 1/4/2022
# <p align="center">BINARY CLASSIFICATION</p>
## Aim:
To write a python program to perform binary classification.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner /Google Colab

## related Theory Concept:
Binary classification is a form of classification — the process of predicting categorical variables — where the output is restricted to two classes. It is used in many different data science applications, such as Medical Diagnosis, Email analysis, Marketing, etc. For example, in medical diagnosis, a binary classifier for a specific disease could take in symptoms of a patient and predict whether the patient is healthy or has a disease. The possible outcomes of the diagnosis are positive and negative.

## Algorithm
1.define dataset.<br>
2.summarize dataset shape.<br>
3.summarize observations by class label.<br>
4.summarize first few examples.<br>
5.plot the dataset and color the by class label










## <br>Program:
```
Program to implement binary classification.
Developed by: ASHWIN A O 
RegisterNumber: 212220230005
```
```python
from numpy import where
from collections import Counter
from sklearn.datasets import make_blobs
from matplotlib import pyplot

X,y = make_blobs(n_samples=10,centers=2,random_state=1)
print(X.shape,y.shape)
counter=Counter(y)
print(counter)

for i in range(5):
    print(X[i],y[i])
    
for label, _ in counter.items():
    row_ix=where(y==label)[0]
    pyplot.scatter(X[row_ix,0], X[row_ix,1], label=str(label))
pyplot.legend()
pyplot.show()
```

# Output:
#![164031274-ac6ec9ad-aada-4b8a-8484-1ad571cae5f3](https://user-images.githubusercontent.com/75235601/164068954-7eda074e-0483-487c-bc8d-f5d144bb4db8.jpeg)


## Result:
Thus the python program performed binary classification successfully.
