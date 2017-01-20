
# PhotoPipe

### Photometry Pipeline for RATIR and RIMAS

[![astropy](http://img.shields.io/badge/powered%20by-AstroPy-orange.svg?style=flat)](http://www.astropy.org/)
[![PyPI version](https://badge.fury.io/py/photopipe.svg)](https://badge.fury.io/py/photopipe)

PhotoPipe is a pipeline for automated reduction, photometry and astrometry, written in Python (2.7), and designed to process imaging data from the following instruments:

* [RATIR](http://butler.lab.asu.edu/RATIR/): the Reionization and Transients Infrared/Optical Project.
* [RIMAS](https://lowell.edu/research/research-facilities/4-3-meter-dct/rimas/): the Rapid infrared IMAger Spectrometer.

This project is based on the previous versions of the pipeline by [cenko](https://github.com/cenko/RATIR-GSFC) and [vickitoy](https://github.com/vickitoy/photometry_pipeline).  
Built at the NASA Goddard Space Flight Center, in collaboration with the University of Maryland.
<br><br><br>
![NASA GSFC - RATIR - UMD](https://github.com/maxperry/photometrypipeline/raw/master/docs/readme-logos.jpg)


## Full Documentation

See the [Wiki](https://github.com/maxperry/photometrypipeline/wiki) for full documentation, examples, operational details and other information.


## Prerequisites

The pipeline can be installed with very little additional software. However, depending on the installation, different libraries and software may be required. Please see the [Installation](#installation) section below, and the dedicated [wiki page](https://github.com/maxperry/photometrypipeline/wiki/Prerequisites) for a full list of prerequisites.


## Installation

The easiest way to get up and running with the pipeline is to download the ready-to-use **virtual machine** box and run it with Vagrant.

Alternatively, it can be installed on Linux or macOS either with `pip`, or with the provided installation scripts.
_(**WARNING:** compiling the dependencies can take more than 6 hours.)_

#### 1) Download a pre-configured Virtual Machine

Please refer to the virtual machine [repository](https://github.com/maxperry/photometrypipeline-vm).

#### 2) Install on your machine from PyPI or git

* Run `sudo -H pip install photopipe` to install the latest stable version from [PyPI](https://pypi.python.org/pypi/photopipe). 

* Or clone from `git`:

 ```
 $ git clone git@github.com:maxperry/photometrypipeline.git
 $ cd photometrypipeline
 $ sudo python setup.py install
 ```
 
**NOTE (macOS)**: If the installation fails with `sudo: port: command not found` make sure that [MacPorts](https://guide.macports.org/#installing) is installed and `/opt/local/bin` is in the $PATH (e.g. `export PATH=/opt/local/bin:/opt/local/sbin:$PATH`).

#### 3) Manual Installation
If you to run the pipeline from the Python enviroment rather than using the `photopipe` command as described in the [Usage](#usage) section, please follow the step by step instructions in the wiki pages below to install all the dependencies manually.

* [Instructions for macOS](https://github.com/maxperry/photometrypipeline/wiki/Manual-Installation-(macOS))
* [Instructions for Linux-Debian](https://github.com/maxperry/photometrypipeline/wiki/Manual-Installation-(Linux-Debian))


## Usage

The following steps can be reproduced using the test data downloadable [here](https://drive.google.com/file/d/0BzMOBEOpFL9LaHpkWnFXc0IzRmM/view?usp=sharing), either from your local machine or from the virtual machine.

####1. Prepare the imaging data

 - Create a new folder with the following structure:
 
 ```
data  
│
└───bias
│   │   20160628T032914C0b.fits
│   │   20160628T032914C1b.fits
│   │   ...
│   
└───dark
│   │   20160628T040211C0d.fits
│   │   20160628T040211C1d.fits
│   │   ...   
│
└───flat
│   │   20160628T024207C0f.fits
│   │   20160628T024207C1f.fits
│   │   ...    
│
└───science
    │   20160628T043940C0o.fits
    │   20160628T043940C1o.fits
    │   ...    
```

## Bugs and Feedback

For bugs, questions and discussions please use the [Github Issues](https://github.com/maxperry/photometrypipeline/issues).


## License
This project is licensed under the GNU GPLv3 License - see the [LICENSE](https://github.com/scrapy/scrapy/blob/master/LICENSE) file for details.
