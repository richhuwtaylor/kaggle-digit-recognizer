# kaggle-digit-recognizer

An attempt to solve Kaggle's Digit Recognizer problem using a shallow neural network.

https://www.kaggle.com/richhuwtaylor/digit-recognizer

The model consists of a single hidden layer with 200 hidden units using a ReLU activation function
and an output layer using Softmax. It has no regularisation, but uses the Adam optimiser and trains
on the entire batch.

## About the dataset

The competition's train and test data sets contain gray-scale images of hand-drawn digits, from zero through nine.

Each image is 28 pixels in height and 28 pixels in width, for a total of 784 pixels in total. Each pixel has a single pixel-value associated with it, indicating the lightness or darkness of that pixel, with higher numbers meaning darker. This pixel-value is an integer between 0 and 255, inclusive.

The training data set has 785 columns. The first column, called "label", is the digit that was drawn by the user. The rest of the columns contain the pixel-values of the associated image.

The test data set is the same as the training set, except that it does not contain the "label" column.

This project generates a submission file in the following format: For each of the 28000 images in the test set, output a single line containing the ImageId and the predicted digit.

| ImageId | Label |          
| ------- |-------|
| 1       | 3     |
| 2       | 7     |
| 3       | 8     |
(27997 more lines)

The evaluation metric for the contest is the categorization accuracy, or the proportion of test images that are correctly classified. For example, a categorization accuracy of 0.97 indicates that you have correctly classified all but 3% of the images.