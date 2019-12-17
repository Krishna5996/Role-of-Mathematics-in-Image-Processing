# Role-of-Mathematics-in-Image-Processing
Most commonly used Image Processing tasks include; Image Restoration, Image Segmentation,Image Enhancement, De-Blurring, De-noising, etc
Mathematics is quite inherent and deeply connected to various core Image
Processing tasks: just like, De-noising, De-blurring, Enhancement, Segmentation and Edge Detection etc. The study of such Image Processing tasks provides a unique opportunity of incorporating Mathematical tools and techniques to address several of the Image Processing applications in various scientific fields of study.

Histogram Equalization
The operation of histogram equalization is used to reassign grey values in the image, such that the histogram of the resultant image is (theoretically) flat. I say theoretically because practically, image intensities are discrete, and it may not be possible to reassign values equally across greyscale.
Practically speaking, this also means that the contrast is enhanced in the image, which is most of the times, a good thing, depending on your application.
By contrast enhancement, we mean that intermediate greyscale intensities that were not well represented in the image earlier, are now distributed better, and the intensities that occurred with very high frequency are de-emphasized.
 
https://upload.wikimedia.org/wikipedia/commons/thumb/c/ca/Histogrammeinebnung.png/300px-Histogrammeinebnung.png

Mostly the histogram isn't perfectly flat and perfectly distributed after equalization, and the mean will be close to the middle grey level. Closer to the middle grey level after histogram equalization than it was earlier.

2) Spatial Linear Filters
There are two classes of spatial linear filters:
(i) smoothing linear spatial filters
(ii) sharpening linear spatial filters

Smoothing linear spatial filters
Smoothing is known to cause local averaging (or blurring),which is similar with spatial summation or spatial integration.During the smoothing process, small details and noise gets lost,but sharp edges becomes blurry. Sharpening and smoothing operations results in opposite effects. Using smoothing, a blurry image f is made sharper, where edge of the image f would get enhanced

Sharpening linear spatial filters
Sharpening linear filters for image enhancement uses the Laplacian technique. It is assumed that image function f has second order partial derivatives.

Discrete Cosine Transform (DCT)

This technique is used for performing image compression 
step 1
find out dct matrix
.For first row fomula is given by 1/sqrt(n)
For next rows of  matrix sqrt(2/n)*cos[(2v+1)PI*u/2n] u and v are  indices of rows and matrix. For more information on DCT compression technique refer the  video link  given in reference
Step 2 multiply input image with dct matrix 
step3 resultant will be a matrix of comressed image. plot that matrix using matplotlib imshow function. for practical implementaion please refer code

About DCT
With the advent of the web and industry wide digital transformation, the JPEG (Joint  Photographic Experts Group) image format has emerged as a most commonly used format for
sharing images with lossy compression over the web. Discrete Cosine Transform (DCT) is one of the powerful techniques in domain of signal processing .

 DCT performs execution using mathematical operation technique known as Fast Fourier Transform (FFT). FFT takes one signal as an input and then transforms the representation from one type to another. In this transformation process, a signal from the spatial domain
gets transformed to the frequency domain. During this process, information redundancy is kept minimum because of kernel functions (cosines) comprise an orthogonal basis. This technique was first developed by J.W. Cooley and J.W. Tukey in 1965. FFT found wide acceptance since it helped in reducing the computation time and increased the ease of performing the digital Fourier analysis much more feasible.

4) Laplacian Distribution
The Laplacian distribution is one of the most commonly used approach used for performing image analysis. Since Laplacian approach uses invariant Gaussian kernels, there are known issues with regard to inability to represent the edges of images suitably. Hence, this approach
is not recommended for edge centric operations like preservation of  image edges, image, smoothing and tone mapping. 
Laplacian Operator is also known as a derivative operator which is used to find edges in an image. The major difference between Laplacian and other operators like Prewitt, Sobel, Robinson and Kirsch is that these all are first order derivative masks but Laplacian is a second order derivative mask. In this mask we have two further classifications one is Positive Laplacian Operator and other is Negative Laplacian Operator.
Another difference between Laplacian and other operators is that unlike other operators Laplacian didn’t take out edges in any particular direction but it take out edges in following classification.
•	Inward Edges
•	Outward Edges


Reference:
Research Papre Name :Role of Mathematics in Image Processing
Other Links
https://theailearner.com/2019/04/21/spatial-filtering/
https://docs.opencv.org/master/d4/d13/tutorial_py_filtering.html
https://medium.com/@almutawakel.ali/opencv-filters-arithmetic-operations-2f4ff236d6aa
https://opencv-python-tutroals.readthedocs.io/en/latest/py_tutorials/py_imgproc/py_histograms/py_histogram_equalization/py_histogram_equalization.html
https://www.youtube.com/watch?v=tW3Hc0Wrgl0

