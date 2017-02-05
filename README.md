# Udacity Self-Driving Car NanoDegree - Project 1
## Finding lane lines


<img src="test_images/laneLines_thirdPass.jpg" width="480" alt="Combined Image" />

When we drive, we use our eyes to decide where to go.  The lines on the road that show us where the lanes are act as our constant reference for where to steer the vehicle.  Naturally, one of the first things we would like to do in developing a self-driving car is to automatically detect lane lines using an algorithm.

The goal of this project is to detect lane lines in images using Python and OpenCV.  OpenCV means "Open-Source Computer Vision", which is a package that has many useful tools for analyzing images.  

## Set up

**Step 1:** Getting setup with Python

To do this project, you will need Python 3 along with the numpy, matplotlib, and OpenCV libraries, as well as Jupyter Notebook installed. 

Downloading and installing the Anaconda Python 3 distribution from Continuum Analytics is recommended because it comes prepackaged with many of the Python dependencies needed for this and future projects. It also makes it easy to install OpenCV, and includes Jupyter Notebook.  Beyond that, it is one of the most common Python distributions used in data analytics and machine learning, so a great choice if you're getting started in the field.

Choose the appropriate Python 3 Anaconda install package for your operating system <A HREF="https://www.continuum.io/downloads" target="_blank">here</A>.   Download and install the package.

If you already have Anaconda for Python 2 installed, you can create a separate environment for Python 3 and all the appropriate dependencies with the following command:

````
$ conda create --name=yourNewEnvironment python=3 anaconda
````
````
$ source activate yourNewEnvironment
````

**Step 2:** Installing OpenCV

Once you have Anaconda installed, first double check you are in your Python 3 environment:

````
$ python   
> Python 3.5.2 |Anaconda 4.1.1 (x86_64)| (default, Jul  2 2016, 17:52:12)  
  [GCC 4.2.1 Compatible Apple LLVM 4.2 (clang-425.0.28)] on darwin  
  Type "help", "copyright", "credits" or "license" for more information.  
>>>   
````
(Ctrl-d to exit Python)

run the following commands at the terminal prompt to get OpenCV:

````
$ pip install pillow  
$ conda install -c https://conda.anaconda.org/menpo opencv3
````

then to test if OpenCV is installed correctly:

````
$ python  
>>> import cv2  
>>>
```` 
(Ctrl-d to exit Python)

**Step 3:** Installing moviepy  

The "moviepy" package for processing video in this project is recommended (though you're welcome to use other packages if you prefer).  

To install moviepy run:

````
$ pip install moviepy  
````

and check that the install worked:

````
$ python  
>>>import moviepy  
>>>
```` 
(Ctrl-d to exit Python)

**Step 4:** Opening the code in a Jupyter Notebook

You will complete this project in a Jupyter notebook.  If you are unfamiliar with Jupyter Notebooks, check out <A HREF="https://www.packtpub.com/books/content/basics-jupyter-notebook-and-python" target="_blank">Cyrille Rossant's Basics of Jupyter Notebook and Python</A> to get started.

Jupyter is an ipython notebook where you can run blocks of code and see results interactively.  All the code for this project is contained in a Jupyter notebook. To start Jupyter in your browser, run the following command at the terminal prompt (be sure you're in your Python 3 environment!):

````
$ jupyter notebook
````

A browser window will appear showing the contents of the current directory.  Click on the file called "P1.ipynb".  Another browser window will appear displaying the notebook.  Follow the instructions in the notebook to complete the project.  

## Structure

This notebook is set up to test on static images first and then to pass in images from a video source into the pipeline.
All the code is in P1.ipynb.  (The cells listed below are in order they appear in the notebook, not the number next to them. I am still very much learning my way around a Jupyter notebook and have not yet looked into how to renumber the cells).

* Cell 1
    * Handles all the imports.
* Cell 2
    * Prints out a sampel image with the image dimensions.
* Cell 3
    * Contains helper functions used to process images.
* Cell 4
    * Lists the images in the directory.  Makes it easier to switch through them all.
* Cell 5
    * The code in cell 5 handles processing the image.
* Cell 6
    * Loads in the first video to run the pipeline on, this video uses white lane lines.
* Cell 7
    * Loads in the second video to run the pipeline on, this video contains a yellow lane line.
* Cell 8 
    * An extra challenge video that contained some roadblocks.
