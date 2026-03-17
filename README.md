# OPENING--AND-CLOSING
### Name - Naveenkumar M
### Register Number - 212224230183
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages

### Step2:
Create the Text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Use Opening operation

### Step5:
Use Closing Operation
 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create a blank image

image = np.zeros((500, 500, 3), dtype=np.uint8)
# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Naveenkumar', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)

# Create the structuring element
kernel = np.ones((3, 3), np.uint8)

# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')


# Opening is erosion followed by dilation
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)

# Display the result of Opening
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Opening Operation")
plt.axis('off')




# Closing is dilation followed by erosion
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
# Display the result of Opening
plt.imshow(cv2.cvtColor(closed_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Closing Operation")
plt.axis('off')

```
## Output:

### Display the input Image
<img width="706" height="572" alt="image" src="https://github.com/user-attachments/assets/a8bd95e4-a669-4d4e-8105-bef6375b680d" />


### Display the result of Opening
<img width="798" height="559" alt="image" src="https://github.com/user-attachments/assets/8248bf53-8e1c-4cda-8c2c-f1b3fee0aa9f" />


### Display the result of Closing
<img width="823" height="569" alt="image" src="https://github.com/user-attachments/assets/b0c5a888-7411-43fb-a7a2-3a20d482bdbf" />


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
