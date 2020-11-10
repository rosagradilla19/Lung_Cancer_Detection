# Lung_Cancer_Detection

The goal of this project is to take three-dimensional CT scans of human torsos 
to detect the location of suspected malignant tumors, if any exist within the lungs.

Methodology:

1. Load raw CT scan data into a form that is interpretable by PyTorch.
2. Identify voxels of potential tumors via segmentation
3. Group interesting voxels into lumps: here we will find the rough center of each hotspot.
4. Classify(nodule/non-nodule) candidate nodules using 3D convolution.
5. Diagnose using the combined per-nodule classifications: determine whether nodule is benign or malignant

Dataset: https://luna16.grand-challenge.org/download/
