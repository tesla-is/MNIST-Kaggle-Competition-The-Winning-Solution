# MNIST-Kaggle-Competition-The-Winning-Solution
The project provides a step by step guide to solving and winning the MNIST competition on Kaggle. MNIST is a famous computer vision dataset that is often cited as a "Hello World!" for Machine Learning.

In this project I have demonstrated how to step by step design a model to tackle the MNIST challenge.
Download the dataset : https://www.kaggle.com/c/digit-recognizer

A special regard to Francis Chollet (Author of Keras) for writing an amazing book, "Deep Learning with Python".

Let us begin!

![Kaggle](KaggleMNISThist3.png)

I have used the following techniques which will get you a step by step increment on the test set accuracy

1. Random Forest Algorithm (93.5% on the Test set)

A limited parameter (max_depth = 20) ensemble of only 20 Decision Trees (default value is 100) which prevents overfitting and provides satisfactory accuracy on the validation set (around 95%)

2. A Simple Convolutional Neural Network (98.5% on the Test set)

A simple CNN with minimal parameters. No advanced techniques like Batch Normalization, Learning Rate Annealer, or Data Augmentation. The validation accuracy will be around 99.1% (see previous versions of the kernel)

3. CNN with Data Augmentation (99.35% on the Test set)

Apply Data Augmentation on the CNN along with learning rate annealer and Nadam optimizer. The validation accuracy will be around 99.48% at 20 epochs

4. An ensemble of CNNs (99.67% on the Test set)

Combine 7 previously designed CNNs to work on random shuffled subsets of training and validation data. The ensemble technique used is Bagging. The validation accuracy achieved is 99.55%. To touch the test set accuracy mark of 99.7% you just have to increase the number of CNNs in the ensemble

5. An ensemble of CNNs with Batch Normalization and Learning Rate Annealer (99.72% on the Test set)

Use the same CNN architecture but this time introduce a batch normalization layer after convolution. Apply data augmentation to the entire training set and increase the number of epochs.

6. We have used multiple ML and DL algorithms & techniques to touch the golden mark of 99.7%. But the problem is, you still would not win the competition. Because some kagglers have been cheating to get a perfect test score of 100%.

Read this article to know more.

https://www.kaggle.com/c/digit-recognizer/discussion/61480

So how can you cheat and hit the bullseye

Train a model on the entire MNIST dataset (70K images) and then use it to make predictions

A lot of notebooks use an ensemble CNN or simple CNN with the full MNIST dataset for a perfect score.

But wait! If cheating is what you want to do, maybe do it the smart way. Simply use a Decision Tree Algorithm with (max_depth = None). It is in the nature of Decision Trees to overfit the training data. You'll get a perfect score of 100%.

The winning solution is in notebook version 2

Make sure to implement all the versions.

If you find the project useful, please upvote it on Kaggle. My id is mentioned below.

https://www.kaggle.com/captaintyping


