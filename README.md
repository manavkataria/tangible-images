## Tangible Images
_Images you can Touch and Feel_

----
This project describes an algorithm for generation of forces from two-dimensional bitmapped images. The forces allow the user to feel the contours of the image with sufficient realism using haptic devices. We also propose an algorithm to generate textures for virtual surfaces in a simple manner. The main focus of this project pertains to generating a model for synthesizing haptic interaction with static images. We hope to compare our approach and improve upon the work by Manivannan and Vasudevan.^[1]^

**_Primary Keywords_**: Haptic Feedback, Image Processing, Virtual Reality

**_Secondary Keywords_**: Haptic Interaction, Rendering, two dimensional digital bitmapped image, Image Segmentation, Image Texture, Haptic Texture

1. Introduction
  1. Image Segmentation
2. Haptic Feedback
  1. Haptic Surface
  2. Haptic Texture
3. References

# Introduction
The project can be divided into the following major tasks / phases. Proposed Algorithm:
1. Conceive a (tangible) surface model from a given bitmap image using depth-detection or contour^[1]^ method. This model could be programmed on a haptic device to feel the shape/geometry of the generated virtual surface.
2. Identify image-segments with known texture properties using gradient-method,^[2]^ or others. The image segments would be mapped to haptic textures (see 3).
3. Map segments to haptic texture models like sand, ice, etc.
4. Generating Forces: If feasible, implement the algorithm on the haptic device Novint Falcon using Haptik Library^[3]^ on Matlab.
5. If time permits, design a suitable GUI that synchronizes Haptics Interface Point from Falcon and the input image.

## Image Segmentation
Image segmentation is a process of dividing an image into a number of different regions such that each region is homogeneous with respect to certain visual characteristics (but the union of any two adjacent regions is not.)^[4][5]^

### Algorithm
1. Convert image to gray scale.
2. Detect edge using canny filter or others.
3. Use gradient magnitude^[2]^ method to segment image. 

We intend to implement the following Image Processing content: 
* Edge Detection
* Image Texture Identification and 
* Image Segmentation (using image filters, convolution and correlation as required)

# Haptic Feedback
_What is Haptics?_: The science of sensing and manipulation through touch is called Haptics^[7]^. Recent advances in science and technology allow a user to touch and feel a virtual object using devices called Haptic Interfaces. One such device called Novint Falcon is a part of the Haptics Lab, IIT Bombay. If feasible we would attempt to physically generate Haptic Surfaces or Textures^[6]^.

## Haptic Surface 
Shape or Geometry of an object that a user can feel or touch. We intend to define a 3D landscape from an image that is tangible/touchable. The generation of Haptic Surface may be based on depth detection or contour method.^[1]^

### Algorithm
1. Start with a bounded rectangular planar surface model 
2. Add height / depth to the plane’s locales according to the image properties at the respective locale. May be derived from depth-detection/contour based methods (references)

** OR ** 

## Haptic Texture 
One of the possible objectives would be to generate textures haptically to give the user a feel of the image/object’s coarseness or smoothness. Haptic Texture can be defined as the repetitive or random deviation from the nominal surface that forms the three dimensional surface topography. The attributes of surface like lay, waviness, roughness, and flaws that a user can feel through touch. Image-segmentation using gradient method, histogram or others would be used as input to generate haptic textures. 

# References
1. _Vasudevan, H. and Manivannan_, M. “Tangible Images: Runtime Generation of Haptic Textures From Images” for HAPTICS. IEEE Computer Society, Washington, DC. Proceedings of the 2008 Symposium on Haptic interfaces For Virtual Environment and Teleoperator Systems, 357-360 (March 13 - 14, 2008). DOI=http://dx.doi.org/10.1109/HAPTICS.2008.4479971 
2. _V. Lakshmanan_, “A Heirarchical, Multiscale Texture Segmentation Algorithm for Real-World Scenes” PhD thesis, U. Oklahoma, Norman, OK, 2001 
3. _M. de Pascale and D. Prattichizzo_ “The Haptik Library: A Component Based Architecture for Uniform Access to Haptic Devices” IEEE Robotics & Automation Magazine, vol. 14, no. 4, pp. 64-75, Dec. 2007 
4. _M. Frucci et al._ “Case-Based Reasoning for Image Segmentation by Watershed Transformation” Studies in Computational Intelligence, Volume 73/2008, 319-353 DOI=10.1007/978-3-540-73180-1_11
5. http://en.wikipedia.org/wiki/Segmentation_(image_processing) 
6. _Manav Kataria and Tapudum_ “The Story of Touch” to be published in Electrical Dept. Technical Newspaper, IIT Bombay, 2009-10. http://manavkataria.wordpress.com/ 
7. _Srinivasan, Mandayam A._ “What is Haptics?” Touch Lab, Massachusetts institite of Technology 
8. Segmentation Image Courtsey: http://spie.org/x8899.xml?ArticleID=x8899 
  
  
**_Updated: 23rd September 2009_**

