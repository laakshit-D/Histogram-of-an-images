# Histogram-of-an-images
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
```
Developed By: LAAKSHIT D
Register Number: 212222230071
```
## Input Grayscale Image and Color Image 
```py
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("GRAY IMAGE.jpg")
color_image = cv2.imread("newimgcolor.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Histogram of Grayscale Image and any channel of Color Image
```py
import numpy as np
import cv2
Gray_image = cv2.imread("GRAY IMAGE.jpg")
Color_image = cv2.imread("newimgcolor.jpg")
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
## Histogram Equalization of Grayscale Image
```py
import cv2
gray_image = cv2.imread("GRAY IMAGE.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
## Input Grayscale Image and Color Image

![gray scale out](https://github.com/KRISHNARAJ-D/Histogram-of-an-images/assets/119559695/cb291312-a8f3-49ac-9db0-4b2c2a6c6fe6)

![Screenshot 2024-03-20 232626](https://github.com/KRISHNARAJ-D/Histogram-of-an-images/assets/119559695/1aeee5ad-5ba2-4eaf-a4e1-dd79694b537e)

## Histogram of Grayscale Image and any channel of Color Image

![dip 3 out 2](https://github.com/KRISHNARAJ-D/Histogram-of-an-images/assets/119559695/cf44d470-3681-4734-8d96-5008f56c20de)

![dip 3 out 3](https://github.com/KRISHNARAJ-D/Histogram-of-an-images/assets/119559695/613192d2-e12b-4d0c-8f48-7da06146512c)

![dip 3 out 4](https://github.com/KRISHNARAJ-D/Histogram-of-an-images/assets/119559695/6c33abf3-5b79-42c3-8897-c2c208f2891c)

![dip 3 out 5](https://github.com/KRISHNARAJ-D/Histogram-of-an-images/assets/119559695/49c32635-d625-4f8a-a581-6591d338482e)

## Histogram Equalization of Grayscale Image.

![IP 3 OUT 6](https://github.com/KRISHNARAJ-D/Histogram-of-an-images/assets/119559695/b43cc2b8-f3d4-40a8-ad8a-4477f3326f71)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
