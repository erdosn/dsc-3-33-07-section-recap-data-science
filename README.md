
# Section Recap

## Introduction

This short lesson summarizes key takeaways from section 33.

## Objectives
You will be able to:
* Understand and explain what was covered in this section
* Understand and explain why this section will help you become a data scientist

## Key Takeaways

The key takeaways from this section include:
* Support Vector Machines can be used for regression tasks, although they're better known as a powerful algorithm for classification.
* SVMs optimize for maximizing the margin between the decision boundary and the nearest data points (the support vectors)
* For data that isn't linearly seperable (no single straight line will correctly classify all of the observations into the correct categpries) a soft margin classifier can be used to allow for a model that may mis-classify some of the training data points
* You can improve the performance of your SVMs for data sets where a linear decision boundary isn't very useful by using the kernel trick
* With the kernel trick, you project your data set into a higher dimensional space 
* The Gaussian/Radial Basis Function (RBF) kernel provides you with tro hyper parameters - C and Gamma
* C allows you to trade off between misclassification of the training set and simplicity of the decision function (to avoid overfitting). It's common to all kernels
* Gamma allows you to define how much influence a single training example has
* The polynomial kernel is specified as $$(\gamma \langle  x -  x' \rangle+r)^d $$
* The sigmoid kernel is specified as $$\tanh ( \gamma\langle  x -  x' \rangle+r) $$
* Based on the "no free lunch" theorum, there's no kernel that is guaranteed to be better for a given training set than others, but the RBF kernel is often a good default to start with
* in Scikit-learn, the SVC method is one classifier supporting multiple kernels. It takes C as the penalty parameter and additional kernel specific parameters such as degree (for polynomail) and gamma (for RBF, polynomial and sigmoid) https://scikit-learn.org/stable/modules/generated/sklearn.svm.SVC.html
* There are other implementations of SVM built into Scikit-learn. For example:
    * NuSVC introduces $\nu$ (pronounced "nu") creates an upper bound on training errors and a lower bound on support vectors
    * LinearSVC is a "one-vs-rest" method which often scales better for cases with many potential classes 

