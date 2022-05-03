### EX NO: 03
### DATE: 25-04-2022
# <p align="center">MULTI CLASS CLASSIFICATION</p>
## AIM:

To write a python program to implement the multi class classification algorithm .

## Equipments Required:

1. Hardware – PCs

2. Anaconda – Python 3.7 Installation / Moodle-Code Runner / Google Colab.

# Concept:

• In Multi Class Classification, multiple class labels are present in the dataset.

• The number of classifier models depends on the classification technique we are 
  applying to. 

• One vs. All: N-class instances then N binary classifier models.

• One vs. One: N-class instances then N* (N 1)/2 binary classifier models.

• The Confusion matrix is easy to derive but complex to understand.

• Example : Check whether the fruit is apple, banana, or orange.

Popular algorithms that can be used for multi-class classification include: 

k-Nearest Neighbors. 

Decision Trees. 

Naive Bayes. 

Random Forest. 

Gradient Boosting. 

## Libraries Used in the program:

# NUMPY
NumPy is a library for the Python programming language, adding support for large, 
multidimensional arrays and matrices, along with a large collection of high-level 
mathematical functions to operate on these arrays. 
# SKLEARN
Scikit-learn is a free software machine learning library for the Python programming 
language. It features various classification, regression and clustering algorithms including 
support-vector machines. 
# MATPLOTLIB
Matplotlib is a plotting library for the Python programming language and its numerical 
mathematics extension NumPy. It provides an object-oriented API for embedding plots into 
applications using general purpose GUI toolkits like Tkinter, wxPython, Qt, or GTK
# Counter
Counter tool to easily count words in a document or two. It also works well with pandas data
frames, allowing us to make simple comparisons.
## Algorithm
1. Start the program. 

2. Import libraries required as per requirement. 

3. Define dataset use the make_blobs() function to generate a synthetic multi -class 
   classification dataset. 

4. summarize dataset shape . 

5. summarize observations by class label. 

6. summarize first few examples. 

7. plot the dataset and color the by class label. 

8. stop the program

# Program:
/* 
Program to implement the multi class classifier. 

Developed by: U. VIVEK KRISHNA

RegisterNumber: 212219040180

*/

from numpy import where

from collections import Counter

from sklearn.datasets import make_blobs

from matplotlib import pyplot

X, y = make_blobs(n_samples=1000, centers=3, random_state=1)

print(X.shape, y.shape)

counter = Counter(y)

print(counter)

for i in range(10):
	print(X[i], y[i])

for label, _ in counter.items():
	row_ix = where(y == label)[0]
	pyplot.scatter(X[row_ix, 0], X[row_ix, 1], label=str(label))

pyplot.legend()

pyplot.show()

# Output:
![Output - Multi Class Classification](https://user-images.githubusercontent.com/63917883/166463897-3609f570-29e0-4a01-b7d3-b021c2d54397.png)

# Result:
Thus the python program to implement the multi class classification was implemented successfully.
