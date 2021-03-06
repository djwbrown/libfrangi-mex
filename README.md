libfrangi-mex
=============

Matlab Compatibility with MEX
-----------------------------
This fork of libfrangi has been modified to allow calling the filter function from Matlab.

Originally implemented by a team at the Norwegian University of Science and Technology (NTNU - Trondheim).
https://ntnu-bioopt.github.io/software/libfrangi.html

Basic usage
-----------

[J, scale, directions] = frangi2d ( img )

Include `frangi.h`. Create a variable `frangi2d_opts_t opts`. Set each field
to desired values or use `frangi2d_createopts(&opts)` for default values. 

Load the image into a `cv::Mat` instance. Create `cv::Mat` instances
for Frangi filter outputs: `J`, `scale` and `directions`. The 2D Frangi
filter can then be applied as `frangi2d(img, J, scale, directions, opts)`.

Building and installing
-----------------------

1. `TO DO`


Filter details
---------------

C++/OpenCV implementation of the Frangi multiscale vesselness filter in 2D (reference:
A. F. Frangi, W. J. Niessen, K. L. Vincken, and M. A. Viergever, “Multiscale vessel enhancement filtering,”
in Proc. Med. Image. Comput. Assist. Interv. 1496, pp. 130–137 (1998)).

This code is based on a MATLAB implementation found at [MATLAB Central](http://www.mathworks.com/matlabcentral/fileexchange/24409-hessian-based-frangi-vesselness-filter). 
