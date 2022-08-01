# Blind source separation

## Task
The purpose of the project is to separate an image obtained as a sum of a two images into its components.
The two images img1 and img2 summed together come from different dataset: mnist and fashion_mnist, respectively.
No pre processing is performed. 

## U-Net
This repo contains two versions of Unet. First Version of Unet first version is a Semi Siamese Unet where data are encoded via an encoder and two decodings are performed, one per image.  Second version instead of having two decoders, trying to see this task as a two-labels image segmentation. The resulting model will be much slimmer, as it has only one decoder instead of two. Last convolutional layer has been modified to output two channels (the two images). These will be then concatenated along the width to get an image of the desired shape (32, 64, 1).
## Results
The respective metrics used to compare the two implemented versions of unet are MSE and standard deviation.

