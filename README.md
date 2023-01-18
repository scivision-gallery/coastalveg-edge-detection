<div align="center">
    <h1>Coastal Vegetation Edge Detection</h1>
</div>

<p align="center">
    <a href="https://github.com/scivision-gallery/coastalveg-edge-detection/blob/main/LICENSE">
        <img alt="License" src="https://img.shields.io/badge/License-MIT-yellow.svg">
    </a>
    <a href="https://mybinder.org/v2/gh/scivision-gallery/coastalveg-edge-detection/main?labpath=vedge_detector.ipynb">
        <img alt="Binder" src="https://mybinder.org/badge_logo.svg">
    </a>
    <a href="https://github.com/scivision-gallery/coastalveg-edge-detection/workflows/ci/badge.svg">
        <img alt="Continuous integration badge" src="https://github.com/scivision-gallery/coastalveg-edge-detection/workflows/ci/badge.svg">
    </a>
    <br/>
</p>

<p align="center">
  <img src="https://github.com/scivision-gallery/coastalveg-edge-detection/blob/main/figs/VEdge_detector_prediction_example.png?raw=true" 
        alt="VEdge_Detector prediction over a sample PlanetScope satellite" width="70%" align="center">
</p>

<p align="center">
    <em>
    VEdge_Detector prediction of coastal vegetation edge over a sample PlanetScope satellite image in Winterton, UK. 
    </em>
</p>

## Abstract
Recent advances in satellite imagery availability and spatial resolution are providing new opportunities for the rapid, cost-effective detection of a shoreline’s location and dynamics. [Rogers et al. (2021)](https://www.tandfonline.com/doi/abs/10.1080/01431161.2021.1897185?journalCode=tres20) advance in coastal vegetation monitoring by developing `VEdge_detector`, a tool to extract the coastal vegetation line from remote-sensing imagery, training a very deep convolutional neural network (holistically nested edge detection), to predict sequential vegetation line locations on annual to decadal timescales. The `VEdge_Detector` model was trained using Planet 3 – 5 m spatial resolution imagery. It has also detected vegetation edges in Landsat and Copernicus Sentinel imagery, although performance is not guaranteed. The tool cannot detect the vegetation edge in aerial imagery.

In this notebook, we demonstrate how `scivision` facilitates the discovery of the `VEdge_detector` model for differentiating between the coastal vegetation edge and other boundaries in remote sensing images. We pair the model with one of the matched data sources from the scivision data catalog, in this case some sample of satellite images (n=3) from different geographical areas (Suffolk, United Kingdom; Wilk auf Föhr, Germany; Varela, Guinea Bissau) provided within the VEdge model repository.

## How to run

The notebook is designed to be launched from Binder.
* Click the **Launch Binder** button at the top level of the repository

You may also download the notebook from GitHub to run it locally:
* Open your terminal
* Check your conda install with `conda --version`. If you don't have conda, install it by following these instructions (see [here](https://docs.conda.io/en/latest/miniconda.html))
* Clone the repository into your current folder `git clone https://github.com/scivision-gallery/coastalveg-edge-detection.git` 
* Move into the cloned repository, `cd coastalveg-edge-detection`
* Install the dependencies in a new environment `conda env create -f environment.yml`
* Activate the installed environment, `conda activate coastalvegedge-detection-scivision`
* Launch the jupyter interface of your preference, notebook, `jupyter notebook` or lab `jupyter lab`

## Acknowledgment 
This notebook was supported by [Rogers et al. (2021)](https://www.tandfonline.com/doi/abs/10.1080/01431161.2021.1897185?journalCode=tres20)'s research. The scivision team thanks the model maintainer and collaborators involved in the deployment of the `VEdge_detector` model, in particular [Martin Rogers](https://www.bas.ac.uk/profile/user_3491-2/) (British Antarctic Survey) for his feedback in the preparation of the scivision model plugin and sample images provided for this notebook.
