# Deep Learning for Computer Vision
This is the courseworks of deep learning for computer vision provided in Columbia University, including lectures, homeworks and my notes.

You may add your issues for me and we can grow together.

[DL for CV Website](https://www.deeplearningforcomputervision.com/home/deep-learning-for-computer-vision)

[Slack](https://app.slack.com/client/TMZ6V7B5K/DMLKZQWCS)

### Deep Learning for Computer Vision

#### URL: [deeplearning4cv.slack.com](https://deeplearning4cv.slack.com/)

#### Email: qw2261@columbia.edu



## [Lecture 1](https://www.deeplearningforcomputervision.com/uploads/9/6/6/6/96660590/lecture_1.pdf): An Introduction to Old-School Computer Vision

## [Lecture 2](https://www.deeplearningforcomputervision.com/uploads/9/6/6/6/96660590/lecture_2.pdf): Introduction to Old-School Machine Learning

## [Lecture 3](https://www.deeplearningforcomputervision.com/uploads/9/6/6/6/96660590/lecture_3.pdf): Probability, Bayes Theorem and Bayes Classification

## [Lecture 4](https://www.deeplearningforcomputervision.com/uploads/9/6/6/6/96660590/lecture_2.pdf): Introduction to Python and Numpy

## [Lecture 5](https://www.deeplearningforcomputervision.com/uploads/9/6/6/6/96660590/lecture_4_corrected.pdf): High-Dim Feature Spaces, Curse of Dimensionality, Gradient Descent, SVMs 

## [Lecture 6](https://www.deeplearningforcomputervision.com/uploads/9/6/6/6/96660590/lecture_5_corrected.pdf): Logistic Regression, Computational Graphs, Backpropagation 

## [Lecture 7](https://www.deeplearningforcomputervision.com/uploads/9/6/6/6/96660590/lecture_7.pdf): Universal Approximation Theorem, More Hidden Units, Multi-Class Classifiers, Softmax, and Regularization

### 1. Universal Approximation Theorem

A feedforward neural network with a linear output layer and one or more hidden layers with ReLU **[Leshno et al. ’93]**, or sigmoid or some other “squashing” activation function **[Hornik et al. ’89, Cybenko ’89]** can approximate any continuous function on a closed and bounded subset of Rn. This holds for functions mapping finite dimensional discrete spaces as well.

### 2. Caveats

- Optimization may fail to find the parameters needed represent the desired function.
- Training might choose the wrong function due to overfitting. 
- The network required to approximate this function might be so large as to be infeasible.

### 3. Multi-Class Classification

- In general you only need n - 1 discriminate functions. But in practice, it is simpler to use nand train n **one-vs-all** classifiers.

- In the binary case, we used a logistic sigmoid function to assign probabilities to the predictions:  $P (y = 1|x)$
- In the multi-class, $P(y=i|x) = \frac{e^{z_{i}}}{\sum_{j}{e^{z_{j}}}}$ , Softmax

![](/Users/wangqi/Desktop/Courses/2019下半年/DeepLearning4CV/Graphs/Loss Layer.png)

![](/Users/wangqi/Desktop/Courses/2019下半年/DeepLearning4CV/Graphs/softmax loss layer.png)

### 4. Regularization

#### L2 Regularization

![](/Users/wangqi/Desktop/Courses/2019下半年/DeepLearning4CV/Graphs/l2.png)

![](/Users/wangqi/Desktop/Courses/2019下半年/DeepLearning4CV/Graphs/Frobenius norm.png)

#### L1 Regularization

![](/Users/wangqi/Desktop/Courses/2019下半年/DeepLearning4CV/Graphs/l1.png)





- L1 produces solutions that are sparse compared L2.
- This means most weights are driven to zero. Why? The gradient of this regularizer does not flatten out as it approaches zero and pushes unneeded weights down.

- This can be used as a method of feature selection.

