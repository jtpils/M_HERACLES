# M_HERACLES
HERitAge by point CLoud procESsing for Matlab

(c) by Arnadi Murtiyoso                          
Photogrammetry and Geomatics Group, ICube UMR 7357 INSA Strasbourg
Contact: arnadi.murtiyoso@insa-strasbourg.fr
https://github.com/murtiad          

A toolbox with functions for processing point cloud data in the context of cultural heritage documentation.

The code was developped with the Matlab Computer Vision Toolbox installed (2018a), as well as third party dependencies:
- Cloth Simulation Filter (CSF) by Wuming Zhang et al. (Zhang W, Qi J, Wan P, Wang H, Xie D, Wang X, Yan G. An Easy-to-Use Airborne LiDAR Data Filtering Method Based on Cloth Simulation. Remote Sensing. 2016; 8(6):501.): https://github.com/jianboqi/CSF
- M_MAP Toolbox by Rich Pawlowicz: https://www.eoas.ubc.ca/~rich/map.html. Note that I used this because I don't have the Matlab Mapping Toolbox installed :(

Available functions (05/10/2018):
- shapeseg.m : function to use (polygonal) ESRI shapefiles (.shp) to delimit ("cookie cutter" style) 3D point cloud area to be then cleaned using the pcsegdist function. This function generates separate segmented point clouds for each object, with their attributes as per the description in the shapefile.
- clustering.m : function to create individual point clouds in Matlab structure from an original point cloud segmented using the pcsegdist function 
- shpload.m : Loads a polygonal ESRI .shp file and convert it into a struct called 'Shape'. 'Shape' will contain as fields the individual objects in the file. Each field will contain a struct with information available in the .dbf file attached to the .shp file, as well as object type and geometry, both in the form of a list of vertex coordinates and in native Matlab polyshape object type. 
