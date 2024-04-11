# Innovate 2024
## Overview

<add Innovate image here>
  
This repository contains materials created for, and presented at, SAS Innovate 2024. Materials for all of the sessions presented can be found in the corresponding folders. Information for all of the presented sessions can be found below.

## Getting Started with Computer Vision

This session consisted of an object detection demo and a segmentation demo. Relevant materials can be found in the folders of the same name.

### Modeling Objectives

The models in this notebook were developed as part of a Data for Good project with the UNC Center for Galapagos Studies to assist them with their sea turtle conservation efforts. The researchers want to allow tourists to upload pictures of any sea turtles they may find, see, or swim with. These images can then be used to identify whether a turtle is in an uploaded image. If a turtle is in an uploaded image, we can then try to identify whether that turtle has been previously tagged (known) or not (unknown). Identifying whether the turtle is known or unknown is useful to the researchers since they can use the image metadata to track the turtles, and any groups they may be traveling with, and provide them with healthcare if necessary.

### Object Detection Demo

In the object detection demo notebook, a YOLOv2 model is trained to detect humans and turtles in images. The primary objective of the object detection model in this process is to identify if turtles appear in the input images and the image coordinates in which they appear. The predicted bounding box locations can be used to crop an image. This cropped image can eventually be passed to a keypoint detection model where potential turtle matches can be identified. A secondary objective of this model is detecting whether humans appear in images. This is useful because images containing humans can be deleted entirely (especially if no turtle is present in the image) or removed from the images automatically for privacy reasons. 

### Segmentation Demo

In the segmentation demo notebook a UNet model is trained to classify pixels to separate turtles from the rest of the background. The objective of this model is to remove noise from an image containing a detected turtle. The scales in the face of turtles are unique, similar to human fingerprints. By keeping only turtle faces, we eliminate the possibility of background objects affecting the keypoint detection model that identifies if there is a match for a given turtle. 

## Getting Started with Generative AI

### Generating Synthetic Tabular Data with Generative Adversarial Networks (GAN)

In the GAN demo notebook, a GAN is trained to generate synthetic tabular data. The synthetically generated data is based off of financial data. The dataset that is used to train the GAN comes from a company that offers their customers home equity loans. It contains customer information and whether a given customer defaulted on their requested loan or not. This dataset can be useful in machine learning tasks, so the synthetic data is used to build machine learning models that predict whether a customer defaults on their home equity loan or not. Synthetic data can be used for many different use cases which means that there are many ways to assess the usefulness of the data. In this demo, models are trained using the real dataset as well as the synthetic dataset, assessed on a real validation partition, and compared using a variety of assessment metrics.

### Classifying Text Messages Using a BERT Model

In the bert demo notebook a BERT model is used to classify text. BERT is an encoder only model based on the transformer architecture that can be used to learn the interrelatedness of words in a sequence. The last layer in the BERT model that predicts words is removed and replaced with a layer that can be used for classification. The BERT base and large models are pre-trained on 3.3B tokens, so there is already some level of language understanding in the pre-trained model. The BERT model can then be adapted to a given task by fine-tuning it with a desired dataset. In this notebook, the BERT model is fine-tuned on data containing real text messages and spam text messages so that the model can detect whether incoming text messages are real or spam. The fine-tuning is achieved by training the model on the supervised task with a gentle learning rate. 

**NOTE:** BERT model table cannot be provided via GitHub repository. Code allows users to train the model but a GPU is strongly recommended to replicate this demo.

## No Programming End-to-End Computer Vision Model Development



