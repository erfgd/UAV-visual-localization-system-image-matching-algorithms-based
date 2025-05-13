# UAV Visual Localization System Based on Image Matching Algorithms

## introduction 

The project implements a visual localization system for Unmanned Aerial Vehicles (UAVs) using state-of-the-art image matching algorithms, LoFTR and Omniglue. The system estimates the UAV's position by matching real-time onboard camera images with a pre-built map of the environment.

![Demo:](/demo/LoFTR_map_match_demo.png)

## results

When run on a dataset based on a real UAV flight, the autonomous localization system achieved a cumulative error of 10 meters over 2 minutes of flight.
![fly](/demo/fly.jpg)

### Technologies
Matching Algorithms:

    LoFTR – Detector-Free Local Feature Matching with Transformers
    Omniglue – Omnidirectional Local Feature Matching

Libs:

    General libs:
        numpy, pytorch, opencv-python, matplotlib
    Special libs
        for LoFTR - Kornia (since version 0.5.11), kornia_moons
        for OmniGLue - tensorflow (GPU version)

## Installation and use

'Flight1' from [this](https://zenodo.org/records/1244296) dataset was used in this work. To run and test system on this dataset you need to install 'Maps' and 'Flight1' directory to  this system folder

If you want to test system on another dataset - you need to change only 1 cell with dataset's parameters in project to use your dataset. 

```
git clone https://git.miem.hse.ru/nlkorolev/diplom/-/tree/master/
```
To use the OmniGlue version of system, you need to additionally install OmniGlue from from [its repository](https://github.com/google-research/omniglue)
