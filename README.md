# OBMO

## Abstract
Compared to typical multi-sensor systems, monocular 3D object detection has attracted much attention due to its simple configuration. However, there is still a significant gap between LiDAR-based and monocular-based methods. In this paper, we empirically find that the ill-posed nature of monocular imagery can lead to depth ambiguity. Specifically, objects with different depths can appear with the same bounding boxes and similar visual features in the 2D image. Unfortunately, the network cannot accurately distinguish different depths from such non-discriminatory visual features, resulting in unstable depth training.To facilitate depth learning, we propose a simple yet effective plug-and-play module, **O**ne **B**ounding Box **M**ultiple **O**bjects (OBMO). Concretely, we add a set of suitable pseudo-3D labels by shifting the depth for each original 3D bounding box and carefully design a scoring strategy to represent their qualities.In contrast to original hard depth labels, such soft pseudo labels allow the network to learn a reasonable depth range, boosting training stability and thus improving final performance. Extensive experiments on KITTI and Waymo benchmarks show that our method significantly improves state-of-the-art monocular 3D detectors by a significant margin (The improvements under the moderate setting on KITTI validation set are **$1.82\sim 10.91\%$ mAP in BEV and $1.18\sim 9.36\%$ mAP in 3D**). Codes will be available.

## Codes
The OBMO module embedded in PatchNet is at [https://github.com/mrsempress/OBMO_GUPNet](https://github.com/mrsempress/OBMO_patchnet/).

The OBMO module embedded in GUPNet is at [https://github.com/mrsempress/OBMO_GUPNet](https://github.com/mrsempress/OBMO_GUPNet/).
