# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:
### Step1:
Import the necessary packages.

### Step 2:
Create the Text using cv2.putText.

### Step 3:
Create the structuring element.

### Step 4:
Use Opening operation.

### Step 5:
Use Closing Operation.

### Step 6:
Print the output and end the program.

 
## Program:
```
Developed by: NAVEENKUMAR V
Register number: 212221230068
```

``` 
# Import the necessary packages
import numpy as np
import matplotlib.pyplot as plt
import cv2

# Create the Text using cv2.putText
text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image,"NAVEEN",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("ORIGINAL IMAGE")
plt.imshow(text_image)
plt.axis('off')

# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation
open_image = cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("OPENING")
plt.imshow(open_image)
plt.axis('off')

# Use Closing Operation
close_image = cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("CLOSING")
plt.imshow(close_image)
plt.axis('off')
```

## Output:

### Display the input Image
![image](https://github.com/Naveenvetrivel/Opening-and-Closing/assets/94165322/9859228a-6c11-470b-8929-845f531730fb)


### Display the result of Opening
![image](https://github.com/Naveenvetrivel/Opening-and-Closing/assets/94165322/ba8cd6c5-6d00-4b31-87d4-f29b260c1c64)

### Display the result of Closing
![image](https://github.com/Naveenvetrivel/Opening-and-Closing/assets/94165322/22160221-847f-4709-9e2c-bf31a5e3ea24)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
