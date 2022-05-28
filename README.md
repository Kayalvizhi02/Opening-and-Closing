# Opening and Closing

## Aim:
To implement Opening and Closing using Python and OpenCV.

## Software Required:
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:
### Step 1:

Import the necessary packages.

### Step 2:

Create the text image using cv2.putText.

### Step 3:

Then create the structuring element for opening and closing.

### Step 4:

Apply erosion and dilation using cv2.MORPH_OPEN and cv2.MORPH_CLOSE.

### Step 5:

Plot the images using plt.imshow.

 
## Program:
### Developed by : KAYALVIZHI M
### Register Number: 212220230024

``` Python
# Import the necessary packages

import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText

text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image,"Kayal",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image,'magma')
plt.axis('off')

# Create the structuring element

kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(9,9))

# Use Opening operation

image1=cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("Opening")
plt.imshow(image1,'magma')
plt.axis('off')


# Use Closing Operation

image2=cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("Closing")
plt.imshow(image2,'magma')
plt.axis('off')

```
## Output:

### Display the input Image

![img](https://user-images.githubusercontent.com/75413726/170830330-cec7127e-259b-47fc-9471-1316b5731d81.jpg)

### Display the result of Opening

![img1](https://user-images.githubusercontent.com/75413726/170830348-61108994-e0cf-428e-a9c9-0ed008f840e8.jpg)

### Display the result of Closing

![img2](https://user-images.githubusercontent.com/75413726/170830359-a6ff92bc-97ef-4fc5-be9d-c347dca678a5.jpg)

## Result:

Thus the Opening and Closing operation is used in the image using python and OpenCV.
