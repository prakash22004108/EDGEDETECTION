# EDGEDETECTION

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step 1:
Import the required packages for further process.

### Step 2:
Read the image and convert the bgr image to gray scale image.

### Step 3:
Use any filters for smoothing the image to reduse the noise.

### Step 4:
Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.

### Step 5:
Display the filtered image using plot and imshow.

## Program:
```
DEVELOPED BY : PRAKASH R
REG NO : 212222240074
```
## Import the packages
```
import cv2
import matplotlib.pyplot as plt
```
# Load the image, Convert to grayscale and remove noise
```
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("windows.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
# SOBEL EDGE DETECTOR:
# SOBEL X AXIS :
```
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
# SOBEL Y AXIS :
```
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
# SOBEL XY AXIS :
```
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
# LAPLACIAN EDGE DETECTOR
```
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
# CANNY EDGE DETECTOR
```
canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:
### SOBEL EDGE DETECTOR
# SOBEL X AXIS :
![WhatsApp Image 2023-09-27 at 11 38](https://github.com/prakash22004108/EDGEDETECTION/assets/113497032/21e89840-52a2-4076-804f-256813f94072)

# SOBEL Y AXIS :
![WhatsApp Image 2023-09-27 at 11 38 2](https://github.com/prakash22004108/EDGEDETECTION/assets/113497032/b15f65ab-ec01-4501-a112-e9db89e79214)

# SOBEL XY AXIS :
![WhatsApp Image 2023-09-27 at 11 38 28](https://github.com/prakash22004108/EDGEDETECTION/assets/113497032/4716a5d7-c433-469c-b016-440ef040ddfe)


### LAPLACIAN EDGE DETECTOR
![WhatsApp Image 2023-09-27 at 11 38 29](https://github.com/prakash22004108/EDGEDETECTION/assets/113497032/9b2dd69d-0d3f-42ea-b527-d49e7e921111)


### CANNY EDGE DETECTOR
![WhatsApp Image 2023-09-27 at 11 38 30](https://github.com/prakash22004108/EDGEDETECTION/assets/113497032/14a858b0-b89a-4dbb-bb39-3e7c1d822bc9)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
