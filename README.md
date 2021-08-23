# A Labelled Underwater Fish Dataset In Poor Visibility Conditions
[![Powered by](https://img.shields.io/badge/Powered%20by-FishID-green)](https://globalwetlandsproject.org/tools/fishid/)
![Status](https://img.shields.io/badge/Status-Completed-green)


# Table of Contents
1.  [Overview](#overview)
3.  [Uses](#uses)
4.  [Datasets](#datasets)
5.  [Species](#species)
6.  [Dataset Links](#dataset-links)
7.  [Attributions](#attributions)


## Overview
Here we provide an open-access and annotated baited underwater dataset of poor and fair visibility videos for the development of fish detection models and benchmarking of image pre-processing tools. We provide the annotated training annotations and images, and a 12 hour testing dataset with groundtruth MaxN abundance for four target species.


## Uses
This dataset can be used
1. As a computer vision training dataset to monitor estuarine fish in the eastern coast of Australia. 
2. As a benchmark dataset to test image pre-processing techniques (e.g. colour correction).
3. As a benchmark dataset to test image post-processing techniques (e.g. fish occlussion filters)
4. To supplement global fish detection models (e.g. see [MegaDetector by Microsoft](https://github.com/microsoft/CameraTraps/blob/master/megadetector.md))
5. To increase accessibility of underwater computer vision tools for aquatic monitoring and environmental science (e.g. see [lilascience](https://lila.science/))


## Datasets
We provide access to two datasets: training and testing dataset. 

The training dataset is a fully annotatated dataset that contains images, annotations and labels of various fish species. The training dataset includes videos from 2017-2021 of Moreton Bay, Australia across poor visibility secchi depths (2-5 m) from an standard baited underwater video rig with GoPro cameras recording at 1080p.

The testing dataset includes several non-annotated videos from the same location, visibility scenarios and period as the training dataset. The testing dataset can be used to evaluate computer vision fish detection models. The groundtruth is a csv that has manual maximum abundance counts of each fish species across each video. The maximum number of individuals per video were manually determined by researchers at the Moreton Bay Environmental Education Centre.

The training and testing dataset were collected by the [Moreton Bay Environmental Education Centre](https://moretoneec.eq.edu.au/).


## Species
The training dataset contains >65,000 segmentation mask annotations of 19 different estuarine fish species from Moreton Bay, Australia. We targeted four species for studies conducted at the [Global Wetlands Project](https://globalwetlandsproject.org/tools-2/fishid/). Therefore, these species have a larger number of annotations. We suggest caution when using annotations of the non-targeted species, as these were variably annotated across the dataset. [Please contact Sebastian Lopez-Marcano for more information](https://ecoseabass.wixsite.com/endlessocean)


| Species        | Num Annotations                                                                                  |Targeted species                                                                                        | 
|------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
|[Australasian Snapper](https://fishesofaustralia.net.au/home/species/678) | 9,489 | YES|
|[Bengal Sergeant](https://fishesofaustralia.net.au/home/species/306) | 277 | NO|
|[Black-Banded Trevally](https://fishesofaustralia.net.au/home/species/2991) | 89| NO|
|[Blue Catfish](https://fishesofaustralia.net.au/home/species/2141) | 2,411| NO|
|[Blue Swimmer Crab](https://australian.museum/learn/animals/crustaceans/blue-swimmer-crab/)|847|NO|
|[Eastern Striped Grunter](https://fishesofaustralia.net.au/home/species/698)|14,631|NO|
|[Eastern Stripey](https://fishesofaustralia.net.au/home/species/525)|307|NO|
|Echinoderm|14|NO|
|[Fanbelly Leatherjacket](https://fishesofaustralia.net.au/home/species/810)| 190| NO|
|[Gunthers Wrasse](https://fishesofaustralia.net.au/home/species/1255)| 603| NO|
|[Mackerel spp](https://fishesofaustralia.net.au/home/species/2544)|139|NO|
|[Moses Snapper](https://fishesofaustralia.net.au/home/species/566)| 53|NO|
|[Paradise Threadfin Bream](https://fishesofaustralia.net.au/home/species/615)|10,658|YES|
|[Pinkbanded Grubfish](https://fishesofaustralia.net.au/home/species/751)|502|NO|
|Pomacentrid spp|27|NO|
|[Remora spp](https://fishesofaustralia.net.au/home/species/4251)|41|NO|
|[Smallmouth Scad](https://fishesofaustralia.net.au/home/species/3712)|7,067|YES|
|[Smooth Golden Toadfish](https://fishesofaustralia.net.au/home/species/866)|5,014|YES|
|[Yellowfin Bream](https://fishesofaustralia.net.au/home/species/672) and [Tarwhine](https://fishesofaustralia.net.au/home/species/679)|11,872|NO|


## Dataset Links

| Dataset          | Raw Videos                                                                                        | Raw Images                                                                                         | Version | Num Annotations | Annotations (CSV/JSON)                                                                                     |
|------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|---------|-----------------|--------------------------------------------------------------------------------------------------|
| Training dataset | NA                                                                                               | [Download 555 MB](https://research-storage.griffith.edu.au/owncloud/index.php/s/9PMCoNEXVdJuXbH)                                                                              | 7       | 8,696           | [Download 19 MB](https://research-storage.griffith.edu.au/owncloud/index.php/s/9PMCoNEXVdJuXbH) |
| Testing dataset | [Download 6.5 GB](https://research-storage.griffith.edu.au/owncloud/index.php/s/cnK1vOP6jPzt8PU) | NA | 1       | NA          | [Groundtruth](https://research-storage.griffith.edu.au/owncloud/index.php/s/cnK1vOP6jPzt8PU)|



## Annotations
Each annotation includes object instance annotations which consists of the following key fields: Labels are provided as a common name: YellowfinBream for *Acanthopagrus australis*; bounding boxes that enclose the species in each frame are provided in "[x,y,width,height]" format, in pixel units; Segmentation masks which outline the species as a polygon are provided as a list of pixel coordinates in the format "9x,y,x,y,...]".

The corresponding image is provided as an image filename. All image coordinated (bounding box and segmentation masks) are measured from the top left mage corner and or 0-indexed.

Annotations are provided in both CSV format and COCO JSON format which is a commonly used data format for integration with object detection frameworks including PyTorch and TensorFlow. For more information on annotations files in COCO JSON and/or CSV formats go [here](https://github.com/globalwetlands/luderick-seagrass#coco-json).

## Attributions
To attribute this database, please include the following citation.
We kindly request that the following text be included in an acknowledgements section at the end of your publications:
"We would like to thank the Moreton Bay Environmental Education Centre for freely supplying us with the fish dataset for our research"
