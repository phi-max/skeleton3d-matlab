# skeleton3D-matlab: Parallel medial axis thinning of a 3D binary volume

This code calculates the 3D medial axis skeleton of an arbitrary 3d binary volume. It is an optimized MATLAB implementation of the homotopic thinning algorithm described in [1]. We developed it to quantify the network of cell processes in bone [2], but it should work on images of any tubular or filamentous structures. An example volume (testvol.mat) is included, along with an example script (Test_Skeleton3D.m). Any comments, corrections or suggestions are highly welcome.

## Usage:

`skel = Skeleton3D(bin)`

where "bin" is a 3D binary image, and "skel" the resulting image containing only the skeleton voxels, or

`skel = Skeleton3D(bin,mask)`

to mask all foreground voxels in 'mask' from skeletonization, e.g. to preserve certain structures in a image volume.

For additional cleanup, e.g. pruning of short branches, please use my Skel2Graph3D package on MATLAB File Exchange.

This code is inspired by the ITK implementation by Hanno Homann [3] and the Fiji/ImageJ plugin by Ignacio Arganda-Carreras [4]. If you include this in your own work, please cite our original publicaton [2].

Philip Kollmannsberger 09/2013
philipk@gmx.net

References:

[1] Ta-Chih Lee, Rangasami L. Kashyap and Chong-Nam Chu
"Building skeleton models via 3-D medial surface/axis thinning algorithms."
Computer Vision, Graphics, and Image Processing, 56(6):462–478, 1994.

[2] Kerschnitzki, Kollmannsberger et al.,
"Architecture of the osteocyte network correlates with bone material quality."
Journal of Bone and Mineral Research, 28(8):1837-1845, 2013.

[3] http://hdl.handle.net/1926/1292

[4] http://fiji.sc/wiki/index.php/Skeletonize3D
