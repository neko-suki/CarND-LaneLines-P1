# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. 
- First, I converted the images to grayscale. 
- Second, I used gaussian_blur with `kernel_size` = 3. 
- Thrid, I applied Canny's edge detection algorithm with `low_threshold = 200`, `high_threshold = 220`. 
- Then, I applied region_of_interest with a Quadrilateral. I used coordinates of ROI as (0,540), (450, 315), (550, 315), (960, 540). 
- Finally, I applied `hough_lines` with parameter of `rho = 1`, `theta=1`, `threshold=10`, `min_line_len=10`, `max_line_gap=10`

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by ...

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
