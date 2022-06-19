# My Final project 👻
Introduction：
I prefer to focus on the practicality of the project, so my final project aims to optimize CNN classification based on imageclassifier that we learned in class and train a simple convolutional neural network (CNN) to classify cifar images. Replace more complex data sets, and "expand" the training set to solve the problem of overfitting.
<br>reference：<br>
https://git.arts.ac.uk/rfiebrink/ExploringMachineIntelligence_Spring2022/blob/main/week2/ImageClassifier.ipynb<br>
https://www.tensorflow.org/tutorials/images/

# File description: <br>
My project contains two code files: compare and modified.<br>
Compared is a training model based on imageclassifier to replace cifar100.
Modified is the optimization model code to solve the above overfitting problem.<br>
👇here are very clear explanations and comments on the production process in the code. Please check them!!!
Link:https://github.com/RayWangRui/Coding3_ML/tree/main/最终项目<br>

# My Ideas🤖

<img width="639" alt="截屏2022-06-19 下午6 20 44" src="https://user-images.githubusercontent.com/91971211/174492914-6010fa9b-e915-4bc4-96a0-226ec3a1838c.png">
First of all, in order to make the task more challenging, I chose the cifar100 dataset, which is a relatively complex dataset and not so easy to train. It has 100 classes, which is much more difficult than MNIST or cifar10.<br>
Link: http://www.cs.toronto.edu/~kriz/cifar.html<br>
<img width="467" alt="截屏2022-06-19 下午3 43 29" src="https://user-images.githubusercontent.com/91971211/174486669-6a4ca715-962e-4a95-870d-c1e72284244b.png"><br>
This dataset is just like the CIFAR-10, except it has 100 classes containing 600 images each.  There are 500 training images and 100 testing images per class.  The 100 classes in the CIFAR-100 are grouped into 20 superclasses.  Each image comes with a "fine" label (the class to which it belongs) and a "coarse" label (the superclass to which it belongs)
<br>

<br><br>I use the methods given in the imageclassifier we learned in class to train directly. From the training results, we can see that the accuracy of the training set is much higher than that of the test set. I learned that the reason for this phenomenon is called overfitting, which is that the network is too adapted to the training set and the test set results are too poor. This model is too suitable for the training set and ignores other data sets, such as the test data set.
<img width="742" alt="截屏2022-06-19 下午6 23 20" src="https://user-images.githubusercontent.com/91971211/174493017-f8f6950e-6e62-4fd3-ae3c-4f30e2250264.png">

In order to solve the problem of overfitting, I used two methods. 

<img width="558" alt="截屏2022-06-19 下午6 29 56" src="https://user-images.githubusercontent.com/91971211/174493277-732e8201-e939-44b0-b7bb-32083ec7c89e.png">
One is to use data augmentation, that is, to randomly change the image input into the neural network to prevent the neural network from adapting to the training set too much, which can also play the role of "expanding" the training set. After loading the dataset, I chose several data enhancement methods, including resizing, random cropping, and random brightness. I map these methods to the original dataset to make the dataset more diverse. 

<img width="614" alt="截屏2022-06-19 下午6 27 00" src="https://user-images.githubusercontent.com/91971211/174493180-d2a0dcce-c3e0-4768-b995-1aa7cb8c8805.png">
The other is a dropout. Dropout will randomly change some parameters stretching into the network to 0, which also has the effect of restraining the overfitting of the neural network. In fact, the accuracy of the test set is even higher than that of the training set, and the method is effective.

<img width="808" alt="截屏2022-06-19 下午6 30 32" src="https://user-images.githubusercontent.com/91971211/174493291-f849e9c7-4be8-42fb-b5e2-4902ea09f915.png">

Finally, I want to analyze why the accuracy can not be further improved. I think it is because the model is too simple. If you want to further improve, you should change to a more complex model on the premise of solving the overfitting problem.
<br>
# Video Link:

