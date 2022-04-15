# Neural_Style_Transfer with Pytorch

In this project, we implement an image style transfering system using convolutional neural networks. 

We are given two images: content image and style image. Our goal is to extract the style features from the style image and transfer them to the content image. 

The project is based on the following paper:

Gatys, Leon A., Alexander S. Ecker, and Matthias Bethge. "[Image style transfer using convolutional neural networks.](https://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/Gatys_Image_Style_Transfer_CVPR_2016_paper.pdf)" Proceedings of the IEEE conference on computer vision and pattern recognition. 2016.

The neural network used in this project is based on [VGG-19](https://arxiv.org/pdf/1409.1556.pdf) network. As we use Pytorch for our neural network training, we can access the pretrained VGG-19 model as follows

```
from torchvision import models

models.vgg19(pretrained=True).features
```

Below are a sample content (left) and style (right) images: 
<p align="center">
<img width="598" alt="sample" src="https://user-images.githubusercontent.com/37718565/162112643-cafca78d-d92e-4907-8172-4c29f3e36098.png">
</p>

After training the network, the resulting image would be:
<p align="center">
<img width="255" alt="sample result" src="https://user-images.githubusercontent.com/37718565/162112875-2254b4a2-a413-49f8-85fd-0b1bef823cd4.png">
</p>
This shows that the features of the style image is transferred to the original image. 

To write this code, I used the instructions in ["Deep Learning with PyTorch : Neural Style Transfer"](https://www.coursera.org/projects/deep-learning-with-pytorch-neural-style-transfer) project. 
