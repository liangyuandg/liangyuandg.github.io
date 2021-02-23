---
layout: single
permalink: /projects/
title: Some of My Projects
classes: single
modified: 5-28-2019
comments: false
---

I believe the power of computing and AI can shape the future of healthcare.
By working closely with physicians, I develop AI algorithms, and build AI-empowered systems that can either (1) enable physician's faster and more accurate diagnosis, or (2) increase patient's understanding about his/her health and treatments.


### OralViewer: Patient Education Tool for 3D Demonstration of Dental Surgeries
[*MICCAI2020, AAAI2021, IUI2021*]\
Patient-physician communication is a core requirement of patient-centered care.
Due to the complexity of dental surgeries and patient-dentist gap of expertise, conventional techniques are usually not effective for explaining surgical steps.
As such, we developed *the first* interactive tool that enables 3D demonstration of dental surgeries to promote patients’ understanding.

***Algorithm:***
To reflect patient's condition from common imaging, we developed *the first CNN for the 3D reconstruction of dental structure from 2D X-ray*.
The unique challenge is that shapes and spatial localization of multiple objects (teeth) should be estimated from their 2D projection.
To tackle, we decomposed the task into sub-tasks of teeth segmentation and patch-wise object reconstruction, and developed a random sampling strategy for the end-to-end optimization of CNN.
<figure class="one">
  <img src="../assets/images/OralViewer_algorithm.png" alt="my alt text"/>
</figure>

***System:***
We developed the tool with virtual dental instruments that are simple to operate and illustrative with *real-time effects* on reconstructed dental models.
The tool was implemented using OpenGL, JavaScript and three.js, and can run readily inside a modern browser.
<video width="100%" oncontextmenu="return false;" controls controlsList="nodownload" poster="../assets/images/OralViewer_teaser.png">
  <source src="../assets/images/OralViewer_demo.mp4" type="video/mp4">
</video>



### OralCam: A Smartphone Tool for Self-Awareness of Oral Health
[*CHI2020, Oral Disease*]\
Due to a lack of medical resources or oral health awareness, oral diseases are often left unexamined and untreated, affect-ing a large population worldwide.
With the advent of low-cost, sensor-equipped smartphones, mobile apps offer a promising possibility for promoting oral health.
We developed the first interactive tool that enables end-users’ self-examination of five common oral conditions (diseases or early disease signals) by taking smart-phone photos of oral cavity.

***Algorithm:***
We formulated the task as a combination of classification and detection based on the nature of each disease, and utilized the *Multi-Task Learning* to improve the model generalization.
Moreover, we went beyond the existing approaches that purely rely on the images;
instead, users can provide information (e.g., living habits) via a survey and annotations on the captured images, which serves as model priors with *feature fusion* and enhanced model accuracy.
<figure class="one">
  <img src="../assets/images/OralCam_algorithm.jpg" alt="my alt text"/>
</figure>

***System:***
We implemented the tool as a web application to run on any device with Vue and Flask.
We designed the tool to provide contextualized results with model attention reasoning from *Classification Activation Mapping*, and show results hierarchically to avoid information overload for layman users.
<video width="100%" oncontextmenu="return false;" controls controlsList="nodownload" poster="../assets/images/OralCam_teaser.png">
  <source src="../assets/images/OralCam_demo.mp4" type="video/mp4">
</video>


### Smart Reporting: A Radiologist's Reporting Tool for Fast Report Generation
[*MICCAI2019, ACML2020, Patent 17/006.590*]\
A physician is required to write a comprehensive and accurate report describing all the findings for each study, which is essentially time consuming.
To solve the problem, we developed the interactive tool that largely reduces reporting time (by up to 50%) with two key techniques:
(1) the automatic awareness of anatomies, and (2) the embedding of a medical knowledge graph.

***Algorithm:***
Automatic anatomy awareness enables a physician to interactively input a finding by clicking the region of interest on the study, and pre-fill certain report contents.
Existing anatomical segmentation CNNs are not robust to image variations caused by pathology and different scanning setups.
To tackle the issue, we proposed a general method to increase the robustness of CNNs with underlying anatomical invariances---incorporating probabilistic atlas priors as explicit constraints for predictions over a *locally-connected Conditional Random Field*.
The method achieved state-of-the-art accuracy on two brain segmentation benchmarks with significantly boosted robustness.
<figure class="one">
  <img src="../assets/images/SmartReporting_algorithm.jpg" alt="my alt text"/>
</figure>

***System:***
We developed the generic application in C++ and performed user testing.
A physician can input a finding by simply clicking the location, selecting a template with predefined entries and options, and making selection for most of time.
The tool collects all filled templates for a study, and automatically converts them into a readable medical report based on the knowledge graph.
<!-- <figure class="one">
  <img src="../assets/images/SmartReporting_demo.jpg" alt="my alt text"/>
</figure> -->
<video width="100%" oncontextmenu="return false;" controls controlsList="nodownload" poster="../assets/images/SmartReporting_teaser.png">
  <source src="../assets/images/SmartReporting.mp4" type="video/mp4">
</video>


### XPath: A Pathologist's Tool for Human-AI Collaborative Tumor Grading
We developed a human-AI collaborative tool for tumor grading based on histological images.
Different from existing tools simply provide an AI prediction, we increase (1) the system integrability by decomposing the grading as the joint analyses of multiple low-level criteria; and (2) the system transparence with hierarchically traceable evidence on demand.

***Algorithm:***
To provide AI predictions on the multiple criteria, we developed a backend image processing engine with a variety of *deep learning based and traditional feature based* models.
Tasks of detection, segmentation, and patch-wise classification were formulated by considering the nature of criteria.
<figure class="one">
  <img src="../assets/images/XPath_algorithm.jpg" alt="my alt text"/>
</figure>

***System:***
We developed a generic application with Electron.
The tool was designed to provide a hierarchical trace of evidence, which include a high-level computed grading, a mid-level samples with positive findings, and a low-level registered image locations in higher magnification.  
<video width="100%" oncontextmenu="return false;" controls controlsList="nodownload" poster="../assets/images/XPath_teaser.png">
  <source src="../assets/images/XPath_demo.mp4" type="video/mp4">
</video>