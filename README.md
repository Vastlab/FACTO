# PEACH: Provable Extreme-value Agglomerative Clustering-threshold Estimation (PEACE) is applied to a classical Agglomerative Clustering of Hierarchies, we call the resulting algorithm PEACH.



# Abstract
PEACH clustering presents an Extreme Value Theory-based approach to threshold selection for clustering, proving that the "correct" linkage distances must follow a Weibull distribution for smooth feature spaces. Deep networks and their associated deep features have transformed many aspects of learning, and this paper shows they are consistent with our extreme-linkage theory and provide Unreasonable Clusterability.
We show how our novel threshold selection can be applied to both classic agglomerative clustering and the more recent FINCH (First Integer Neighbor Clustering Hierarchy) algorithm. Our evaluation utilizes over a dozen different large-scale vision datasets/subsets, including multiple face-clustering datasets and ImageNet for both in-domain and, more importantly, out-of-domain object clustering. Across  multiple deep features clustering tasks with very different characteristics, our novel automated threshold selection performs well, often outperforming state-of-the-art clustering techniques even when they select parameters on the test set.

This is release for non-commerical use with attribution (CC BY-NC-ND 4.0 https://creativecommons.org/licenses/by-nc-nd/4.0/) and 
This algorith/code is patent-pending. 
For attribtuion please cite  
@article{li2022agglomerative,
  title={Agglomerative Clustering with Threshold Optimization via Extreme Value Theory},
  author={Li, Chunchun and G{\"u}nther, Manuel and Dhamija, Akshay Raj and Cruz, Steve and Jafarzadeh, Mohsen and Ahmad, Touqeer and Boult, Terrance E},
  journal={Algorithms},
  volume={15},
  number={5},
  pages={170},
  year={2022},
  
  publisher={MDPI}
}  or one of our later works if combining it with them.in your publications if it helps your research::



# System Overview

![peach_paper](https://user-images.githubusercontent.com/20711687/206747297-171a1e57-c69b-49f2-8618-8bafc1f562df.jpg)

This figure shows the overall pipeline of PEACH. First, we extract deep features, then we compute the initial pairs, $median \{d({\cal S})\}$ and $max \{d({\cal S})\}$ for the EVT Estimation to compute the threshold $\tau_r$ / $\tau_w$. Next, we use the nearest neighbors to generate initial clusters and the $\tau_r$ / $\tau_w$ will be used for merging to obtain final clustered data.


# Usuage
PEACH Autonomous Clustering

Uses sode from Pytorch and Flann

Requirement: Python3, Pytorch, PyFlann, Scikit-learn, SciPy.

Python Flann: "pip install pyflann-py3"

Example MNIST: "python example.py" 

Set "no_singleton = True" will cluster all samples (and take longer).

Set metric = "euclidean" will use Euclidean distance, default is Cosine.

