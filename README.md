# tensorflow segmentation
Here is my first version in segmented prediction.

Using U-net for Medical Segmentation.
The paper is from https://arxiv.org/pdf/1505.04597.pdf

![image](https://user-images.githubusercontent.com/33461503/122873769-5e735200-d35c-11eb-9c03-ec3099519c9d.png)


The image-mask dataset was augmented with opencv, pillow ans scikit image. The images were augmented by adjusting the brightness, contrast (using opencv), log value (darkness adjustment - using scikit image), whereas the masks were dilated using pillow in order to get more information in the images.

Some comments of improvement:
- The model is improved if I combine between residual block and unet. 
- The resblock is inserted in each left-side unet block to keep boundary original features.
- Skip connection at the triangle bottom can be used 3-4 residual blocks.
