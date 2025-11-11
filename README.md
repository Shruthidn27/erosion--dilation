# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV

# Algorithm:
### Step1:
import the neccesary packages

### Step2:
create the text using cv2.put Text

### Step3:
create the structuting element

### Step4:
Erodde the image

### Step5:
Dilate the image

 
## Program:
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
## Create a blank image
```
image = np.zeros((500, 500, 3), dtype=np.uint8)
```
## Add text on the image using cv2.putText
```
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Shruthi D N', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
```
## Display the input image
```
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
```
## Create a simple square kernel (3x3)
```
kernel = np.ones((3, 3), np.uint8)
```
## Apply erosion (shrinking effect)
```
eroded_image = cv2.erode(image, kernel, iterations=1)
```
## Display the eroded image
```
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Eroded Image")
plt.axis('off')
```






## Output:

### Display the input Image
<img width="819" height="545" alt="image" src="https://github.com/user-attachments/assets/dbe12011-7a6c-45ac-a31d-8ebf135c767e" />




### Display the Eroded Image
<img width="912" height="552" alt="image" src="https://github.com/user-attachments/assets/d0c5349e-646d-4988-bf0f-03b45bb91066" />


### Display the Dilated Image
<img width="873" height="557" alt="image" src="https://github.com/user-attachments/assets/62f49c95-c68f-41a9-8a58-0ba3e96f26f3" />



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
