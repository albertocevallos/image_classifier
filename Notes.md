## Step 1

First things first, initialize variables for our training and validation data

## Step 2

We'll initialize the type of model using the sequential model function which allows you to build a linear stack of layers. Which creates an object that feeds in to the next.
First layer of a CNN (Convolutional Neural Network) is the convolutional layer. Its a 32 by 32 by 3 array of pixel values. Where 3 refers to RGB values. Each number in the array is given a alue from 0 to 255. This number decribes the pixel intensity at that point.

ON a very high level, the convolutional network analyzes the image starting from the top left corner and updates the weights for a given feature that it is identifying in pattern. The first layer finds lower levels such as lines and curves based on probability, and therefore detecting or not detecting features.

This feature map is put through an activation layer name "relu" or rectified linear unit. Its a non-linear operation that replaces all negative pixel valeus with zero, which increases the non linear properties of the model, allowing the model to learn more complex functions than linear regressions.

We minimiz the loss function (measures differnece between target ouput and expected output) by taking the derivative of the loss in each layer, starting by the last, propagating the loss values backwards, which changes the values of the gradients to decrease our loss function (back propagation). We use "adam" as our optimizer and a sigmoid function to convert the data to probabilities in each class.

