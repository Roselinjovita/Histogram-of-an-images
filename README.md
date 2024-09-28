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
# Developed By: ROSELIN MARY JOVITA.S
# Register Number: 212222230122

import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread('gray.jpg')
color_image = cv2.imread('color.jpg')
cv2.imshow("Gray image",gray_image)
cv2.imshow("color image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

import numpy as np
gray_image=cv2.imread('gray.jpg')
import matplotlib.pyplot as plt 
gray_hist=cv2.calcHist(gray_image,[0],None,[255],[0,255])
plt.figure(figsize=(10,6))
plt.subplot(1,2,1)
plt.imshow(gray_image)
plt.subplot(1,2,2)
plt.title("Histogram")
plt.xlabel("Grayscale value")
plt.ylabel("pixel count")
plt.stem(gray_hist)
plt.show()

import numpy as np
color_image=cv2.imread('color.jpg')
color_img=cv2.cvtColor(color_image,cv2.COLOR_BGR2RGB)
import matplotlib.pyplot as plt 
color_hist=cv2.calcHist(color_img,[0],None,[255],[0,255])
plt.figure(figsize=(8,4))
plt.subplot(1,2,1)
plt.imshow(color_img)
plt.subplot(1,2,2)
plt.title("Histogram")
plt.xlabel("Colorscale value")
plt.ylabel("pixel count")
plt.stem(color_hist)
plt.show()

import cv2
gray_image = cv2.imread("gray.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
## Output:
### Input Grayscale Image and Color Image
<table>
<tr>
<td>
      
![Screenshot 2024-09-28 111149](https://github.com/user-attachments/assets/10bf0686-d92e-4bf2-ba02-4b9921d10770)

</td>
<td>
  
![Screenshot 2024-09-28 110330](https://github.com/user-attachments/assets/aa57c85b-75ae-473b-9b15-b7b4f2316ad7)


</td>
</tr>
</table>


### Histogram of Grayscale Image  any channel of Color Image

![Screenshot 2024-09-28 111045](https://github.com/user-attachments/assets/6e6951b5-b902-476d-9f13-8fdba0e11e59)


### Histogram of any channel of Color Image

![Screenshot 2024-09-28 111443](https://github.com/user-attachments/assets/17e7aa1f-900d-4d63-85e1-08da0e38e8a4)


### Histogram Equalization of Grayscale Image.


![Screenshot 2024-09-28 111022](https://github.com/user-attachments/assets/fae88680-2977-4e02-bbaa-b4525b9f07c1)




## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
