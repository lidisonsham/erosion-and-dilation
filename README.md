# Ex: 09 Implementation-of-Erosion-and-Dilation-Using-OpenCV
# Aim
To write a Python program using OpenCV to perform morphological operations such as Erosion and Dilation on an image.

The program performs the following operations:

Image Erosion Image Dilation

# Software Used
Anaconda – Python 3.7 Jupyter Notebook / VS Code OpenCV (cv2) NumPy Matplotlib

# Algorithm
Step 1: Import the required libraries: OpenCV, NumPy, and Matplotlib.

Step 2: Create a blank image using NumPy.

Step 3: Insert text onto the image using OpenCV's text drawing function.

Step 4: Display the original image.

Step 5: Create a structuring element (kernel) of suitable size.

Step 6: Image Erosion Apply the erosion operation using the created kernel. Remove pixels from the boundaries of foreground objects. Display the eroded image. Step 7: Image Dilation Apply the dilation operation using the same kernel. Add pixels to the boundaries of foreground objects. Display the dilated image. Step 8: Compare the original, eroded, and dilated images.

 # program

 ```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = np.zeros((500, 500, 3), dtype=np.uint8)
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'HELLO WORLD', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')

kernel = np.ones((3, 3), np.uint8)
eroded_image = cv2.erode(image, kernel, iterations=1)
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Eroded Image")
plt.axis('off')
dilated_image = cv2.dilate(image, kernel, iterations=1)
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Dilated Image")
plt.axis('off')

```

# output
<img width="538" height="505" alt="image" src="https://github.com/user-attachments/assets/15512446-9e1e-48fb-b415-b145defff66c" />
<img width="522" height="507" alt="image" src="https://github.com/user-attachments/assets/3dfbcb02-7e66-41ee-991b-2023b1958589" />
<img width="507" height="507" alt="image" src="https://github.com/user-attachments/assets/801a29f3-648d-4b94-a7e5-b189a35c7f76" />


# result
Thus, the erosion and dilation is successfully implemented by completing the missing code sections. The system detects and highlights lane lines effectively.
