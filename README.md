# Improving-existing-segmentators-performance-with-zero-shot-segmentators
Improving existing segmentators performance with zero-shot segmentators

This repository stores the code for applying SAM as suggested in the paper.

The link for downloading the code for DeepLabV3+: https://github.com/LorisNanni/An-empirical-study-on-ensemble-of-segmentation-approaches
the link for PVT is https://github.com/DengPingFan/Polyp-PVT

! very important, you should comment the line (in PVT):

res = (res - res.min()) / (res.max() - res.min() + 1e-8)

otherwise you will always find a foreground region

see line 40 of https://github.com/DengPingFan/Polyp-PVT/blob/main/Test.py

you could comment that normalization also in the training set, e.g. if you use images without foreground pixels.
