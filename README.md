# PeopleSansPeople: A Synthetic Data Generator for Human-Centric Computer Vision, [arXiv](https://arxiv.org/abs/3940169)

<!-- Global site tag (gtag.js) - Google Analytics -->
<!--
<script async src="https://www.googletagmanager.com/gtag/js?id=G-ZCKG4HKTMK"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'G-ZCKG4HKTMK');
</script>
-->

<!--
### [Paper](https://arxiv.org/abs/3940169) &nbsp; [Source Code](https://github.com/Unity-Technologies/PeopleSansPeople) &nbsp; [macOS Binary](https://storage.googleapis.com/peoplesanspeople-gha-binaries/StandaloneOSX_39ff5eb9ab4ce79440a3f743ebeb4f7b3c967024.zip) &nbsp; [Linux Binary](https://storage.googleapis.com/peoplesanspeople-gha-binaries/StandaloneLinux64_39ff5eb9ab4ce79440a3f743ebeb4f7b3c967024.zip)
-->

<p align="center">
  <a href="https://arxiv.org/abs/3940169" style="font-size: 25px; text-decoration: none">Paper</a>
  &nbsp; &nbsp;
  <a href="https://github.com/Unity-Technologies/PeopleSansPeople" style="font-size: 25px; text-decoration: none">Source Code</a>
  &nbsp; &nbsp;
  <a href="https://storage.googleapis.com/peoplesanspeople-gha-binaries/StandaloneOSX_39ff5eb9ab4ce79440a3f743ebeb4f7b3c967024.zip" style="font-size: 25px; text-decoration: none">macOS Binary</a>
  &nbsp; &nbsp;
  <a href="https://storage.googleapis.com/peoplesanspeople-gha-binaries/StandaloneLinux64_39ff5eb9ab4ce79440a3f743ebeb4f7b3c967024.zip" style="font-size: 25px; text-decoration: none">Linux Binary</a>
</p>


<!--
<form action="https://arxiv.org/abs/3940169/" method="get" target="_blank"><button type="submit">Paper</button></form> &nbsp; <form action="https://github.com/Unity-Technologies/PeopleSansPeople/" method="get" target="_blank"><button type="submit">Source Code</button></form> &nbsp; <form action="https://github.com/Unity-Technologies/PeopleSansPeople/releases/download/v0.1.1/mac_0.1.1.zip" method="get" target="_blank"><button type="submit">macOS Binary</button></form> &nbsp; <form action="https://github.com/Unity-Technologies/PeopleSansPeople/releases/download/v0.1.1/linux_0.1.1.zip" method="get" target="_blank"><button type="submit">Linux Binary</button></form>
-->

<p align="center">
  <img src="./images/teaser_images/rgb_1528.png" width="20%" />

  <img src="./images/teaser_images/rgb_2711.png" width="20%" />

  <img src="./images/teaser_images/rgb_8687.png" width="20%" />
<br>
  <img src="./images/teaser_images/img__anns__1528.png" width="20%" />

  <img src="./images/teaser_images/img__anns__2711.png" width="20%" />

  <img src="./images/teaser_images/img__anns__8687.png" width="20%" />
<br>
  Top row: PeopleSansPeople generated images. 
<br>
  Bottom row: corresponding COCO-style bounding box and keypoint labels.
</p>

<!--
 &nbsp; &nbsp;
-->

<p align="center">
  <a href="https://www.linkedin.com/in/saleheerfanianebadi">Salehe Erfanian Ebadi</a>,
  <a href="https://www.linkedin.com/in/ycjhang">You-Cyuan Jhang</a>, 
  <a href="https://scholar.google.com/citations?user=2nA9bVMAAAAJ&hl=en&oi=ao">Alex Zook</a>, 
  <a href="https://www.linkedin.com/in/sauravdhakad/">Saurav Dhakad</a>, 
  <br>
  <a href="https://www.linkedin.com/in/adam-crespi-81b1287">Adam Crespi</a>,
  <a href="https://www.linkedin.com/in/pete-parisi-81a179">Pete Parisi</a>,
  <a href="https://www.linkedin.com/in/steve-borkman-5983325">Steven Borkman</a>,
  <a href="https://www.linkedin.com/in/jonathan-hogins-1952b919">Jonathan Hogins</a>,
  <a href="https://scholar.google.com/citations?hl=en&user=4XuOFfUAAAAJ">Sujoy Ganguly</a>
  <br>
  Unity Technologies
</p>

<!--
> **Authors:** Salehe Erfanian Ebadi, You-Cyuan Jhang, Alex Zook, Saurav Dhakad, Adam Crespi, Pete Parisi, Steven Borkman, Jonathan Hogins, Sujoy Ganguly
> <br />
> **Authors' affiliation:** Unity Technologies
> <br />
> **Submitted to:** NeurIPS 2021 Track Datasets and Benchmarks Round2
> <br />
> **Paper ID:** 54
-->

---

>
> ### *People + Sans (Middle English for “without”) + People*
> 
> #### A data generator for a few human-centric computer vision tasks without needing real-world human data.
> 

---

<img src="./images/unity/unity-wide-whiteback.png" align="middle" width="3000"/>

[![license badge](https://img.shields.io/badge/license-Apache--2.0-green.svg)](LICENSE.md)
&nbsp;
<img src="https://img.shields.io/badge/unity-2020.3.20f1-green.svg?style=flat-square" alt="unity 2020.3.20f1">
&nbsp;
<img src="https://badge-proxy.cds.internal.unity3d.com/5ab9a162-9dd0-4ba1-ba41-cf25378a927a?style=flat-square" alt="perception 0.9.0-preview.2">

---

## Summary
* We introduce PeopleSansPeople, a human-centric privacy-preserving synthetic data generator with highly parametrized domain randomization.
* PeopleSansPeople contains simulation-ready 3D human assets, a parameterized lighting and camera system, and generates 2D and 3D bounding box, 
instance and semantic segmentation, and COCO pose labels. 
* We use naïve ranges for the domain randomization and generate a synthetic dataset with labels. 
* We provide some guarantees and analysis of human activities, poses, and context diversity on our synthetic data.
* We found that pre-training a network using synthetic data and fine-tuning on target real-world data 
([COCO-person train](https://cocodataset.org/#home)) resulted in bbox AP of **57.44** and keypoint AP of **66.83** 
(COCO-person validation) outperforming models trained with the same real data alone (bbox AP of **56.73** and keypoint AP of **65.12**).

<details>
  <summary>Abstract (click to expand)</summary>
  
_In recent years, person detection and human pose estimation have made great strides, helped by large-scale labeled datasets.
However, these datasets had no guarantees or analysis of human activities, poses, or context diversity.
Additionally, privacy concerns may limit the ability to collect more data.
An emerging alternative to real-world data that alleviates some of these issues is synthetic data.
However, creation of synthetic data generators is incredibly challenging and prevents researchers from exploring their usefulness.
Therefore, we release a human-centric synthetic data generator PeopleSansPeople which contains simulation-ready 3D human assets,
a parameterized lighting and camera system, and generates 2D and 3D bounding box, instance and semantic segmentation, and COCO pose labels.
Using PeopleSansPeople, we performed benchmark synthetic data training using a
[Detectron2 Keypont R-CNN variant](https://github.com/facebookresearch/detectron2).
We found that pre-training a network using synthetic data and fine-tuning on target real-world data
([COCO-person train](https://cocodataset.org/#home)) resulted in bbox AP of **57.44** and keypoint AP of **66.83**
(COCO-person validation) outperforming models trained with the same real data alone (bbox AP of **56.73** and keypoint AP of **65.12**).
This freely available data generator should enable a wide range of research into the emerging field of simulation to
real transfer learning in the critical area of human-centric computer vision._
</details>

## What does PeopleSansPeople provide?
> * 28 parameterized simulation-ready 3D human assets
> * 39 diverse animation clips
> * 21,952 unique clothing textures (from 28 albedos, 28 masks, and 28 normals)
> * rameterized lighting
> * Parameterized camera system
> * Natural backgrounds
> * Primitive occluders/distractors
> * All packaged in a macOS and Linux binary

A comparison between PeopleSansPeople and the COCO person dataset.
<table><thead><tr><th> </th><th># train</th><th># validation</th><th># instances (train)</th><th># instances w/ kpts (train)</th></tr></thead><tbody><tr><td>COCO</td><td>64,115</td><td>2,693</td><td>262,465</td><td>149,813</td></tr><tr><td>PeopleSansPeople</td><td>490,000</td><td>10,000</td><td>&gt;3,070,000</td><td>&gt;2,900,000</td></tr></tbody></table>


## Generated data and labels
PeopleSansPeople produces the following types of labels in COCO format: 2D bounding box, human keypoints, semantic and instance segmentation masks.
In addition PeopleSansPeople generates 3D bounding boxes which are provided in [Unity's Perception](https://github.com/Unity-Technologies/com.unity.perception) format.
<p align="center">
  <img src="./images/label_fig/1.png" width="20%" />
  &nbsp; &nbsp;
  <img src="./images/label_fig/2.png" width="20%" />
  &nbsp; &nbsp;
  <img src="./images/label_fig/3.png" width="20%" />
  &nbsp; &nbsp;
  <img src="./images/label_fig/4.png" width="20%" />
  <br>
  Generated image and corresponding labels: 2D bounding box, human keypoints, semantic and instance segmentation masks in COCO format. 
  3D bounding box annotations are provided separately in [Unity Perception](https://github.com/Unity-Technologies/com.unity.perception) format.
</p>

## Results
Here we show a comparison of gains obtained from pre-training on our synthetic data and fune-tuning on COCO person class
over training from scratch on COCO. For each dataset size we show the results of the best performing model.

<table><thead><tr><th></th><th colspan="3">bbox AP</th><th colspan="3">keypoint AP</th></tr></thead><tbody><tr><td>size of real data</td><td>scratch</td><td>w/ pre-train</td><td>Δ</td><td>scratch</td><td>w/ pre-train</td><td>Δ</td></tr><tr><td>641</td><td>13.82</td><td>42.58</td><td>+28.76</td><td>7.47</td><td>46.40</td><td>+38.93</td></tr><tr><td>6411</td><td>37.82</td><td>49.04</td><td>+11.22</td><td>39.48</td><td>55.21</td><td>+15.73</td></tr><tr><td>32057</td><td>52.15</td><td>55.04</td><td>+2.89</td><td>58.68</td><td>63.38</td><td>+4.70</td></tr><tr><td>64115</td><td>56.73</td><td>57.44</td><td>+0.71</td><td>65.12</td><td>66.83</td><td>+1.71</td></tr></tbody></table>

## Unity Shader Graph randomizer for simulated clothing appearance diversity
<p align="center">
  <img src="./images/shadergraph_renderpeople/renderpeople_material.png" width="80%" />
  <br>
  <img src="./images/shadergraph_renderpeople/renderpeople_shader.png" width="80%" />
  <br>
  Top row: our 3D human assets from RenderPeople with their original clothing textures.
  <br>
  Bottom row: using Shader Graph randomizers we are able to swap out clothing texture albedos, masks, and normals,
  yielding very diverse-looking textures on the clothing, without needing to swap out the clothing items themselves.
</p>

## Additional examples
<p align="center">
  <img src="./images/more_examples/rgb_100.png" width="14%" />

  <img src="./images/more_examples/rgb_159.png" width="14%" />

  <img src="./images/more_examples/rgb_168.png" width="14%" />
  
  <img src="./images/more_examples/rgb_392.png" width="14%" />
  
  <img src="./images/more_examples/rgb_582.png" width="14%" />
  
  <img src="./images/more_examples/rgb_801.png" width="14%" /> 
<br>
  <img src="./images/more_examples/rgb_978.png" width="14%" />

  <img src="./images/more_examples/rgb_1281.png" width="14%" />

  <img src="./images/more_examples/rgb_1462.png" width="14%" />
  
  <img src="./images/more_examples/rgb_2178.png" width="14%" />
  
  <img src="./images/more_examples/rgb_2243.png" width="14%" />
  
  <img src="./images/more_examples/rgb_2291.png" width="14%" /> 
<br>
  <img src="./images/more_examples/rgb_2881.png" width="14%" />

  <img src="./images/more_examples/rgb_3099.png" width="14%" />

  <img src="./images/more_examples/rgb_3335.png" width="14%" />
  
  <img src="./images/more_examples/rgb_3877.png" width="14%" />
  
  <img src="./images/more_examples/rgb_4257.png" width="14%" />
  
  <img src="./images/more_examples/rgb_4531.png" width="14%" /> 
<br>
  <img src="./images/more_examples/rgb_5420.png" width="14%" />

  <img src="./images/more_examples/rgb_5789.png" width="14%" />

  <img src="./images/more_examples/rgb_5935.png" width="14%" />
  
  <img src="./images/more_examples/rgb_5944.png" width="14%" />
  
  <img src="./images/more_examples/rgb_6339.png" width="14%" />
  
  <img src="./images/more_examples/rgb_6352.png" width="14%" /> 
<br>
  <img src="./images/more_examples/rgb_7491.png" width="14%" />

  <img src="./images/more_examples/rgb_7638.png" width="14%" />

  <img src="./images/more_examples/rgb_7763.png" width="14%" />
  
  <img src="./images/more_examples/rgb_8023.png" width="14%" />
  
  <img src="./images/more_examples/rgb_8867.png" width="14%" />
  
  <img src="./images/more_examples/rgb_8981.png" width="14%" /> 
<br>
  <img src="./images/more_examples/rgb_9265.png" width="14%" />

  <img src="./images/more_examples/rgb_9383.png" width="14%" />

  <img src="./images/more_examples/rgb_9471.png" width="14%" />
  
  <img src="./images/more_examples/rgb_9480.png" width="14%" />
  
  <img src="./images/more_examples/rgb_9591.png" width="14%" />
  
  <img src="./images/more_examples/rgb_9983.png" width="14%" /> 
<br>
  Additional images generated with PeopleSansPeople. 
  Notice the high diversity of lighting, camera perspectives, scene background and occluders, as well as human poses, 
  their proximity to each other and the camera, and the clothing texture variations. Our domain randomization is done 
  here with naïvely-chosen ranges with uniform distributions. It is possible to drastically change the look and the 
  structure of the scenes by varying the randomizer parameters.
</p>



## Citation
```
@article{ebadi2021peoplesanspeople,
    title={PeopleSansPeople: A Synthetic Data Generator for Human-Centric Computer Vision},
    author={Salehe Erfanian Ebadi and You-Cyuan Jhang and Alex Zook and Saurav Dhakad 
            and Adam Crespi and Pete Parisi and Steven Borkman and Jonathan Hogins and Sujoy Ganguly},
    journal={arXiv},
    year={2021}
}
```

## Source code
Code is available [here](<https://github.com/Unity-Technologies/PeopleSansPeople/>)

Unity Environment Template [coming soon](<https://github.com/Unity-Technologies/PeopleSansPeople/>)

Unity Tutorial [coming soon](<https://github.com/Unity-Technologies/PeopleSansPeople/>)


## Related links
- [Unity's Perception Package](https://github.com/Unity-Technologies/com.unity.perception)
- [Unity Computer Vision](https://unity.com/products/computer-vision)
- [Unity's Perception Tutorial](https://github.com/Unity-Technologies/com.unity.perception/blob/master/com.unity.perception/Documentation~/Tutorial/TUTORIAL.md)
- [Unity's Human Pose Labeling and Randomization Tutorial](https://github.com/Unity-Technologies/com.unity.perception/blob/master/com.unity.perception/Documentation~/HPTutorial/TUTORIAL.md)
- [SynthDet Project](https://github.com/Unity-Technologies/SynthDet)
- [Robotics Object Pose Estimation Demo](https://github.com/Unity-Technologies/Robotics-Object-Pose-Estimation)
- [Unity Simulation Smart Camera Outdoor Example](https://github.com/Unity-Technologies/Unity-Simulation-Smart-Camera-Outdoor)


## License
PeopleSansPeople is licensed under the Apache License, Version 2.0. See [LICENSE](LICENSE.md) for the full license text.
