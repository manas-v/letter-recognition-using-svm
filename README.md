# Comparing SVM Kernels performance using Letter Recognition Dataset
## Objective - Letter Recognition using SVM
The objective is to identify each of a large number of black-and-white rectangular pixel displays as one of the 26 capital letters in the English alphabet. The character images were based on 20 different fonts and each letter within these 20 fonts was randomly distorted to produce a file of 20,000 unique stimuli. Each stimulus was converted into 16 primitive numerical attributes (statistical moments and edge counts) which were then scaled to fit into a range of integer values from 0 through 15.

## About the Dataset
The Dataset was obtained from the UCI Machine Learning Repository(https://archive.ics.uci.edu/ml/datasets/letter+recognition)
Each row in the data set represents an image of a handwritten alphabet, as shown in figure 1(A). Using some basic image processing, the images are converted into m X n pixels (figure 1(B)), where m and n depend on the size and resolution of the original image. Each pixel contains numeric values, with higher values denoting the presence of dense 'ink'. In the pixels where nothing is written, the pixel value is 0.

A pixel is called 'on' if it contains to a positive numeric value, else it is called 'off'.

Using the pixelated images, 16 features are derived for each image, such as the width of the box, the ratio of the mean variance of x divided by the width of the box, etc.

![image](https://user-images.githubusercontent.com/59551550/105849541-8907eb80-6006-11eb-8182-4c41e5fdb5a4.png)

## Attribute Information
1. lettr capital letter (26 values from A to Z)
2. x-box horizontal position of box (integer)
3. y-box vertical position of box (integer)
4. width width of box (integer)
5. high height of box (integer)
6. onpix total # on pixels (integer)
7. x-bar mean x of on pixels in box (integer)
8. y-bar mean y of on pixels in box (integer)
9. x2bar mean x variance (integer)
10. y2bar mean y variance (integer)
11. xybar mean x y correlation (integer)
12. x2ybr mean of x * x * y (integer)
13. xy2br mean of x * y * y (integer)
14. x-ege mean edge count left to right (integer)
15. xegvy correlation of x-ege with y (integer)
16. y-ege mean edge count bottom to top (integer)
17. yegvx correlation of y-ege with x (integer)

## Structure of the Data
Here the average of all attributes for the 26 letters are plotted in the form of a heatmap.

![image](https://user-images.githubusercontent.com/59551550/105850388-a8ebdf00-6007-11eb-9fa4-f9feae3d0d50.png)

## Classification
### Support Vector Machine(SVM)
Support vector machines (SVMs) are a set of supervised learning methods used for classification, regression and outliers detection.
Support Vector Classifier or SVC is capable of classification using multiple kernels (Different Kernel functions can be specified for the decision function). Common kernels are provided, but it is also possible to specify custom kernels. The four inbuilt kernels provided for classification are ‘linear’, ‘poly’, ‘rbf’(default), ‘sigmoid’.
### SVC using PyKernels
PyKernels is a python library for working with kernel methods in machine learning. It provides implementations of various kernel functions ranging from typical linear, polynomial or rbf ones through wawelet, fourier transformations, kernels for binary sequences and even kernels for labeled graphs.

The ten kernels used in this project are:
* Linear Kernel
* RBF Kernel
* Polynomial Kernel
* Sigmoid Kernel
* Cossim Kernel
* InverseMultiquadratic Kernel
* Laplacian Kernel
* Log Kernel
* TStudent Kernel
* ANOVA Kernel

## Comparing Kernel Performance
In the experiment the performance of 10 kernels is compared the results of which are as follows

![image](https://user-images.githubusercontent.com/59551550/105850618-f700e280-6007-11eb-9d31-5a4e3afeb438.png)
