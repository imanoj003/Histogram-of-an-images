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
 Developed By: MANOJ M
 Register Number: 212221240027
```
### Input Grayscale Image and Color Image

```python
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("mano.png")
color_image = cv2.imread("manoj.png",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-26 160108](https://github.com/user-attachments/assets/70b0a374-734c-4d75-866f-f8087aaf2df0)


### Histogram of Grayscale Image and any channel of Color Image

```python
import numpy as np
Gray_image = cv2.imread("mano.png")
Color_image = cv2.imread("manoj.png")
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
```![Screenshot 2024-09-26 1601
46](https://github.com/user-attachments/assets/bd4f558f-f0a7-44ad-aacd-7a0da6cc5f74)




#### Grayscale Image



#### Color Image

```python
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```

![Screenshot 2024-09-26 160210](https://github.com/user-attachments/assets/c5592897-faf1-4f06-8f3e-7e979b251fab)


### Histogram Equalization of Grayscale Image.

```python
import cv2
gray_image = cv2.imread("mano.png",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![Screenshot 2024-09-26 160249](https://github.com/user-attachments/assets/0dfaa036-266b-4ae7-b8bf-523a819f9177)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
