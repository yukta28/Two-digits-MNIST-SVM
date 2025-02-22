# Two-digits-MNIST-SVM
Two-digits MNIST
# Problem Statement
The goal here is to build a linear Support Vector Machine (SVM) classifier using Scikit-Learn’s SGDClassifier. We aim to apply this classifier to a subset of the handwritten digit dataset (MNIST) by selecting any two digits and treating the problem as a binary classification task. In particular, we choose two digits (for example, digits 3 and 8) and use the hinge loss function with L2 regularization. The classifier’s performance is evaluated in terms of classification accuracy and the confusion matrix.
#Approach
Data Preparation:
Dataset: We have to use the MNIST dataset loaded with load_digits() from Scikit-Learn.
Binary Subset: I filtered the dataset to keep only two chosen digits (e.g., 3 and 8).
Label Conversion: The selected digits are converted into binary labels (e.g., label 0 for digit 3 and label 1 for digit 8).
Model:
Classifier: I used Scikit-Learn’s SGDClassifier with loss='hinge' (linear SVM) and penalty='l2' for regularization.
Training: The classifier is trained using the training portion of the data.
Evaluation: After training, I evaluated the model by predicting on the test set and computing the accuracy and confusion matrix.


#Discussion & Conclusion
Key Observations: 
High Accuracy (98.61%)
The classifier effectively distinguishes between digits 3 and 8, making only one misclassification.

Confusion Matrix Analysis
41 correct classifications of '3' (True Negative).
30 correct classifications of '8' (True Positive).
1 instance where '3' was misclassified as '8' (False Positive).
0 instances where '8' was misclassified as '3' (False Negative).

# Interpretation
The model rarely misclassifies but may occasionally confuse a digit with similar features.
Advantages of Using SVM:
Effective for small datasets like MNIST.
Robust to high-dimensional data, as pixels are used as features.
Margin Maximization improves generalization.

# Limitations & Future Work
Scalability: Linear SVMs may struggle with larger datasets like full MNIST (10 classes) or CIFAR-100.
Feature Engineering: Feature extraction techniques (e.g., PCA, HOG features) could further improve classification.
Kernel SVM: Using non-linear kernels (e.g., RBF Kernel) might perform better for more complex datasets.

# Conclusion
The linear SVM model successfully classifies handwritten digits with high accuracy and minimal misclassification. Future enhancements can explore feature extraction methods or deep learning approaches to further improve performance.
