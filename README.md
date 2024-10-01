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

# Developed By: SENTHAMIL SELVAN G
# Register Number: 212222230139
```python
import cv2
from matplotlib import pyplot as plt

image = cv2.imread('obitowallpap.jpg')

gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')

hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])

plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])


equalized_image = cv2.equalizeHist(gray_image)

plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')

hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])

plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])





```
## Output:
### Input Grayscale Image and Color Image
```
(np.float64(-0.5), np.float64(1023.5), np.float64(1347.5), np.float64(-0.5))
```
![download](https://github.com/user-attachments/assets/83c074f0-6659-4d7f-aa8b-6a4c39718b2b)



### Histogram of Grayscale Image and any channel of Color Image
```
(0.0, 256.0)
```
![download](https://github.com/user-attachments/assets/d1875194-70e6-460b-9b34-d646ad90bd8f)




### Histogram Equalization of Grayscale Image.
```
(np.float64(-0.5), np.float64(1023.5), np.float64(1347.5), np.float64(-0.5))
```
![download](https://github.com/user-attachments/assets/bad1ad11-c699-4f68-b3bb-fc9db447d0ea)
```
(0.0, 256.0)
```
![download](https://github.com/user-attachments/assets/5a9b5fd0-c03c-4c3f-8673-df9625713df0)






## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
