# Transfer_learning for High-Resolution image

*Transfer learning* is an essential tool in deep learning to solve the fundamental training problems of *insufficient training data* 
and *limited computational support*. It tries to transfer the knowledge from the *source domain* to the *target domain* by relaxing 
the assumption that the training data and the test data should be similar. The pre-trained weights on open source database for the 
classic CNN architectures, such as *VGG16*, *ResNet50*, *InceptionNetV3*，can be easily achieved, and we choose the weights trained 
from *’ImageNet’* database, one of the standard image database, as the one used in transfer learning.


## Visualization in CNN
According to the research on the visualization in convolutional networks by Zeiler et al.[7]: 
* Filters in the former layers:   
Recognize colors and certain horizontal and vertical lines
* Filters in the next few layers:  
Recognize trivial shapes using the lines and colors learned in the previous layers
* Filters in the subsequent layers:  
Identify textures and parts of objects
* Filters in the final layers: 
Get activated by whole objects


## Transfer Learning Structure for High-resolution images
High-resolution image is much larger than the normal input size （<img src="http://latex.codecogs.com/gif.latex?224 \times 224" border="0"/>）of CNNs.
One possible way to handle this challenge of high-resolution image input is to stack the additional convolutional layers after the normal ConvNet, 
