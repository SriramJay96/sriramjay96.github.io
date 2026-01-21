---
layout: post
title: Lidar based glass detection for increased occupancy mapping 
description: Conducted detailed analysis of LIDAR data in front of opaque and transparent objects due to limitations , documenting internal components, ROS driver configuration. Created technical analysis documentation with photos and graphical insights for engineering reference. 
skills: 
  - Graphical analysis
  - ROS
  - Ouster LiDAR
  - Mean & Standard Deviation

main-image: /Ouster lidar.jpg
---

---
# Metrics for Analysis 
1. Mean: The mean was chosen as one of the metrics for analysis as it is very helpful to get an overall
picture of what the values lie and how close they are. Also, with the mean value of a dataset, we
can also find the differences in how different materials values differ just by observing one single
value.
2. Standard Deviation: Standard deviation unlike mean gives a curve of data for a given window,
which shows the distribution of the values over the period of time. It helps in understanding how
the values are changing over time or with change in material, and around what area most of the
values lie.
3. Types of Data from Ouster: As Ouster provides different types of values other than just point
clouds such as Range image. Intensity Image and Reflectivity Image. All three give different
insights, which helps in analysis.
### Types of Data from Ouster
Types of Data from Ouster
- Range image - 

## Analysis of Data
1. LiDAR facing a transparent object
{% include image-gallery.html images="/Hist1.jpeg" height="400" %}
images: /Hist1.jpg
The plots of colormap and histogram provide a thorough examination of the data gathered by LiDAR and demonstrate how the data can be utilized to identify opaque and transparent items to the LiDAR. By taking the mean and visualizing the standard deviation of a group of intensity
values collected from LiDAR, the intensity plots are calculated. The color map shows the light orange regions, which show the area where an opaque object is next to a transparent object, and the blue regions, which show the area where the LiDAR faces glass. The transparent item causes the intensity values to be lower, and the abrupt spike is assigned to the opaque object next to the transparent object, according to the histogram.

2. LiDAR facing an opaque object
{% include image-gallery.html images="/Hist2.jpeg" height="400" %}
Figure depicts the colormap and histogram plots of LiDAR facing an opaque object. We can see that the histogram plots of the intensity values of the LiDAR data follows a Gaussian Distribution and can be seen concentrated at a small interval, unlike that of the reflection from a
transparent object. The values are equally distributed since the laser pulse generated at that point on the object is consistently returned to the LiDAR to detect.

### Point Cloud data comparison 
The following data are the point cloud data alongside camera images with camera in front of transparent glass object, opaque object and no object respectively. From the data below it can be clearly seen that the point cloud data for the opaque object clearly sees the object in front of it as the rays are reflected whereas in the cases of transparent the rays pass through giving the impression of there is no
object in front of it, similar to what we can see when there is literally no object in front of the LiDAR, which shows how difficult it is to identify transparent objects with just LiDAR data. There could be a number of factors affecting the laser pulse generated that passes through transparent objects. It could be the refractivity of the material or the texture and thickness of the transparent object.
<!-- ## Embedding images 
### External images
{% include image-gallery.html images="https://live.staticflickr.com/65535/52821641477_d397e56bc4_k.jpg, https://live.staticflickr.com/65535/52822650673_f074b20d90_k.jpg" height="400"%}
<span style="font-size: 10px">"Starship Test Flight Mission" from https://www.flickr.com/photos/spacex/52821641477/</span>  
You can put in multiple entries. All images will be at a fixed height in the same row. With smaller window, they will switch to columns.   -->

### Images
{% include image-gallery.html images="/Transparentobject.jpeg" height="400" %} 
{% include image-gallery.html images="/Opaqueobject.jpeg" height="400" %} 
{% include image-gallery.html images="/Noobject.jpeg" height="400" %} 
place the images in project folder/images then update the file path.   

<!-- ## Embedding youtube video
The second video has the autoplay on. copy and paste the 11-digit id found in the url link. <br>
*Example* : https://www.youtube.com/watch?v={**MhVw-MHGv4s**}&ab_channel=engineerguy
{% include youtube-video.html id="MhVw-MHGv4s" autoplay= "false"%}
{% include youtube-video.html id="XGC31lmdS6s" autoplay = "true" %}

you can also set up custom size by specifying the width (the aspect ratio has been set to 16/9). The default size is 560 pixels x 315 pixels.  

The width of the video below. Regardless of initial width, all the videos is responsive and will fit within the smaller screen.
{% include youtube-video.html id="tGCdLEQzde0" autoplay = "false" width= "900px" %}  

<br>

## Adding a hozontal line
---

## Starting a new line
leave two spaces "  " at the end or enter <br>

## Adding bold text
this is how you input **bold text**

## Adding italic text
Italicized text is the *cat's meow*.

## Adding ordered list
1. First item
2. Second item
3. Third item
4. Fourth item

## Adding unordered list
- First item
- Second item
- Third item
- Fourth item

## Adding code block
```ruby
def hello_world
  puts "Hello, World!"
end
```

```python
def start()
  print("time to start!")
```

```javascript
let x = 1;
if (x === 1) {
  let x = 2;
  console.log(x);
}
console.log(x);

```

## Adding external links
[Wikipedia](https://en.wikipedia.org)


## Adding block quote
> A blockquote would look great if you need to highlight something


## Adding table 

| Header 1 | Header 2 |
|----------|----------|
| Row 1, Col 1 | Row 1, Col 2 |
| Row 2, Col 1 | Row 2, Col 2 |

make sure to leave aline betwen the table and the header -->


