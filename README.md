# VET-IndoorDataset

3D reconstruction of the scene | 3D virtualization using VET
:-------------------------:|:-------------------------:
|![Figure 1](./Images/room_cut.png)|![Figure 2](./Images/final_scene_VR.png)|

[![License](https://img.shields.io/badge/License-MIT-blue.svg)](https://github.com/Pamogar/VET-IndoorDataset/blob/main/LICENSE.txt)

## Overview
VET-IndoorDataset is an open-source dataset that complements and is similar to the ScanNet dataset. It consists of multiple scenes with the
sensor data in a .sens file, containing the RGB-D images, the camera pose information and the camera intrinsics information, all the necessary information to generate a 3D reconstruction.
We recommend the use of ScanNet [SensReader](https://github.com/ScanNet/ScanNet/tree/master/SensReader) to read this files. Additionally, this
dataset contains an extra scene with the different steps of the virtualization, specifically: 3D reconstruction, 3D semantic
segmentation, 3D instance segmentation and CAD alignment + layout. The dataset focuses on indoor
environments of various sizes and types, providing valuable resources for computer vision and robotics research.

This README provides an overview of the dataset and instructions for accessing it.


## Original Paper
For detailed information about the dataset and the framework presented with it, please refer to the original paper (Currently on review):
- Virtual Experience Toolkit: An End-to-End Automated 3D Scene Virtualization Framework implementing Computer Vision Techniques

Temporarily, please refer to the conference publication:
- [Virtual Experience Toolkit: Enhancing 3D Scene Virtualization From Real Environments Through Computer Vision and Deep Learning Techniques](https://ieeexplore.ieee.org/abstract/document/10405757)

## Contents
The dataset consists of 30 indoor scenes, specifically, 2 bathrooms, 4 storage rooms, 1 pizzeria, 4 living rooms, 1 bedroom, 1 kitchen, 1 i+d lab, 3 offices, 1 clothing store, and 12 meeting rooms.
For each room, the sensor data in .sens files is provided; it was captured with an Intel RealSense D415i through the BundleFusion app implemented in VET. Additionally, for the room_demo used in the results
of the original paper, we also provide the step-by-step virtualization results; more precisely, we provide the .ply file for the 3D reconstruction, the 3D semantic segmentation and the 3D instance 
segmentation, and a .fbx file for the CAD alignment + layout. Regarding the interpretation of these results, the 3D instance segmentation results represent every individual instance with a different random color,
and the 3D semantic segmentation results are color coded following the next image. 

![Figure 1](./Images/colors.png) 

The scenes dataset organization is as follows:

- room_demo
	- Sensor data (.sens file)
		- RGB-D images
		- Camera pose information
		- Camera intrinsics
  	- 3D reconstructed scene
	- 3D semantic segmentation
	- 3D instance segmentation
	- CAD alignment + Layout
 - room_XXXX_XX
 	- Sensor data (.sens file)
   		- RGB-D images
		- Camera pose information
		- Camera intrinsics

The CAD dataset is organized following the [ShapeNet](https://shapenet.org/) organization. It is divided in folders with ids that represent the type of objects, with individual folders for each model inside.
The dataset also contains a taxonomy.json file that links the class names to the ids.

## Accessing the Datasets
The VET-IndoorDataset is hosted on OneDrive due to the large size. You can access and download the scenes following the next link:

[Download VET-IndoorDataset from OneDrive](https://upvedues-my.sharepoint.com/:f:/g/personal/pamogar_upv_edu_es/EkXtIVKaAltNkaleXeFLfZABZpTvqg6BDXhUDPDmm410qw?e=45wBNp)

The VET-CAD-Dataset is hosted on OneDrive due to the large size. You can access and download the scenes following the next link:

[Download VET-CAD-Dataset from OneDrive](https://upvedues-my.sharepoint.com/:f:/g/personal/pamogar_upv_edu_es/Ev8i533sCsJMi_H4_Ghw0sUBHM1eB_q4gAidiUUITKRXiQ?e=FE5Ije)

## Citation
If you find VET-IndoorDataset or VET-CAD-Dataset useful for your research, please consider citing it:

```
Paper is now on review. The citation will be updated once the paper is published.
```

```
@INPROCEEDINGS{10405757,
  author={Garcia, Clara and Mora, Pau and Ortega, Mario and Ivorra, Eugenio and Valenza, Gaetano and Alcañiz, Mariano L.},
  booktitle={2023 IEEE International Conference on Metrology for eXtended Reality, Artificial Intelligence and Neural Engineering (MetroXRAINE)}, 
  title={Virtual Experience Toolkit: Enhancing 3D Scene Virtualization From Real Environments Through Computer Vision and Deep Learning Techniques}, 
  year={2023},
  volume={},
  number={},
  pages={694-699},
  keywords={Deep learning;Training;Computer vision;Solid modeling;Three-dimensional displays;Psychology;Virtualization;3D Scene Understanding;Indoor Scenes;Virtual Reality (VR);ScanNet;Scene Reconstruction},
  doi={10.1109/MetroXRAINE58569.2023.10405757}}
```

## License
This datasets are released under the [MIT License](https://github.com/Pamogar/VET-IndoorDataset/blob/main/LICENSE).


For any questions or concerns regarding the dataset, please feel free to contact the project maintainers.
