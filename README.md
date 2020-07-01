# Finding Lane Lines on the Road

The goals / steps of this project are the following:
Make a pipeline that finds lane lines on the road

## Reflection
### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.
My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I apply gaussian blur. 
Edges are calculated using canny function, region of interest is applied and hough transform is applied.
In order to draw a single line on the left and right lanes, I modified the draw_lines() function by splitting 
the data into left and right side and then calcultate the limits of each side. 
### Test images are presented below

![alt text](https://github.com/ranceaaa/PROJECT-1---FINDING-LANE-LINES/tree/master/test_images_output/_solidWhiteCurve.jpg?raw=true)
[Image 2]: https://github.com/ranceaaa/PROJECT-1---FINDING-LANE-LINES/tree/master/test_images_output/_solidWhiteRight.jpg  "Image 2"
[Image 3]: https://github.com/ranceaaa/PROJECT-1---FINDING-LANE-LINES/tree/master/test_images_output/_solidYellowCurve.jpg "Image 3"
[Image 4]: https://github.com/ranceaaa/PROJECT-1---FINDING-LANE-LINES/tree/master/test_images_output/_solidYellowCurve2.jpg  "Image 4"
[Image 5]: https://github.com/ranceaaa/PROJECT-1---FINDING-LANE-LINES/tree/master/test_images_output/_solidYellowLeft.jpg  "Image 5"
[Image 6]: https://github.com/ranceaaa/PROJECT-1---FINDING-LANE-LINES/tree/master/test_images_output/_whiteCarLaneSwitch.jpg  "Image 6"

### 2. Identify potential shortcomings with your current pipeline
One potential shortcoming would be what would happen when shadow are covering the line
Another shortcoming could be when camera angle changes ( hood appears in the picture)

### 3. Suggest possible improvements to your pipeline
A possible improvement while working with videos would be calculating an average slope for each line and if there is no line detected, the average one will be used.
Another potential improvement could be to plot the last line, if the current one wasn't detected

### 4. Pipeline for challange video
