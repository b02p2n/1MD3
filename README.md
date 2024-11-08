java c
1MD3 Assignment 2
Please read this document very carefully. Follow instructions exactly. This assignment is due Nov. 8th, by 11:59pm
How can we represent an image as data? There are several (well infinite) ways to do that, but one intuitive approach is to view an image as a grid or table of pixels, where each pixel is encoded by three numerical values. The first, second, and third values represent how much red, green, and blue is present in that pixel. This is called RGB encoding and is quite common. If interested read: https://en.wikipedia.org/wiki/RGB_color_model for more information.
In Python, we can encode an image as a nested list of pixels. The interesting thing about this, is we can “read in” an image and convert it to a nested list, loop over this nested list potentially modifying and manipulating this data which in turn changes the image it is encoding, then save this data as a new image. In this assignment you will do exactly that.
You are given a file, assignment.py, with five incomplete functions. You must implement these five functions according to the information given in the document as well as the doc tests in the file. Note, there are also two complete functions given in the file. These are: get_raw_image() and image_from_raw(). The string parameters of these function refer to the name of the image file you wish to read from or write to. Note, for this to work assignment.py and the image file must be in the same directory.
For the purposes of this assignment we will use the following definitions.
1. Pixel: A pixel is a list of integers which has length three. The integer values within the list all range between 0 and 255 inclusive. For example, the following are all pixels: [1, 2, 3], [255, 0, 255], [0, 100, 200], while all of the following are not pixels: [-1, 2, -3], [300, 1000, 255], [0, 55.5]
2. Image data: Image data is a list of a list of pixels. Note, this means it is a list of a list of a list of ints. The length of all the rows of any image data are equal. The image data does not need to be square. That is, if data is image data, then len(data) does not necessarily equal len(data[0]). The following is image data:
[[[2代 写1MD3 Assignment 2Python
代做程序编程语言33, 100, 115], [0, 0, 0], [255, 255, 255]]
[[199, 201, 116], [1, 9, 0], [255, 255, 255]]]
while the following are not image data:
[[[233, 100], [0, 0, 0], [255, 255, 255]]
[[199, 201, 116], [1, 9], [255, 255, 255]]]
[[[233, 100, 115], [0, 0, 0], [255, 255, 255]]
[[199, 201, 116], [1, 9, 0]]]
[[[233, 100, 700], [0, 0, 0], [255, 255, 255]]
[[199, 201, 116], [1, -9, 0], [255, 255, 255]]]
3. Height and width: If data is image data we refer to its height as len(data) and the width as len(data[0])
Submitting and Grading
This assignment will be submitted electronically via Avenue. Please submit your file as assign ment2.py.
This assignment is worth 10% of your final grade. Grading is done completely automatically. That is, a program calls your function, passes it certain arguments, and checks to see if it returns the expected output. The TA will not grade the assignment by running it and playing around with images, they will only test your functions. Each function is worth 20% of the assignment grade. For any one function, if you pass n of the m tests we run on that function, your grade for that function will be n/m. Late submissions will receive a grade of 0. It is considered submitted when I receive it, not when you try to submit it. Do not leave submissions to the last minute. Good luck!
Final Notes
To aid in further explanations of when these functions do, there will be some additional doc tests posted additional doc tests where needed.
You will note an import at the top of the file, i.e. PIL. You will need to install this library/package to read in and save images. You do not need to install this package to receive 100% on this assign-ment. I was able to install this using the command:
python -m pip install pillow
However, this may be different for you depending on your version of Python and OS. If you are having difficulties, try Googleing for a solution or ask the TAs for assistance in tutorial.
You Find some before-and-after images for some functions below:
Grey

Invert

Compress
Note this image has been compressed several times.
Mirror





         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
