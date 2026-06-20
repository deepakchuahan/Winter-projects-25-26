# EEG-Based P300 Speller

## Project Objective
The objective of this project is to build a real-time Brain-Computer Interface (BCI) speller based on the P300 Event-Related Potential (ERP) using OpenViBE. This project extends beyond the default classical Machine Learning pipeline by integrating customizable ML and Deep Learning models. 

## Workflow & Features
The project covers the complete workflow of EEG-based BCI systems:
* **Signal Acquisition & Preprocessing:** Handles event tagging, epoch extraction, band-pass filtering, artifact handling, baseline correction, and downsampling.
* **Feature Engineering:** Extracts time-domain samples and PCA/CSP features for P300 peak detection.
* **Classification Models:** 
  * Baseline classifiers including LDA and Logistic Regression.
  * Classical supervised ML models like SVM and Random Forest. The current Python implementation specifically utilizes Support Vector Classification (SVC).
  * Deep Learning integration using the EEGNet architecture tailored for ERP classification.
* **OpenViBE Integration:** Connects trained models with OpenViBE via Python Scripting Box or TCP/VRPN communication for a unified, real-time spelling interface.

## Dataset
The system utilizes the BNCI2014_009 dataset, accessed and loaded via the moabb library, representing raw EEG arrays for processing. 

## Dependencies
The environment requires the following core Python libraries:
* pandas==2.2.2
* mne==1.11.0
* moabb==1.5.0
* scikit-learn
* matplotlib
* seaborn
* numpy

## Final Deliverables
* A fully functional P300-based EEG speller system integrated into OpenViBE.
* A modular ML backend supporting plug-and-play functionality for SVM and EEGNet.
* Performance evaluations comparing model accuracy, latency, and Information Transfer Rate (ITR).
