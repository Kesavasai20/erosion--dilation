# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages


### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate the Image

## Program:
## Developed by : K KESAVA SAI
## Register Number : 212223230105
```PY
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt
# Create the Text using cv2.putText
img = np.zeros((100,400),dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img,'KESAVA SAI',(40,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
# Create the structuring element
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))

# Erode the image
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
# Dilate the image
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```

## Output:

### Display the input Image
![image](https://github.com/Kesavasai20/erosion--dilation/assets/138849303/3520d43b-e8ce-4c37-98c8-04c651626ec5)

### Display the Eroded Image
![image](https://github.com/Kesavasai20/erosion--dilation/assets/138849303/a5eea1bf-b8f3-4f67-a5de-c20e9581a634)


### Display the Dilated Image
![image](https://github.com/Kesavasai20/erosion--dilation/assets/138849303/6a4ed512-1c74-4338-a346-043aa4004093)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
