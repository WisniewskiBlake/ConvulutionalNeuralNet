Conulutional Neural Networks are widely used to images and videos. The one I built here solves an image classification problem
where the goal is to take in images and classify them as either Cat or Dog. This is a broad conulutional neural network. If the
CNN was fed images of the human brain, one with tumors and one without, it would be able to distinguish if a brain has a tumor or
not.

First, this is a sequential classification problem, so we define our classifier as sequential. That means our problem can 
be solved using a sequence of layers. Next, we add a convulutional layer. This is the first step in the order: Conv. Layer->Max
Pooling->Flattening->Full Connection. In the convulution layer, I create 32 feature detectors, which will in turn create 32 feature
maps. Feature detectors are essentially filters that are applied to the image. Each feature detector I created has 3 rows and 3
columns. The input shape is the shape of the input image which I use to apply the feature detectors through the convulution
operation. Specification of the input shape will format the pictures in such a way that 32 detectors can be used evenly on
all of them.

The pooling step is an easy to understand one. All that happens here is reduction of the size of the feature maps created in
the convulution step. In pooling, the feature map is scanned with a 2x2 square and the maximum number inside of each square is
copied to the pooled feature map. Taking the max number is called max pooling.

Next, I add another convulutional layer. Then I begin flattening, which is the process of taking all the pooled feature maps and
putting them into one vector. This vector will be the future input layer of the ANN in step 4: full connection.

The last step is to make a classic ANN that is composed of fully connected layers. Since I already have the input layer from
flattening, all I need to do is create a hidden layer, or fully connected layer. The Dense function is used to add a fully
connected layer.
