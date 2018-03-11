# **Finding Lane Lines on the Road** 

## Writeup Template

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report

[//]: # (Image References)

[image1]: ./test_images_output/solidWhiteRight_greyscale.jpg "Greyscale"
[image2]: ./test_images_output/solidWhiteRight_gaussian.jpg "Gaussian"
[image3]: ./test_images_output/solidWhiteRight_canny.jpg "Canny"
[image4]: ./test_images_output/solidWhiteCurve_hough.jpg "Hough"
[image5]: ./test_images_output/solidWhiteRight_detected.jpg "Canny"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps (following in from the lectures):

1. First make the image greyscale ![alt text][image1]

2. Then Gaussian Blur ![alt text][image2]

3. Then Canny ![alt text][image3]

4. Define a polygon 

5. Define a Hough transformation ![alt text][image4]

6. Then Draw the lines ![alt text][image5]

## In order to draw a single line on the left and right lanes, I modified the draw_lines() function by ...

I just kept playing around with the parameters in order to get the continuous single line, especially playing with the rho value and the threshold. After a lot of trial and error the values seemed to work. Honestly the polygon values took the longest time to establish.


### 2. Identify potential shortcomings with your current pipeline

There are many many shortcomings with the project. It is very heavily based off the lectures and the lines do not exactly match up with the lane markings. I'm sure that I could use some kind of gradient of derivative to more closely align the line drawing to match the lane markings.

Also, my lack of python skills severely hampered my thinking. I need to improve on them to experiment more.

### 3. Suggest possible improvements to your pipeline

There is definitely a better line equation and detection of y = mx + b that I could use to better fit the line. Possible improvements are obviously attempting the challenge question. On the whole, however I am matching relatively closely to the lane markings and surprisingly did not have to change a lot from the pictures to the video.
