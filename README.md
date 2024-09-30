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
# Developed By:NITHYAA SRI S S 
# Register Number:212222230100

import cv2
import numpy as np
from matplotlib import pyplot as plt

# Load the color image
image = cv2.imread('gems.jpg')

# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')

hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
# Plot histogram of the original grayscale image
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])


# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')

# Plot histogram of the equalized image
hist_equalized = cv2.calcHist([equalized_image], [0], None, [255], [0, 255])
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 255])

```
## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/user-attachments/assets/e74796cf-8f43-47d7-b836-85d96a8ab22d)

### Histogram of Grayscale Image and any channel of Color Image
![image](https://github.com/user-attachments/assets/55705fab-5cb7-408d-a0d8-39ab05e45eef)

### Histogram Equalization of Grayscale Image.
![image](https://github.com/user-attachments/assets/301c9855-e4f3-4c1b-913b-ad6067919bf7)
### Histogram of the equalized image
![image](https://github.com/user-attachments/assets/e587f3b7-3fd4-4c1d-a2c9-2e71289112b0)








## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
