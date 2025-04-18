# 🔮 Readout Guidance: Learning Control from Diffusion Features (reproduced)
**Grace Luo, Trevor Darrell, Oliver Wang, Dan B Goldman, Aleksander Holynski**
## CVPR 2024 (Highlight)

## Releases
- 🚀 2024/04/26: Additional code for pose estimation with readout heads in the [readout_pose](readout_pose) directory.
- 🚀 2024/01/31: Initial codebase release with demos for drag-based manipulation and spatial control, as well as readout head training code. Includes weights for SDXL and SDv1-5 readout heads for appearance, correspondence, depth, edge, pose.

## Setup
This code was tested with Python 3.8. To install the necessary packages, please run:
```
conda env create -f environment.yml
conda activate readout
```

## Readout Heads
All model weights can be found on our [HuggingFace page](https://huggingface.co/g-luo/readout-guidance/tree/main/weights). To automatically download the weights run:
```
./download_weights.sh
```

| Readout Head Type| SDv1-5 | SDXL |
|----------|----------|----------|
| Pose Head | [download](https://huggingface.co/g-luo/readout-guidance/resolve/main/weights/readout_sdv15_spatial_pose.pt?download=true) | [download](https://huggingface.co/g-luo/readout-guidance/resolve/main/weights/readout_sdxl_spatial_pose.pt?download=true) |
| Depth Head | [download](https://huggingface.co/g-luo/readout-guidance/resolve/main/weights/readout_sdv15_spatial_depth.pt?download=true) | [download](https://huggingface.co/g-luo/readout-guidance/resolve/main/weights/readout_sdxl_spatial_depth.pt?download=true) |
| Edge Head | [download](https://huggingface.co/g-luo/readout-guidance/resolve/main/weights/readout_sdv15_spatial_edge.pt?download=true) | [download](https://huggingface.co/g-luo/readout-guidance/resolve/main/weights/readout_sdxl_spatial_edge.pt?download=true) |
| Correspondence Feature Head | [download](https://huggingface.co/g-luo/readout-guidance/resolve/main/weights/readout_sdv15_drag_correspondence.pt?download=true) | [download](https://huggingface.co/g-luo/readout-guidance/resolve/main/weights/readout_sdxl_drag_correspondence.pt?download=true) |
| Appearance Similarity Head | [download](https://huggingface.co/g-luo/readout-guidance/resolve/main/weights/readout_sdv15_drag_appearance.pt?download=true) | [download](https://huggingface.co/g-luo/readout-guidance/resolve/main/weights/readout_sdxl_drag_appearance.pt?download=true) |

## Demos
Note that the generation process is non-deterministic, even without Readout Guidance, so re-running the same cell or script with the exact same settings can yield better results.

- `demo_drag.ipynb`: This demo walks through drag-based manipulation on either real images or generated images, where the user can also annotate the desired drags.
- `demo_spatial.ipynb`: This demo walks through spatial control with the pose head on pose inputs derived from MSCOCO images.


## What I reproduced 

Dragging(reproduced)

``
drag_saqib.ipynb
``

Spatial(reproduced)

``
drag_spatial.ipynb
``

