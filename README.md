# Object detection with Faster R-CNN 

Faster R-CNN is a method for object detection that uses region proposal. Here, we apply Faster R-CNN pre-trained on the coco dataset. 
- Load Pre-trained Faster R-CNN 
- Object Localization
- Object Detection 
We detect several objects by name and use the corresponding likelihood


## R-CNN

Faster R-CNN is a deep convolution network for object detection. It is an extension of Fast-CNN, faster thanks to the Region Proposal Network (RPN).


Traditional object detection technique follows a pipeline of 3 steps 
- Region Proposal Generator
- Feature Extraction
- Classification

In 2014, R-CNN extracts the features using a CNN. It relies on Selective Search algorithm for generating region proposals and SVM algorithm to classify the regions. It cannot be trained end-to-end as it is composed of several modules.

Fast R-CNN builds upon R-CNN, it's a single module and it uses the entire image as input to the CNN and computing the feature maps only once. The region proposals are then generated based on these feature maps, and the proposed regions are aligned with the feature maps using a RoI pooling layer. Fully connected layers to classify the object and refine the bounding box coordinates.

Faster R-CNN uses a RPN. The Region Proposal Network is a fully convolutional network that takes an image as input and outputs a set of rectangular object proposals, each with an objectness score.

## Training for object detection

Training in Object Detection has two objectives: we have to determine the learnable parameters for the box and we have to determine the bounding boxes class. In order to determine the learnable parameters for the bounding box, we use the L2 or squared loss. This is used to find the difference between real value predictions. The L2 Loss Function calculates squared differences between the actual box value and the predicted box, where we have the box and the L2 Loss for each coordinate of the box.

Multitask Loss = L2 Loss + Cross entropy

## Resources

- [Introduction to computer vision](https://www.coursera.org/learn/introduction-computer-vision-watson-opencv/home/week/1)
- [Faster R-CNN: Towards Real-Time Object Detection with Region Proposal Networks](https://arxiv.org/abs/1506.01497?utm_medium=Exinfluencer&utm_source=Exinfluencer&utm_content=000026UJ&utm_term=10006555&utm_id=NA-SkillsNetwork-Channel-SkillsNetworkCoursesIBMDeveloperSkillsNetworkCV0101ENCoursera25797139-2021-01-01)
- [Faster R-CNN Explained for Object Detection Tasks](https://blog.paperspace.com/faster-r-cnn-explained-object-detection/)



