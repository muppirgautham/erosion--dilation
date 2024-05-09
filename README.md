# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary pacakages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate the Image

 
## Program:
```
Name: M Gautham
Register No: 212221230027
```
# Import the necessary packages
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
```

# Create the Text using cv2.putText
```
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_TRIPLEX
cv2.putText(img ,'Gautham',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```

# Create the structuring element
```
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```

# Erode the image
```
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')

```
# Dilate the image
```
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')

```
## Output:

### Display the input Image
![image](https://github.com/muppirgautham/erosion--dilation/assets/94810884/778238df-a545-446f-9e31-26aa76575695)


### Display the Eroded Image
![image](https://github.com/muppirgautham/erosion--dilation/assets/94810884/ff13bef4-6cf6-4da5-bffb-f700f0c1903a)

### Display the Dilated Image
![image](https://github.com/muppirgautham/erosion--dilation/assets/94810884/2a746f64-374a-4d99-81ec-e3ff37827320)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
