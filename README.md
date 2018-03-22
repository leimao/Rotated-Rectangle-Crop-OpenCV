# Rotated_Rectangle_Crop_OpenCV

Author: Lei Mao

Date: 3/2/2018


## Introduction

In OpenCV, cropping a rectangle from an image is extremely easy. However, it does not provide a function to crop a rotated rectangle. Here I developed an algorithm to crop a rotated rectangle from an image, and implemented it as a python function.

## Algorithm

Original image and the rotated rectangle:

<p align="center">
    <img src = "https://github.com/leimao/Rotated_Rectangle_Crop_OpenCV/blob/master/algorithm/alg_step_1.png" width="60%">
</p>

Crop a minimal up-right rectangle containing the rotated rectangle:

<p align="center">
    <img src = "https://github.com/leimao/Rotated_Rectangle_Crop_OpenCV/blob/master/algorithm/alg_step_2.png" width="60%">
</p>

Rotate the cropped image such that the inner rotated rectangle becomes up-right and centered in the image:

<p align="center">
    <img src = "https://github.com/leimao/Rotated_Rectangle_Crop_OpenCV/blob/master/algorithm/alg_step_3.png" width="60%">
</p>

Crop the "rotated rectangle":

<p align="center">
    <img src = "https://github.com/leimao/Rotated_Rectangle_Crop_OpenCV/blob/master/algorithm/alg_step_4.png" width="60%">
</p>

## Dependencies

OpenCV 3.0

Python 3.5

## Usage

In Python or Jupyter Notebook:

```Python
from rotated_rect_crop import crop_rotated_rectangle
# image is the image matrix
# rect is the rotated rect object in OpenCV, i.e. (center (x,y), (width, height), angle of clock-wise rotation)
# center x is regarding to the width
# center y is regarding to the height
# width is the number of the columns of the rectangle.
# height is the number of the rows of the rectangle.
# The angle vector pointing to the "north" is exactly 0 degree
image_cropped = crop_rotated_rectangle(image, rect)
```

## Demo

Generate a random rotated rectangle and crop:

```Shell
python rotated_rect_crop.py
```

<p align="center">
    <img src = "https://github.com/leimao/Rotated_Rectangle_Crop_OpenCV/blob/master/demo/demo_good.png">
</p>