# Histogram-of-an-images
## Date:
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
### Developed By: Ramya R
### Register Number: 212223230169

### Input Grayscale Image and Color Image
## Gray Image
```
import cv2
import matplotlib.pyplot as plt
gray_image=cv2.imread('Exp-3 image.jpg')
grey=cv2.cvtColor(gray_image,cv2.COLOR_BGR2GRAY)
plt.imshow(grey)
plt.axis('on')
plt.show()
```
![Screenshot 2024-09-25 192537](https://github.com/user-attachments/assets/ff994e64-a274-4895-8b0f-3d53c185c652)

## Color Image:
```
color_image=cv2.imread('Exp-3 image2.jpg')
plt.imshow(color_image)
plt.axis('on')
plt.show()
```
![Screenshot 2024-09-25 192742](https://github.com/user-attachments/assets/3b896098-88aa-4a55-8d7c-19c8c84cecca)

### Histogram of Grayscale Image and any channel of Color Image
## Gray Image:
```
import numpy as np
Gray_image = cv2.imread("Exp-3 image.jpg")
Color_image = cv2.imread("Exp-3 image2.jpg")
grey=cv2.cvtColor(gray_image,cv2.COLOR_BGR2GRAY)
gray_hist = cv2.calcHist([grey],[0],None,[1100],[0,1100])
plt.figure()
plt.imshow(grey)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
```
![Screenshot 2024-09-25 194424](https://github.com/user-attachments/assets/b54a73f8-144b-422c-a264-e6350fc6ebcf)

## Color Image:
```
color_hist = cv2.calcHist([Color_image],[0],None,[2600],[0,2600])
plt.figure() 
plt.imshow(color_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
```
![Screenshot 2024-09-25 194545](https://github.com/user-attachments/assets/218fe66d-0ec6-4620-89a6-c49364c364b8)

### Histogram Equalization of Grayscale Image.
## Gray Image:
```
gray_image = cv2.imread("Exp-3 image.jpg")
grey=cv2.cvtColor(gray_image,cv2.COLOR_BGR2GRAY)
plt.imshow(grey)
plt.show()
```
![Screenshot 2024-09-25 194649](https://github.com/user-attachments/assets/d5a8e9f8-f5c0-455d-8030-872fc7a19b5b)

```
equ = cv2.equalizeHist(grey)
plt.imshow(equ)
plt.show()
```
![Screenshot 2024-09-25 194740](https://github.com/user-attachments/assets/56ceee67-3043-4dca-90b4-b5cd8cff893b)

## Color Image:
```
color_image=cv2.imread('Exp-3 image2.jpg')
grey=cv2.cvtColor(color_image,cv2.COLOR_BGR2GRAY)
plt.imshow(color_image)
plt.show()
```
![Screenshot 2024-09-25 194837](https://github.com/user-attachments/assets/056a6b51-6af0-4f00-96e0-5e65ef3a5c81)

```
eq = cv2.equalizeHist(grey)
plt.imshow(eq)
plt.show()
```
![Screenshot 2024-09-25 194923](https://github.com/user-attachments/assets/266c5cf2-21ab-49b6-8c01-b08e9bf97bb0)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
