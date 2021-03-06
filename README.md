## Computer Vision Nanodegree Program
![Computer Vision Nanodegree](https://images.ctfassets.net/2y9b3o528xhq/s0S62tcq7sXKhmKGSpycr/fb972c1ca3725605b33105fcaf1fd310/nd891_open_graph.jpg)

This repository contains my implementation of code exercises and materials for Udacity's Computer Vision Nanodegree program. It consists of tutorial notebooks that demonstrate, or challenged me to complete, various computer vision applications and techniques. These notebooks depend on a number of software packages to run, and so, I suggest that you create a local environment with these dependencies by following the instructions below.

## Nanodegree Syllabus
![YOLO](https://miro.medium.com/max/1400/1*4yMLrBPGadgWEoBu1i2jkQ.png)
### Part 1 - Introduction to Computer Vision
#### - [ ] [Open CV Library Fundamentals and Applications](https://github.com/sourcecode369/computer-vision/tree/master/OpenCV)
#### - [x] [Image Representation](https://github.com/sourcecode369/computer-vision/tree/master/Image%20Representation)
#### -  [x] [Convolutional Filters and Edge Detection](https://github.com/sourcecode369/computer-vision/tree/master/Convolutional%20Filters%20and%20Edge%20Detection)
#### - [x] [Types of Features and Image Segementation](https://github.com/sourcecode369/computer-vision/tree/master/Edge%20Detection%20and%20Image%20Segmentation)
#### - [x] [Feature Vectors](https://github.com/sourcecode369/computer-vision/tree/master/Feature%20Vectors)
 - [ ] Convolutional Neural Network Layers

![Advanced Computer Vision](http://densepose.org/img/anno/anno1.png)
### Part 2 - Advanced Computer Vision and Deep Learning
 - [ ] YOLO - You Only Look Once
 - [ ] LSTM - Long Short Term Memory 
 - [ ] Attention Mechanism in Neural Networks

![Object Tracking](https://s3-ap-south-1.amazonaws.com/av-blog-media/wp-content/uploads/2019/03/image-segmentation.png)
### Part 3 - Object Tracking and Localization
 - [ ] Object Motion and Tracking 
 - [ ] Optical Flow and Feature Matching
 - [ ] Robot Localization
 - [ ] Graph Slam

## Configure and Manage Your Environment with Anaconda

Per the Anaconda [docs](http://conda.pydata.org/docs):

> Conda is an open source package management system and environment management system 
for installing multiple versions of software packages and their dependencies and 
switching easily between them. It works on Linux, OS X and Windows, and was created 
for Python programs but can package and distribute any software.

### Overview
Using Anaconda consists of the following:

1. Install [`miniconda`](http://conda.pydata.org/miniconda.html) on your computer, by selecting the latest Python version for your operating system. If you already have `conda` or `miniconda` installed, you should be able to skip this step and move on to step 2.
2. Create and activate * a new `conda` [environment](http://conda.pydata.org/docs/using/envs.html).

\* Each time you wish to work on any exercises, activate your `conda` environment!

---

### 1. Installation

**Download** the latest version of `miniconda` that matches your system.

**NOTE**: There have been reports of issues creating an environment using miniconda `v4.3.13`. If it gives you issues try versions `4.3.11` or `4.2.12` from [here](https://repo.continuum.io/miniconda/).

|        | Linux | Mac | Windows | 
|--------|-------|-----|---------|
| 64-bit | [64-bit (bash installer)][lin64] | [64-bit (bash installer)][mac64] | [64-bit (exe installer)][win64]
| 32-bit | [32-bit (bash installer)][lin32] |  | [32-bit (exe installer)][win32]

[win64]: https://repo.continuum.io/miniconda/Miniconda3-latest-Windows-x86_64.exe
[win32]: https://repo.continuum.io/miniconda/Miniconda3-latest-Windows-x86.exe
[mac64]: https://repo.continuum.io/miniconda/Miniconda3-latest-MacOSX-x86_64.sh
[lin64]: https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh
[lin32]: https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86.sh

**Install** [miniconda](http://conda.pydata.org/miniconda.html) on your machine. Detailed instructions:

- **Linux:** http://conda.pydata.org/docs/install/quick.html#linux-miniconda-install
- **Mac:** http://conda.pydata.org/docs/install/quick.html#os-x-miniconda-install
- **Windows:** http://conda.pydata.org/docs/install/quick.html#windows-miniconda-install

### 2. Create and Activate the Environment

For Windows users, these following commands need to be executed from the **Anaconda prompt** as opposed to a Windows terminal window. For Mac, a normal terminal window will work. 

##### Git and version control
These instructions also assume you have `git` installed for working with Github from a terminal window, but if you do not, you can download that first with the command:
```
conda install git
```

If you'd like to learn more about version control and using `git` from the command line, take a look at our [free course: Version Control with Git](https://www.udacity.com/course/version-control-with-git--ud123).

**Now, we're ready to create our local environment!**

1. Clone the repository, and navigate to the downloaded folder. This may take a minute or two to clone due to the included image data.
```
git clone https://github.com/udacity/CVND_Exercises.git
cd CVND_Exercises
```

2. Create (and activate) a new environment, named `cv-nd` with Python 3.6. If prompted to proceed with the install `(Proceed [y]/n)` type y.

	- __Linux__ or __Mac__: 
	```
	conda create -n cv-nd python=3.6
	source activate cv-nd
	```
	- __Windows__: 
	```
	conda create --name cv-nd python=3.6
	activate cv-nd
	```
	
	At this point your command line should look something like: `(cv-nd) <User>:CVND_Exercises <user>$`. The `(cv-nd)` indicates that your environment has been activated, and you can proceed with further package installations.

3. Install PyTorch and torchvision; this should install the latest version of PyTorch.
	
	- __Linux__ or __Mac__: 
	```
	conda install pytorch torchvision -c pytorch 
	```
	- __Windows__: 
	```
	conda install pytorch-cpu -c pytorch
	pip install torchvision
	```

6. Install a few required pip packages, which are specified in the requirements text file (including OpenCV).
```
pip install -r requirements.txt
```

7. That's it!

Now all of the `cv-nd` libraries are available to you. Assuming you're environment is still activated, you can navigate to the Exercises repo and start looking at the notebooks:

```
cd
cd CVND_Exercises
jupyter notebook
```

To exit the environment when you have completed your work session, simply close the terminal window.


#### Notes on environment creation and deletion

**Verify** that the `cv-nd` environment was created in your environments:

```
conda info --envs
```

**Cleanup** downloaded libraries (remove tarballs, zip files, etc):

```
conda clean -tp
```

**Uninstall** the environment (if you want); you can remove it by name:

```
conda env remove -n cv-nd
```
### Collaborations
![Udacity+Nvidia](https://pbs.twimg.com/media/DcsJQuVX4AAknCf.jpg)
