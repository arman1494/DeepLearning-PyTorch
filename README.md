# DeepLearning-PyTorch



Our dataset is downloaded from google derive, which contains 45,000 grayscale 32x32 images. This dataset is categorized as 9 class which were labeled as airplane, automobile, bird, cat, deer, dog, frog, horse and ship and each class has 5000 images, the Fig.3 shows some images. In addition, we have divided our dataset into training set and validation set. Randomly, in each class we get 1000 pics and put it as validation set, now we have a training set with 36,000 images and validation set with 9,000 images.

# Data Augmentation
In this project we proposed random window drop, random horizontal flip, random vertical flip and random rotation
 
# Our Deep Learning Structure

In this project we design an innovative CNN, Firstly, 2 convolutional layers are introduced, and the first layer get the input image. In this layer because of the grey scale images, we have just one input channel and by doing the 64 different masking the number of outputs in this layer is 64. The size of our windows for masking is 3 by 3 and with a padding 1 pixels. The activation operation in this layer is ReLU and it is full connected to second convolutional layer. Then the number of input channels of second convolutional layer is 64. Secondly, the outputs of this layer are forwarded to a max pooling layer. We have done it in two three steps with 2 convolutional networks and a max pooling layer with full connection but at the end we have introduced just one convolutional layer with 512 outputs and one max pooling layer again with full connection. After this we have introduced 2 ReLU activation functions with 20% and 50% percent of dropout respectively. The first activation gets 2048 inputs and produces 100 outputs and the second one gets 100 inputs and produces the 9 outputs which is same with the number of classes.
