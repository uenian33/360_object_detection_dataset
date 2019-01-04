# Object Detection dataset for 360 images

## Contents

This repository contains following contents:
* the dataset collected and used in "Object Detection in Equirectangular Panorama"
* the evluation code (to be added)
* the comparison experiment results
* the annotation tool

## Paper
Object Detection in Equirectangular Panorama

Wenyan Yang, Yanlin Qian, Joni-Kristian Kämäräinen Francesco Cricri, Lixin Fan

International Conference on Pattern Recognition (ICPR) 2018

### Dataset

Downloads: [link](https://www.dropbox.com/s/skxqj94rno9ihjq/360-Dataset.zip?dl=0)
Slides: [link](https://1drv.ms/p/s!AjxmjW9wZcKxhWRqnijhIGrST0OC)

It contained three types of the ground truth: BFOV (Bounding FOV), BBox(Bounding box) and 3d-container frame. 

* BFOV (path: 360-Dataset/bbx-annotations/*)
```
<bndbox>
	<xmin>
	<ymin>
	<xmax>
	<ymax>
</BBOX> 
```

* BFOV (path: 360-Dataset/bfov-annotations/*)
```
<BFOV> 
	<center_lon> // centre's longitude
	<center_lat> // centre's latitude
	<bfov_w> // the width's radius
	<bfov_h> //  the height's radius
</BFOV> 
```

* 3D-Container Frame(path: 360-Dataset/bfov-annotations/*)
```
<ThreeDbox> 
// The 4 vertexes and 1 centre point of the BFOV. Stored in radians
      <tl_lon> // top left vertex's longitude.
      <tl_lat> // top left vertex's latitude.
      <tr_lon> // top right vertex's longitude.
      <tr_lat> // top right vertex's latitude.
      <br_lon> // bottom right vertex's longitude.
      <br_lat> // bottom right vertex's latitude.
      <bl_lon> // bottom left vertex's longitude.
      <bl_lat> // bottom left vertex's latitude.
      <c_lon> // centre's longitude
      <c_lat> // centre's latitude.
</ThreeDbox>
```

### Visualization
[![Dataset visualization](https://img.youtube.com/vi/FTnfsmgwdQA/0.jpg)](https://www.youtube.com/watch?v=FTnfsmgwdQA "Data visualization")
* To visualize the BBOX annotation, some traditional annotation tools are needed (e.g: https://github.com/tzutalin/labelImg)
* To visualize the BFOV annotation, use the tool in folder "/visualize_tool" (open the web browser and load the image and XML file)

### Annotation tool

To be added

### Comparison experiments results

To be added

### Running the tests

To be added

### License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

### Citation
* Please cite our paper if you find this work is useful.
```
@INPROCEEDINGS{8546070, 
author={W. Yang and Y. Qian and J. Kämäräinen and F. Cricri and L. Fan}, 
	booktitle={2018 24th International Conference on Pattern Recognition (ICPR)}, 
	title={Object Detection in Equirectangular Panorama}, 
	year={2018}
	pages={2190-2195}, 
	keywords={Detectors;Distortion;Object detection;Cameras;Image resolution;Virtual reality;Graphics processing units}, 
	doi={10.1109/ICPR.2018.8546070}, 
	ISSN={1051-4651}, 
	month={Aug}
}
