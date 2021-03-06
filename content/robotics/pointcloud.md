---
title: "Point cloud"
slug: pointcloud
description: null
date: 2020-01-02T19:40:00-08:00
type: notes
draft: false
categories:
- General
tags:
- AV
series:
-
---

A [point cloud](https://en.wikipedia.org/wiki/Point_cloud) is a set of data points in space.

<!--more-->

## Libraries 

### PCL - Point Cloud Library

Links:
* repo: https://github.com/PointCloudLibrary/pcl

Dependencies:

* [FLANN](https://github.com/mariusmuja/flann) - Fast Library for Approximate Nearest Neighbor
* [Eigen](http://eigen.tuxfamily.org/index.php?title=Main_Page)
* [VTK](https://vtk.org/) - manipulating and displaying scientific data

Cons:
* transitive dependencies can be hard to install

See an example [Dockerfile](https://gist.github.com/winding-lines/2d61189226df8193eeec4669b57d764d).

### Cilantro

"A lean C++ library for working with point cloud data "

Links:

* code: https://github.com/kzampog/cilantro
* technical report: (https://arxiv.org/abs/1807.00399)

Bundled dependencies:

* [nanoflann](https://github.com/jlblancoc/nanoflann) for general dimension kd-trees
* [tinyply](https://github.com/ddiakopoulos/tinyply) for reading pointcloud data
* [QHull](http://www.qhull.org/) for convex hull computation
* [Spectra](https://github.com/yixuan/spectra) for [spectral clustering](https://en.wikipedia.org/wiki/Spectral_clustering)

External dependencies:

* [Eigen](http://eigen.tuxfamily.org/index.php?title=Main_Page)
* [Pangolin](https://github.com/stevenlovegrove/Pangolin) for OpenGL display/interaction

Pros: easy to compile

Cons: no python bindings?

### Open3d

"A modern library for 3D processing"

Links:

* site: http://www.open3d.org/
* repo: https://github.com/intel-isl/Open3D
* intro: http://www.open3d.org/docs/release/tutorial/Basic/pointcloud.html

Cons:
* does not seem to have an implementation of Generalized ICP.

## Algorithms

[Iterative Closest
Point](https://en.wikipedia.org/wiki/Iterative_closest_point) is one of the
algorithms implemented by PCL
[Generalized_ICP](http://www.robots.ox.ac.uk/~avsegal/resources/papers/Generalized_ICP.pdf).
 

A related approach is [Real time correlative scan matching](https://april.eecs.umich.edu/media/pdfs/olson2009icra.pdf)

## Papers

https://paperswithcode.com/task/3d-object-detection/codeless

## Data formats

* pcd: http://pointclouds.org/documentation/tutorials/pcd_file_format.php
* ply: https://en.wikipedia.org/wiki/PLY_(file_format)
* stl: https://en.wikipedia.org/wiki/STL_(file_format)


## Competitions datasets

Multiple Object Tracking Benchmark: https://motchallenge.net/