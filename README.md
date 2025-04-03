# ELE489_HW1
# Wine k-NN Classification Project

## Overview
In this project, I implemented the k-NN algorithm and tested it on the Wine Dataset from the UCI Machine Learning Repository. The dataset contains various chemical properties of wines, and the goal is to predict the class of the wine (class 0, class 1, or class 2) based on these features.

### Distance Metrics Used:
- **Euclidean Distance**
- **Minkowski Distance**
- **Chebyshev Distance**

## Requirements
Make sure to install the following dependencies to run the code:
- `numpy`
- `pandas`
- `scikit-learn`
- `matplotlib`
- `seaborn`

**Description**
I started the implementation by calculating the distances first. I used three different distance metrics. The 
first one was Euclidean distance which is computed by finding the square root of the sum of the squared 
differences between corresponding features of the test and training points. The second one is Minkowski 
distance calculated by taking the absolute difference between the test and training points for each feature, 
raising these differences to the power of p, summing them up, and then taking the p-th root of the total. I 
chose p=4 in my code. As the third one I employed Chebyshev distance which is calculated by taking the 
absolute differences between the test and training points for each feature and then selecting the maximum 
of these absolute differences. Later, I defined a function named NN, which identifies the K nearest 
neighbors by sorting the computed distances and selecting the indices of the smallest K values. After 
identifying the nearest neighbors, the voting() function performs majority voting: it counts how many times 
each label appears in the K nearest neighbors and returns the most common label as the predicted class 
for the test point. Finally, the overall KNN function applies this process iteratively for each test point.  

**Instructions to Run the Code**
Before running the code, the dataset must be uploaded to the same directory as the .py file. You can access the dataset via the link (https://archive.ics.uci.edu/dataset/109/wine)
