# Image_segmentation_CV
Image segmentation using OpenCV

Objective : Count the number of rice grains in the Image. And, Find the number of broken grains in the image.

Technology used: OpenCv, WaterShed Algorithm, Image Preprocessing, pandas, numpy

The Given images were categorized into 3 

*Full grains
*Half grains
*Mixed grains 

Approach I used for
1.	Importing Required Libraries and packages
•	Defining custom "show" function for Image Visualization
2.	Image Pre-Processing
•	Grayscale Conversion
•	Image Thresholding
•	Noise Removal
•	Gaussian blurring
•	foreground object using erode function

3.	using Contours method to find the count the no of object and show the Contour filled in real image

4.	Applying Watershed Algorithm for Solving grains touching problem
5.	Counting total Rice grains and Broken Rice grains using the contour area
Objective of the program
Count the number of rice grains in the Image and Find the number of broken grains in the given image.

Three implementations in this approach are:
1.	Image Preprocessing
2.	Solving Grains touching problem
3.	Counting broken rice
Image Preprocessing
•	Image preprocessing is covers gray scale Conversion, Image Thresholding, Noise Removal, Gaussian blurring, foreground object using erode function, Morphology etc., and it take trail and error method to capture the parameters.
•	 Them the clear Image is obtained.

Solving Grains touching Problem

there is an object touching or overlapping problem, here image segmentation needs to solve these difficulties.
So, eradicate these issues, I applied the Watershed Algorithm:
Watershed Algorithm is based on extracting sure background and foreground and then using markers will make the watershed algorithm run and detect the exact boundaries.
It exactly finds the center of each object using Euclidean distance

Counting broken rice
After that, using labels total no of objects were got using evaluate the area of the pixels.
I used area-based approach, where I put a threshold of 180 to 800 for half grains.

Current limitations:
Still Lot of touching grains are accurately not separately calculated. Lot of half grains were not perfectly counted.
next steps to improve the algorithm.:
The image will zoom into 10 times. Then the touch boundaries of the two or more grains should be easily trace. 
Hence, we will calculate the grains more effectively.
