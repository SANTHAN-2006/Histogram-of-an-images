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
```python
## Developed By : K SANTHAN KUMAR
## Register Number : 212223240065
```
### Gray Image and Color Image
```python
import cv2
gray_img = cv2.imread('graytree.jpg')
gray_img = cv2.resize(gray_img,(300,200))
color_img = cv2.imread('dog.jpg')
color_img = cv2.resize(color_img,(300,200))
cv2.imshow("Gray Image",gray_img)
cv2.imshow("Colour Image",color_img)
cv2.waitKey(0)
```
## OUPUT :
![image](https://github.com/SANTHAN-2006/Histogram-of-an-images/assets/80164014/eb62624d-3efa-4ac4-84fb-664917c5b570)

### Histogram of Grayscale Image
```python
import cv2
import matplotlib.pyplot as plt
gray_img = cv2.imread('graytree.jpg')
color_img = cv2.imread('dog.jpg')
hist = cv2.calcHist([gray_img],[0],None,[256],[0,256])
hist1 = cv2.calcHist([color_img],[1],None,[256],[0,256])
plt.figure()
plt.imshow(gray_img)
plt.show()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()
```
## OUTPUT :
![image](https://github.com/SANTHAN-2006/Histogram-of-an-images/assets/80164014/40782ae8-8972-43b7-af1f-4cc0660456d2)
![image](https://github.com/SANTHAN-2006/Histogram-of-an-images/assets/80164014/05136329-2535-43d4-b4ad-14ea1f1c90b3)


### Histogram of Color Image
```python
import cv2
import matplotlib.pyplot as plt
gray_img = cv2.imread('graytree.jpg')
color_img = cv2.imread('dog.jpg')
hist = cv2.calcHist([gray_img],[0],None,[256],[0,256])
hist1 = cv2.calcHist([color_img],[1],None,[256],[0,256])
plt.figure()
plt.imshow(color_img)
plt.show()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()
```
## OUPUT :
![image](https://github.com/SANTHAN-2006/Histogram-of-an-images/assets/80164014/cf3aa93a-9027-4777-8e9d-70057b071a30)
![image](https://github.com/SANTHAN-2006/Histogram-of-an-images/assets/80164014/1e7a3d36-c67d-4445-a2ab-b30152340bfa)

### Histogram Equilization of GrayScale Image
```python
import cv2
gray_img = cv2.imread('graytree.jpg',0)
gray_img = cv2.resize(gray_img,(300,200))
cv2.imshow('Grey Scale Image',gray_img)
equ = cv2.equalizeHist(gray_img)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
```
## OUTPUT :
![image](https://github.com/SANTHAN-2006/Histogram-of-an-images/assets/80164014/ab8715a4-243a-4f86-969f-7b671b1ee51c)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
