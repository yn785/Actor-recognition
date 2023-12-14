# Celebrity Face Recognition Project
- This was created for Finetuning Purposes
## Overview

This project is aimed at building a celebrity face recognition model using a pre-trained VGG16 neural network architecture. The model is designed to recognize faces of various celebrities and is trained on a dataset carefully split into training, validation, and test sets to ensure a balanced representation of each celebrity.

## Dataset

The dataset consists of RGB images of celebrities, with each celebrity having 60 images. The dataset is split into three subsets:

- Training Set: 80% of the data, 48 images per celebrity for training.
- Validation Set: 10% of the data, containing 6 images per celebrity for validation purposes.
- Test Set: 10% of the data, with 6 images per celebrity for final testing.

This balanced distribution aims to ensure that the model generalizes well across all celebrities.

## Model Architecture

The base model is VGG16 with the last layer removed, and a new fully connected layer is added to match the number of classes, corresponding to the number of celebrities in the dataset.

## Training

The model is trained using early stopping with a patience of 5 on the validation loss and a batch size = 8. After 12 epochs, the training process stopped with a validation loss of 2.5913.

## Evaluation

The model's performance is evaluated on both the validation and test sets. The precision, recall, and F1 score on the test set are as follows:
Test Data:
"""
- Precision: 0.566695
- Recall: 0.532703
- F1 Score: 0.529164
- accuracy: 0.532703
"""
These metrics provide insights into the model's ability to correctly identify celebrities on unseen data.

## Overfitting

The model performance on the training set indicates overfitting, as the accuracy on the training set is 1. This suggests that the model has memorized the training data and may not generalize well to new, unseen data.


## Future Improvements

- Investigate overfitting issues and explore regularization techniques.
- Experiment with different neural network architectures to enhance model performance.
- Augment the dataset to increase the model's robustness.
