### Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```python
# Developed By: Kancharla Narmadha
# Register Number: 212222110016
```
## Grayscale image and Color image
```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("nane.jpg.png")
color_image = cv2.imread("rapo.jpg.png")
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Color Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Histogram of Grayscale image and color image
```
import numpy as np
import cv2
Gray_image = cv2.imread("nane.jpg.png")
Color_image = cv2.imread("rapo.jpg.png")
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
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
## Histogram equalization of Grayscale image
```
import cv2
gray_image = cv2.imread("nane.jpg.png",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
### Input Grayscale Image and Color Image

![dip3 1](https://github.com/kancharlaNarmadha/Histogram-of-an-images/assets/119559316/8b4ed710-f8f8-4d15-9665-b8197b4abb4d)
![dip3 2 2](https://github.com/kancharlaNarmadha/Histogram-of-an-images/assets/119559316/b8bb27d6-970c-49da-83ee-70aa8d00be49)

### Histogram of Grayscale Image and any channel of Color Image
![dip3 3](https://github.com/kancharlaNarmadha/Histogram-of-an-images/assets/119559316/e1d3eb28-b5e8-450d-9302-c853e1d751c7)

![dip3 4](https://github.com/kancharlaNarmadha/Histogram-of-an-images/assets/119559316/6fb9df06-59b6-4336-b311-f0d373bc25f2)


### Histogram Equalization of Grayscale Image.

![dip3 5](https://github.com/kancharlaNarmadha/Histogram-of-an-images/assets/119559316/cb38f1e6-0cb9-43f0-a2d2-06f4150bbc57)


![dip3 6](https://github.com/kancharlaNarmadha/Histogram-of-an-images/assets/119559316/63f27ac0-4153-4d65-87b5-1c2c01874175)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
