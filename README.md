# Histogram of images
## Aim
### To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
### Anaconda - Python 3.7

## Algorithm:
### Step1:
#### Read the gray and color image using imread()

### Step2:
#### Print the image using imshow().

### Step3:
#### Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
#### Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
#### The Histogram of gray scale image and color image is shown.


## Program:

### Colour and Gray Image

py
# Developed By: PREMKUMAR K
# Register Number:  212222230111

```import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("dhoni1.jpeg")
color_image = cv2.imread("dhoni2.jpeg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


### Histogram of Grayscale Image

```py
import numpy as np
import cv2
Gray_image = cv2.imread("dhoni1.jpeg")
Color_image = cv2.imread("dhoni2.jpeg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
```

### Histogram of Green channel of colour Image

```py
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)

```


```py

import cv2
gray_image = cv2.imread("dhoni2.jpeg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()

```

## Output:

### Input Grayscale Image and Color Image

![image](https://github.com/premkumarkarthikeyan/Histogram-of-an-images/assets/119476243/b42a7248-c6d6-4b34-98c2-eda98b3c3e0f)



### Histogram of Grayscale Image

![image](https://github.com/premkumarkarthikeyan/Histogram-of-an-images/assets/119476243/1df94678-355d-4d2d-9300-26fcfef9127d)

### Histogram of Green Channel of colour Image

![image](https://github.com/premkumarkarthikeyan/Histogram-of-an-images/assets/119476243/40e27343-7541-431c-9181-38d64674d3ff)


### Histogram Equalization of Grayscale Image.

![image](https://github.com/premkumarkarthikeyan/Histogram-of-an-images/assets/119476243/7143c071-c05b-4990-9275-390a6dc0b2d4)



## Result: 
### Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
