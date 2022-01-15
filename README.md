# StyleEval
**[Tensorflow 2.6 update 1/15/2022]**

Please see the official [implementation](https://github.com/EndyWon/StyleEval) of the paper "[Evaluate and Improve the Quality of Neural Style Transfer](https://www.researchgate.net/publication/350184156_Evaluate_and_improve_the_quality_of_neural_style_transfer)" (CVIU 2021)

All credits to the researcher!


### Environment Implemented:
- Python 3.8
- TensorFlow 2.66
- Numpy 1.19.0
- CUDA 11.0

### Getting Started:

Step 1: clone this repo


`git clone https://github.com/EndyWon/StyleEval`  
`cd StyleEval`


Step 2: download pre-trained vgg19 model

`bash download_vgg19.sh`

### Quality Evaluation:

- Test on a single image pair

`python quality_criteria.py --content ContentImagePath --style StyleImagePath --stylized StylizedImagePath`

### MO-Net:

`python MONet.py --content inputs/Seth.jpg --style inputs/Gogh.jpg`

## Discussions

For **quality evaluation**, we tested images of size 512x512 on an Intel Core i7-5820K CPU @ 3.30GHz × 12, the average time is about 126 seconds. We found that the most time was spent on calculating LP scores (about 80 seconds).

Currently the evaluation time is too slow, one may consider using GPU convolution to accelerate the patch matching process in LP calculation.


## Citation:

If you find this code useful for your research, please cite the paper:

```
@article{wang2021evaluate,
  title={Evaluate and improve the quality of neural style transfer},
  author={Wang, Zhizhong and Zhao, Lei and Chen, Haibo and Zuo, Zhiwen and Li, Ailin and Xing, Wei and Lu, Dongming},
  journal={Computer Vision and Image Understanding},
  volume={207},
  pages={103203},
  year={2021},
  publisher={Elsevier}
}
```
