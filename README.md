# Image Segmentation using GrabCut
Implementation of GrabCut algorithm for Iterative Foreground Extraction using Iterated Graph Cuts from [Rother et al research paper](https://cvg.ethz.ch/teaching/cvl/2012/grabcut-siggraph04.pdf). 

The code takes an input image and follows these steps:
- It requires a bounding box to be drawn by the user to roughly segment out the foreground pixels.
- It runs an initial min-cut optimization using the provided annotation.
- The result of this optimization gives an initial segmentation.
- To further refine this segmentation, the user provides two kinds of strokes to aid the optimization
    - strokes on the background pixels
    - strokes on the foreground pixels
- The algorithm now utilizes this to refine the original segmentation.