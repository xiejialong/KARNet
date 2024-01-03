---
title: 'Listen, Perceive, Grasp: CLIP-driven attribute-aware network for language-conditioned visual segmentation and grasping'
authors: Jialong Xie, Jin Liu, Saike Huang, Chaoqun Wang, and Fengyu Zhou
affiliations: Shandong University
abstract: Endowing robots with the ability to understand natural language and execute grasping is a challenging task in a human-centric environment. Existing works on language-conditioned grasping achieve end-to-end grasping detection based on language. However, these works lack fine-grained visual grounding, resulting in cognitive deficits for robots. Moreover, they ignore the correlation between visual attributes of objects and grasping, leading to coarse grasp poses. To this end, we propose a CLIP-driven aTtribute-aware network (CTNet) for language-conditioned visual segmentation and grasping, enabling the robots to listen, perceive, and grasp the referred object in real-world applications. Specifically, we first employ Listen stage to understand basic linguistic and visual concepts. Subsequently, we introduce Perceive stage to mine multi-modal features and visual attribute cues (e.g., boundary and spatial location), then yield a language-conditioned segmentation mask. Further, we design Grasp stage to aggregate the perceived attribute information and refine the spatial location and grasping rectangle, generating a high-quality grasp pose. Lastly, we provide an extended large dataset Ref-OCID-Grasp to train and test our method, achieving a grasping accuracy of 97.76%  and segmentation OIoU of 91.82%. The real-world robotic applications demonstrate the effectiveness of our proposed approach.
videoid: _7ieXE7Xms8
github: https://github.com/xiejialong/CTNet.git
---

## The *listen-perceive-grasp* paradigm for robotic grasp reasoning
The listen-perceive-grasp paradigm for robotic grasp reasoning. Given a natural language description of a desired object in the scene, a human is able to adeptly listen for the gist of the description and understand linguistic and visual concepts, then perceive and delimit the referred object, and ultimately grasp the target by factoring in the physical attribute such as shape, scale, and spatial location. This process is similarly applicable to robots. The visual attributes serve to constrain the both width and position of the grasping rectangle, thereby preventing collisions with other objects in the clutter.
![listen-perceive-grasp paradigm](./images/Schematic.jpg)


## Overview of CTNet
An overview of CTNet architecture. Given an image-query pair, we first employ listen module to understand and align visual and linguistic concepts. Then, the perceive module recursively extracts object-orientied features with visual attributes and generates the target mask corresponding to the description. Last,  The grasp module aggregates the attribute-based and semantic-rich features to refine the grasp pose of the desired object.
![listen-perceive-grasp paradigm](./images/architecture.jpg)


## Dataset examples
In order to train the proposed method to perceive and grasp the specific target corresponding to the language, we introduce a RefOCIDGrasp dataset based on [OCID](https://www.acin.tuwien.ac.at/en/vision-for-robotics/software-tools/object-clutter-indoor-dataset/), [OCID-grasp](https://github.com/stefan-ainetter/grasp_det_seg_cnn), and [OCID-Ref](https://github.com/lluma/OCID-Ref)  datasets.
![Dataset Examples](./images/examples.jpg)

## Qualitative results
Qualitative results of our proposed method for different objects under different or same scenes.
![Visualization](./images/visualization.jpg)
