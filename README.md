# EDGEDETECTION

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages for further process.
<br>


### Step2:
Read the image and convert the bgr image to gray scale image.
<br>

### Step3:
Use any filters for smoothing the image to reduse the noise.
<br>

### Step4:
Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.
<br>

### Step5:
Display the filtered image using plot and imshow.
<br>

 
## Program:
```
DEVELOPED BY: GURUMOORTHI R
REG NO : 212222230042
```

 Python
```
# Import the packages
import cv2
import matplotlib.pyplot as plt
```

# Load the image, Convert to grayscale and remove noise
```
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("dipt.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```

# SOBEL EDGE DETECTOR
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
###  SOBEL X AXIS :

![1](https://github.com/gururamu08/EDGEDETECTION/assets/118707009/aeb6f344-5281-4deb-94a4-b50fe98ec99a)


###  SOBEL Y AXIS :

![2](https://github.com/gururamu08/EDGEDETECTION/assets/118707009/c65c2bf2-7aaf-4ed9-893a-265a8bb10a41)


###  SOBEL XY AXIS :

![3](https://github.com/gururamu08/EDGEDETECTION/assets/118707009/53f5032e-ea5a-4243-897b-fb991115e5db)

<br>


### LAPLACIAN EDGE DETECTOR

![4](https://github.com/gururamu08/EDGEDETECTION/assets/118707009/fc091f48-1f3a-4da6-8f2c-573cdd9c00d1)

<br>


### CANNY EDGE DETECTOR

![5](https://github.com/gururamu08/EDGEDETECTION/assets/118707009/7729be3a-ede8-4123-8b75-1aa3084a9c32)

<br>

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
