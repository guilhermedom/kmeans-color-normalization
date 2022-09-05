# K-Means Color Normalization

Using [K-Means] to normalize image colors and help in object segmentation tasks.

---

## Problem Overview

Sometimes shadow and illumination can make it hard for machine learning algorithms to correctly find and segment objects in images. Shadow and illumination provide additional information in pixel colors that may confuse algorithms and make them recognize very bright pixels of an object as being part of another object.

[Color normalization] is one of the image processing techniques that can help [image segmentation] algorithms. With color normalization, it is possible to remove intensity-related information from pixels, eliminating shadows and illumination shifts from the image.

## Analysis Introduction

K-Means, as well as other clustering algorithms, can normalize the colors of an image by fitting centers and clusterizing pixels. If we normalize each cluster of pixels according to the cluster center/centroid colors, we can eliminate intensity-related information from the image, simplifying its colors.

Below, we can see a flower image in its original form (top left) being normalized using less and less K-Means clusters (8, 4 and 2 clusters). The bottom right image is the one with the strongest normalization, where K-Means fits to the image pixels using only 2 clusters.

![flower_normalized](https://user-images.githubusercontent.com/33037020/180671892-97779609-7c6e-43be-aae0-7c1b58c25171.png)

[//]: #

[K-Means]: <https://scikit-learn.org/stable/modules/clustering.html#k-means>
[Color normalization]: <https://en.wikipedia.org/wiki/Color_normalization>
[image segmentation]: <https://www.mathworks.com/discovery/image-segmentation.html>
