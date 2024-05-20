# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
<br>


### Step2:
<br>

### Step3:
<br>

### Step4:
<br>

### Step5:
<br>

 
## Program:
```
Import the necessary packages
import cv2
import numpy as np
from matplotlib import pyplot as plt
Create the Text using cv2.putText
# Read the color image
input_image_path = 'Dhoni.jpg'
color_image = cv2.imread(input_image_path)

# Convert the color image to grayscale
gray_image = cv2.cvtColor(color_image, cv2.COLOR_BGR2GRAY)

# Perform edge detection using Canny
edges = cv2.Canny(gray_image, 100, 200)  # you can adjust the thresholds as needed

# Define the kernel size for erosion and dilation
kernel_size = 5
kernel = np.ones((kernel_size, kernel_size), np.uint8)

# Perform erosion
erosion = cv2.erode(edges, kernel, iterations=1)

# Perform dilation
dilation = cv2.dilate(edges, kernel, iterations=1)

# Perform opening
opening = cv2.morphologyEx(edges, cv2.MORPH_OPEN, kernel)

# Perform closing
closing = cv2.morphologyEx(edges, cv2.MORPH_CLOSE, kernel)
Create the structuring element
plt.figure(figsize=(15, 10))
plt.subplot(2, 3, 1)
plt.imshow(cv2.cvtColor(color_image, cv2.COLOR_BGR2RGB))
plt.title('Original Color Image')
plt.axis('on')
Use Opening operation
plt.subplot(2, 3, 2)
plt.imshow(opening, cmap='gray')
plt.title('Opening')
plt.axis('on')
Use Closing Operation
plt.subplot(2, 3, 3)
plt.imshow(closing, cmap='gray')
plt.title('Closing')
plt.axis('on')

plt.show()

```





## Output:

### Display the input Image
![image](https://github.com/MANOKARTHICK09/OPENING--AND-CLOSING/assets/121785458/1c1ecbce-840a-4a4d-9848-3efa2a3838f1)


### Display the result of Opening
![image](https://github.com/MANOKARTHICK09/OPENING--AND-CLOSING/assets/121785458/eb29687e-10d0-45a1-aed6-0dba3191ab94)


### Display the result of Closing
![image](https://github.com/MANOKARTHICK09/OPENING--AND-CLOSING/assets/121785458/39fa52f5-2f59-436c-af64-e954f1cb8424)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
