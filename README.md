
**Quick note to the reader**

This material has been prepared for the Nordic Remote Sensing 2019 conference with everything set up beforehand. We encourage you to run the tutorial by yourself, but please have a look at the "Running the tutorial with your Sentinel Hub account" section below, which should help you with the setup. We will be happy to hear back from you; feedback is welcome. 

## Abstract

Extracting valuable information from satellite imagery is challenging primarily due to large amounts of data. On top of that, there is a big lack of techniques allowing for automatic detection and extraction of complex patterns in such spatiotemporal data. Join us to see how we leverage [`eo-learn`](https://eo-learn.readthedocs.io/en/latest/) to obtain meaningful information from satellite data with just a few lines of Python code.


## Description


The availability of open Earth observation (EO) data through the Copernicus and Landsat programs, as well as plethora of commercially available satellite imagery, represents an unprecedented resource for many EO applications, ranging from ocean and land use/land cover monitoring to disaster control, emergency services and humanitarian relief. Large amounts of such spatiotemporal data call for tools that are able to automatically extract complex patterns embedded inside.

`eo-learn` is a collection of open source Python packages that have been developed to seamlessly access and process spatio-temporal satellite imagery in a timely and automatic manner. It makes the extraction of valuable information from satellite imagery as easy as defining a sequence of operations to be performed on satellite imagery. It also encourages collaboration --- the tasks and workflows can be shared, thus allowing for community-driven ways to exploit EO data.

The `eo-learn` library acts as a bridge between the Earth Observation (EO)/Remote Sensing (RS) field and the Python ecosystem for data science and machine learning. It lowers the entry barrier to the field of RS for non-experts and simultaneously brings the state-of-the-art tools for computer vision, machine learning, and deep learning existing in Python ecosystem to remote sensing experts.

During the workshop we will introduce the `eo-learn` framework, show examples of tasks dealing with retrieving the EO data (e.g. Sentinel-2, Sentinel-1, DEM), processing it, adding non-EO data (e.g. labels) to the dataset etc. and finally build the whole pipeline to run such workflow for larger areas, thus preparing the data for ML algorithms.


## Installation notes


**Follow the workshop with just your browser?**   
You can use the "launch binder" link above at the top of this README, which will launch a notebook instance on Binder with all required libraries installed.


**Work on your own computer?**  
In case you have some time on your hands and would like to work through the exercises on your machine, the minimal requirements are
+ eo-learn (please see [installation instructions](https://eo-learn.readthedocs.io/en/latest/install.html))
+ [jupyter](https://jupyter.org/install)

At the moment the recommended way is using a virtual environment (`venv`, i.e. `python3.6 -m venv eo-learn-workshop`) or `pipenv` Installing with `conda` might prove problematic. On Linux it is recommended to install system packages from  [CI build instructions](https://github.com/sentinel-hub/eo-learn/blob/master/.travis.yml#L12) first.

Alternatively, create a new environment for this tutorial using the provided environment.yml file:

```
conda env create --name eo-learn-workshop --file environment.yml
conda activate eo-learn-workshop
```


## Downloading the tutorial materials

**Note**: *We'd like to make this repository a "living" tutorial, so we will be updating the materials with the new versions and new functionalities of the `eo-learn` package. To update your local copy, you can download the latest version again, or do a `git pull` if you are using git.*

If you have git installed, you can get the tutorial materials by cloning this repo:

```
git clone https://github.com/sentinel-hub/eo-learn-workshop.git
```

Otherwise, you can download the repository as a .zip file by heading over
to the GitHub repository (https://github.com/sentinel-hub/eo-learn-workshop) in
your browser and click the green "Download" button in the upper right:

<img src="images/download-button.png" alt="download button" width="450">


## Running the tutorial with your Sentinel Hub account

**Note**: *During the workshop, we have provided a Sentinel-Hub account for the participants. If you are trying to run the tutorial by yourself, please follow these instructions.*

It is possible to run the tutorial using your own Sentinel-Hub credentials. In order to do that, there are a few instructions you have to follow:

* if you don't have a Sentinel Hub account, you can create a trial account for free [here](https://www.sentinel-hub.com/trial)
* once you have the account set up, login to Sentinel Hub [Configurator](https://apps.sentinel-hub.com/configurator/). By default you will already have the default confoguration with an instance ID (alpha-numeric code of length 36). For these examples it is recommended that you create a new configuration ("Add new configuration") and set the configuration to be based on `eo-learn workshop template`. The configuration already contains all layers used in this workshop. 
* insert the `instanceId` into the `introduction.ipynb` notebook, as shown here:
<img src="images/instance_id.png" alt="your instance id goes here" width="550">


## Authors

EO Research team at Sinergise (<eoresearch@sinergise.com>).
