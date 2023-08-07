# DiT: Efficient Vision Transformers with Dynamic Token Routing


<!-- ## Description -->

In this paper, we propose a **data-dependent token routing** strategy to elaborate the routing paths of image tokens for Dynamic Vision Transformer, dubbed DiT. The proposed framework generates a data-dependent path per token, adapting to the object scales and visual discrimination of tokens. In feed-forward, the differentiable routing gates are designed to select the **scaling** paths and **feature transformation** paths for image tokens, leading to multi-path feature propagation. In this way, the impact of object scales and visual discrimination of image representation can be carefully tuned. Moreover, the computational cost can be further reduced by giving budget constraints to the routing gate and early-stopping of feature extraction.
 

## :calendar:  Schedule
- [ ] Release code and models of DiT(based on PVTv2)
- [ ] Release code and models of DiT(based on Swinv2)


## :dart:  Motivation
<img width="800" alt="image" src="https://raw.githubusercontent.com/Maycbj/DiT/main/figures/motivation.png">

* Given input image with different spatial scales, the proposed dynamic token routing adaptively selects the token-specific forward paths, including **dynamic-scaling** and **dynamic-depth** paths. In this way, scale-variant objects (e.g. football and children) may be activated on feature maps with appropriate resolutions. Meanwhile, the fine-grained tokens (e.g. children) require more elaborated procedures of feature extraction. 


## :gift:  Major Features 
<img width="800" alt="image" src="https://raw.githubusercontent.com/Maycbj/DiT/main/figures/method.png">

* The proposed dynamic token routing framework of DiT. Left: The routing space with layer L and max downsampling rate 1/32. Lines in green, orange, and gray are alternative paths for dynamic routing, which represent Transformer Block, Patch Embedding Block, and identity mapping layer, respectively.

##  :snowman:  Experiments 
* In experiments, our DiT achieves superior performance and favorable complexity/accuracy trade-offs than many SoTA methods on ImageNet classification, object detection, instance segmentation, and semantic segmentation. Particularly, the DiT-B5 obtains 84.8\% top-1 Acc on ImageNet with 10.3 GFLOPs, which is 1.0\% higher than that of the SoTA method with similar computational complexity. These extensive results demonstrate that DiT can serve as versatile backbones for various vision tasks.

## :eyes: Visualization 
<img width="800" alt="image" src="https://raw.githubusercontent.com/Maycbj/DiT/main/figures/visualization.png">

* Visualization of the dynamic tokens routing.

## 🎫 License
This project is released under the [Apache 2.0 license](LICENSE). 

