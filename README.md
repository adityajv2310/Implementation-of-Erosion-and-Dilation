# Implementation-of-Erosion-and-Dilation
## Aim:
To implement Erosion and Dilation using Python and OpenCV.
## Software Required:
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the Text using cv2.putText.

### Step3:
Create the structuring element.

### Step4:
Erode and Dilate the image.

### Step5:
End Program.

 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Load the image
img1=np.zeros((200,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL

# Create the Text using cv2.putText
cv2.putText(img1,' ADITYA ',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img1,cmap='gray')

# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image
img_erode=cv2.erode(img1,kernel1)
plt.imshow(img_erode,cmap='gray')

# Dilate the image
img_dilate=cv2.dilate(img1,kernel1)
plt.imshow(img_dilate,cmap='gray')

```
## Output:

### Display the input Image

![input image](https://user-images.githubusercontent.com/75235386/170811675-4d829e18-e8b8-4db4-a615-6d77dc9330c2.png)

### Display the Eroded Image

![Eroded img](https://user-images.githubusercontent.com/75235386/170811684-08ccf87d-4557-477c-8d01-d731210771e3.png)

### Display the Dilated Image

![Dilated img](https://user-images.githubusercontent.com/75235386/170811690-730c937f-71f8-4256-be81-1214935cb2af.png)


## Result:
Thus the generated text image is eroded and dilated using python and OpenCV.
