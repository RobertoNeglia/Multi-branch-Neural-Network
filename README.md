#  Differentiable Branching in Deep Networks for Fast Inference.
Project developed for the course "Advanced topics in Machine Learning" at Università della Svizzera Italiana.
The aim of the project is a reproducibility challenge of the paper ["Differentiable branching in deep networks for fast inference"](https://ieeexplore.ieee.org/document/9054209) by professor S. Scardapane et al., DIET Department, Sapienza University of Rome.

<br>

# Abstract
In recent years, one notable advancement in the deep learning field has been the introduction of
models that incorporate multiple auxiliary branches for early exiting during inference. This project
aims to reproduce the findings of a seminal paper that proposed a novel algorithm for end-to-end
training of neural networks, without having to fine-tune manually all the parameters of the auxiliary
branches. We will re-implement the algorithm as described in the paper and apply it to a range
of classification tasks, using the publicly available datasets that are also used in the original paper.
Through this reproducibility project, we aim to provide valuable insights into the practical applicability
and generalizability of the proposed algorithm in real-world classification tasks.

<br>

# Model Architecture 
We implemented the VGG-13 architecture. We did 4 structures: the standard vgg-13(baseline), then the B-net, the authors proposed methodology and then the authors proposed methodology with a different criterion we tried. <br>
<img width="412" alt="vgg13" src="https://github.com/RobertoNeglia/Multi-branch-Neural-Network/assets/44726422/09f4b6d3-b47f-46b6-9dc8-00b63ee7c866">

<br>

# Results
Table 1 shows the results of the test accuracy on the VGG-13 architecture using CIFAR10, CIFAR100 and CINIC10
datasets. Likewise to the paper, better test accuracy were obtained using the CIFAR10 dataset, then CINIC-10 and
the worst results for CIFAR-100. We achieved better results than the result stated in the paper for only dataset
CINIC-10. We were only able to obtain similar test accuracy to the one in the paper for cifar-10. We believe a number
of factor comes into play, such the paper not giving enough details for some of the architecture implementation they used. <br><br>
![Screenshot 2023-11-20 162903](https://github.com/RobertoNeglia/Multi-branch-Neural-Network/assets/44726422/2576e177-3e04-4ae8-b5b1-0e1e4f24fd65)

We wanted to go into more detail like shown in the paper, so we decided to detail the average test accuracy the inference time and the speed up based on the experiment of VGG-13 using CIFAR10 dataset. This is shown in
Table 2. We would like to emphasise that the reason our inference time differs from by a large amount is because of the difference in machine with the paper.<br><br>
![Screenshot 2023-11-20 163715](https://github.com/RobertoNeglia/Multi-branch-Neural-Network/assets/44726422/4ef54cfc-3bc8-48da-bf5c-c37e08883d28)

<br>

# References
@inproceedings{repoduPaper,<br>
  author={Scardapane, Simone and Comminiello, Danilo and Scarpiniti, Michele and Baccarelli, Enzo and Uncini, Aurelio},<br>
  booktitle={ICASSP 2020 - 2020 IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP)}, <br>
  title={Differentiable Branching In Deep Networks for Fast Inference}, <br>
  year={2020},<br>
  pages={4167-4171},<br>
  doi={10.1109/ICASSP40776.2020.9054209},<br>
  ISSN={2379-190X},<br>
  month={May}
}
