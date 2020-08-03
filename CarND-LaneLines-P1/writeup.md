# **Finding Lane Lines on the Road** 


### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps:
* First, I converted the images to grayscale.

* Second, I blurred the images. 

* Third, I detected  edges. 

* Fourth, I selected the region of interest. 

* Fifth, I transformed the selected regions into hough space to detect lines and drawn the lines on the original image.

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by checking the slope of lines to divide them into two categories as left and right. Then find the lines fit the points of the two categories separately then drawn the two fitted lines on the original image.



![solidWhiteRight][image1]

![solidYellowCurve][image2]

![solidYellowLeft][image3]

![solidYellowCurve2][image4]

![solidWhiteCurve][image5]

![whiteCarLaneSwitch][image6]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be when there are shadows of obstacles on the road which will influence the edges detection.

Another shortcoming could be when the road is under strong sun light that the color of the road changes to be almost white wich will influence the edge detection as well.


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to use color images instead of grayscale images to improve the performance of edge detection.

Another potential improvement could be to use a more robust region selection algorithm to adapt to more complicated environment.


[image1]: ./test_images_output/solidWhiteRight.jpg 
[image2]: ./test_images_output/solidYellowCurve.jpg
[image3]: ./test_images_output/solidYellowLeft.jpg
[image4]: ./test_images_output/solidYellowCurve2.jpg
[image5]: ./test_images_output/solidWhiteCurve.jpg
[image6]: ./test_images_output/whiteCarLaneSwitch.jpg
