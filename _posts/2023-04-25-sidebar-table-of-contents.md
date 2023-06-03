---
layout: post
title: The "DOORS" dataset
date: 2023-06-02 10:00:00-0000
description: DOORS in a nutshell
categories: dataset boulders segmentation regression
giscus_comments: true
related_posts: false
toc:
  sidebar: left
---

## What is "DOORS" ? 

DOORS stands for "Dataset fOr bOuldeRs Segmentation" and is an open-access dataset with single and multiple boulders rendered in Blender over the surface of a small body. You can download it <a href="https://zenodo.org/record/7107409"> here </a> on Zenodo.

Also, you can found a detailed description of the dataset <a href="https://arxiv.org/pdf/2210.16253.pdf"> here </a> on ArXiv.  What follows is a "description in a nutshell" of the dataset. 

## Why does it exists? 

Because the capability to detect boulders on the surface of small bodies is beneficial for vision-based applications such as hazard detection during critical operations and navigation. This task is challenging due to the wide assortment of irregular shapes, the characteristics of the boulders population, and the rapid variability in the illumination conditions. We believe that the lack of publicly available and labeled datasets for these applications damps the research on this particular area, thus, we have decided to release our internal dataset we have used in CITE HERE for anyone who wants to play with it. 

## How was it generated ?

In Blender. The dataset is comprised by two subsets: DS1 and DS2, that are made with slightly different settings. 

DS1 is made of 45269 image-label pairs in which a single boulder is represented in the image. The renderings are done in Blender using the following elements: 

1. A single randomly-generated boulder whose Center of Mass (CoM) is positioned in the center of the
Blender reference frame
2. A unitary spherical mesh made of 16’258 vertexes and 32’512 faces
3. A camera, modeled with a 256 × 256 px size sensor and a FOV of 10 × 10 deg
4. A Sun lamp illuminating the scene

DS2 is made of image-label pairs in which a multiple boulders are represented in the same image. The renderings are done in Blender using the following elements:

1. A medium resolution mesh of the (65803) Didymos asteroid made of 652’032 faces that represents the
surface
2. A particle system which scatters randomized populations of boulders from a collection of 30 samples across the surface
3. A camera, modeled with a 128 × 128 px size sensor and a FOV of 10 × 10 deg
4. A Sun lamp illuminating the scene

## Examples of what can you do with it 

In the original work for which the dataset has been designed, it has been used to perform:

-Centroid regression: Contains images, masks, and labels for 4 splits of single boulders positioned on the surface of a spherical mesh. It can be used to perform navigation, boulder recognition, segmentation, and centroid regression.

-boulder segmentation: Contain images, masks, and labels of 2 datasets: DS1 and DS2. DS1 is made of the same images of the Regression dataset but is specifically designed for segmentation. DS2 is made of images with multiple instances of boulders appearing on the surface of the Didymos asteroid model

However, we have included all sorts of labels that can be used for many other tasks such as: 


-navigation
-boulder recognition


## Do you want to use this dataset and don't know how to cite it? 

Mattia Pugliatti, & Francesco Topputo. (2022). DOORS: Dataset fOr bOuldeRs Segmentation (1.0) [Data set]. Zenodo. https://doi.org/10.5281/zenodo.7107409

## Some statistics about DOORS

You can find a detailed characterization of the statistical properties of the DOORS dataset "DOORS: Dataset fOr bOuldeRs Segmentation. Statistical properties and Blender setup", by Mattia Pugliatti and Francesco Topputo, arXiv pre-print, Oct 2022 [<a href="https://arxiv.org/pdf/2210.16253.pdf"> link here </a> on ArXiv]


