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

# Developed By: ibrahim fedah s
# Register Number: 212223240056

# Input Grayscale Image
```
import cv2
from matplotlib import pyplot as plt
# Load the color image
image = cv2.imread('image.jpg')
# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')

```
# Histogram of Grayscale Image
```
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])
```
# Equalization
```
# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)
plt.imshow(equalized_image, cmap='grey')
plt.title('Equalized Image')
plt.axis('off')
```
# Equalized Histogram
```
hist_original = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])
```

## Output:
### Input Grayscale Image and Color Image


<img width="755" height="482" alt="372328424-406ea744-e2d9-4ac5-bc69-5877cdc8e516" src="https://github.com/user-attachments/assets/9ceb2b0d-4ac2-4a22-aea3-d88264b13749" />

### Histogram of Grayscale Image and any channel of Color Image

<img width="835" height="592" alt="372328472-3c20e943-a360-4fcc-a2b1-be6d6d10a712" src="https://github.com/user-attachments/assets/f1454338-edf3-45b3-b3a4-31c4eb3b2ba2" />


### Histogram Equalization of Grayscale Image.

<img width="728" height="497" alt="372328546-6815ee35-f745-45cb-aebc-a6baa1e8bd79" src="https://github.com/user-attachments/assets/f88f9dc3-7540-45f4-b4d7-27db70020558" />

# Equalized Histogram.

<img width="876" height="585" alt="372328664-43e6415f-f296-46be-b06a-f800200e4acf" src="https://github.com/user-attachments/assets/96b0cbb4-59b5-4591-8d9a-559dcf5965c3" />

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
