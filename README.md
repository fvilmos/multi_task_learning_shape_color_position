# Multi Task Learning example for shape type, color, position detection

Implementation of a simple multi-task learner with 3 tasks (heads). Shares internal representation between different tasks (hard parameter sharing, see [2]) having the direct benefit of a lighter, faster model with less trainable parameters.

This implementation has ~195 k trainable parameters, compared to ~290 k  used for the same tasks with a multi-headed implementation, see [3]. Compared to [3] training samples and epochs are significantly increased, after 2k cycles position accuracy is ~84% while color and shape ~99%.  


#### Steps:

    Create toy database, generate shapes, color it
    Normalize the generated images
    Create the multi-task learner Keras functional model, train and test it



#### Model:
<p align="center"> 
  <img src="./info/mtl_model.png" alt="" width="480"></a>
</p>

#### Output:
<p align="center"> 
  <img src="./info/out1.png" alt="" width="1024"></a>
</p>

## Links

1. [keras](https://keras.io/)
2. [An Overview of Multi-Task Learning in Deep Neural Networks, arXiv:1706.05098 [cs.LG] ](https://arxiv.org/abs/1706.05098)
3. [Multi headed DNN predictor, detects object coordinates, color and shape type](https://github.com/fvilmos/shape_color_position_detection)

/Enjoy.
