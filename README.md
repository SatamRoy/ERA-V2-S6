# ERA-V2-S6
## S6 - Assignment

* Added Excel file with the formulas and calculatiosn
* Added word document with explantaion of major steps
* following is the imgae with screenshot ![Screenshot](https://github.com/SatamRoy/ERA-V2-S6/blob/main/S6%20-%20Assignment%20-BP_page-0001.jpg)


# ERA-V2-S6 - CNN Model Explanation 
The architecture of the NN Model is as follows:
1.	Convolutional Layers:
o	Convolutional layers (Conv2d) are used for feature extraction in image data.
o	The first convolutional layer (conv1) takes a single-channel input (like grayscale images) and produces 32 output channels.
o	The second convolutional layer (conv2) also has 32 output channels.
o	The third convolutional layer (conv3) produces 20 output channels.
2.	Activation Function:
o	After each convolutional layer, the ReLU activation function is applied. It introduces non-linearity to the model.
3.	Normalization:
o	Batch normalization (BatchNorm2d) is used to stabilize training by normalizing the input to each layer.
o	It helps improve convergence and generalization.
4.	Pooling Layers:
o	Max pooling (MaxPool2d) reduces the spatial dimensions of the feature maps.
o	It selects the maximum value from a local region (e.g., 2x2) and downsamples the feature map.
5.	Dropout:
o	Dropout (dropout1) randomly sets a fraction of input units to zero during training.
o	It prevents overfitting by encouraging the network to learn robust features.
6.	Global Average Pooling:
o	The global_avg_pool operation computes the average value of each feature map.
o	It reduces the spatial dimensions to a single value per channel.
7.	Final Output:
o	The last convolutional layer (conv4) produces 10 output channels.
o	The output is reshaped (x.view(-1, 10)) to match the desired output size.
o	Finally, the log_softmax function is applied to obtain the log probabilities of different classes.
