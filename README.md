# Semantic Segmentation Autonomous Wheelchair 

![clemson](https://user-images.githubusercontent.com/79725511/119871586-979cdb80-bef0-11eb-91f0-a9ae0734c28e.png) 
> Clemson University Core Campus Precinct

---

### Table of Contents

- [Description](#description)
- [Technologies](#technologies)
- [Results](#results)
- [Recommendations](#recommendations)
- [References](#references)
- [License](#license)
- [Author Info](#author-info)

---

## Description

Wheelchairs are commonly used when walking is difficult or impossible due to illness, injury, problems related to old age, or disability. There are manual wheelchairs and power-driven electric wheelchairs currently in use. As autonomy becomes popular, the integration of autonomous driving with wheelchair systems will be a new trending topic. In this paper, some AI-based solutions/methods are utilized on the electric wheelchair system, demonstrating the potential of applying AI-based autonomy on other wheelchair systems. This work consisted of three parts; 1) A study on control of the wheelchair with the use of a RaspberryPi and object detection for the wheelchair - George, 2) Semantic Segmentation of indoor and outdoor images captured by the wheelchair camera - Venkat, and 3) Implementation of a SLAM solution on the wheelchair - Zack.

Semantic Segmentation (My Contribution):
The CNN models trained for image classification contain information that is useful for segmentation. ResNet or VGG pre-trained is a popular choice for the encoder. In this study, I have used pre-trained ResNet50 dilated architecture for the encoder. And for the decoder, a pre-trained Pyramid Scene Parsing Network (PSPNet) is used. Both the encoder (ResNet50) and decoder (Pyramid Pooling Module (PPM)) were pre-trained on the MIT ADE20K dataset. The dataset contains 20,210 images in the training set, 2,000 images in the validation set, and 3,000 images in the testing set. It has 150 classes of objects and stuff that includes indoor as well as outdoor objects. The overall implementation of the segmentation model is done using the PyTorch framework on the Google Colaboratory. 

![semanticsegmentation](https://user-images.githubusercontent.com/79725511/119871212-3aa12580-bef0-11eb-9923-12b02411b043.png)
> Image source: https://miro.medium.com/max/2122/1*s4MMIUF0QECVP0UGQWzhxg.png

### Classes with color code:

![Classes_with_color_code](https://user-images.githubusercontent.com/79725511/119874027-3296b500-bef3-11eb-9830-52fd68b148c3.png) 

### Performance data for different models:

![Performance_data](https://user-images.githubusercontent.com/79725511/119874028-3296b500-bef3-11eb-9bc6-bf64b49d29b1.png)


## Technologies

- Python
- PyTorch
- CNN
- Transfer learning
- MIT ADE20K dataset

---

## Results

#### 1) Segmentation map for the outdoor images obtained from the wheelchair camera:

![frame1](https://user-images.githubusercontent.com/79725511/119871199-383ecb80-bef0-11eb-9ee1-f1a75d4171a2.png)

![frame3](https://user-images.githubusercontent.com/79725511/119871202-38d76200-bef0-11eb-9260-20dc54b608a0.png)

![frame5](https://user-images.githubusercontent.com/79725511/119871203-38d76200-bef0-11eb-87c1-9330881ab2a0.png)

#### 2) Segmentation map for the indoor images obtained from the wheelchair camera:

![frame7](https://user-images.githubusercontent.com/79725511/119871205-396ff880-bef0-11eb-958c-9c3039bbe5be.png)

![frame8](https://user-images.githubusercontent.com/79725511/119871207-396ff880-bef0-11eb-90d3-46b8cbd89337.png)

![frame10](https://user-images.githubusercontent.com/79725511/119871208-3a088f00-bef0-11eb-859a-c46e3c3bb659.png)

#### 3) Segmentation map for the traffic images obtained from Google:

![traffic](https://user-images.githubusercontent.com/79725511/119871213-3aa12580-bef0-11eb-8420-68336d9939f2.png)

![traffic3](https://user-images.githubusercontent.com/79725511/119871219-3bd25280-bef0-11eb-94ad-0cfd4b2a843a.png)

![trafficsign](https://user-images.githubusercontent.com/79725511/119871223-3c6ae900-bef0-11eb-9836-cdae587fcba8.png)

![road](https://user-images.githubusercontent.com/79725511/119871210-3a088f00-bef0-11eb-8285-711f45a0412b.png)


If you would like to know the complete technical details of the project. Here is the [link](https://drive.google.com/file/d/1utWl3SOhXQZU2aVWuiQNfL9MHpSk5dTX/view?usp=sharing) to the paper written by me and two other creators. The report contains other creators work (Wheelchair control & SLAM) along with the semantic segmentation that we are discussing here.

## Recommendations

The Segmentation map obtained for the indoor and outdoor images could be helpful for the autonomous wheelchair to identify its maneuverable region, size, and shape of the obstacles in its environment. The future work could be running the segmentation model in real-time on the autonomous wheelchair to do the semantic segmentation for each frame recorded by the on-board wheelchair camera.

---

## References

[1] Semantic Understanding of Scenes through ADE20K Dataset. B. Zhou, H. Zhao, X. Puig, T. Xiao, S. Fidler, A. Barriuso and A. Torralba. International Journal on Computer Vision (IJCV), 2018. (https://arxiv.org/pdf/1608.05442.pdf)

[2] Scene Parsing through ADE20K Dataset. B. Zhou, H. Zhao, X. Puig, S. Fidler, A. Barriuso and A. Torralba. Computer
Vision and Pattern Recognition (CVPR), 2017. (http://people.csail.mit.edu/bzhou/publication/scene-parse-camera-ready.pdf)

## License

MIT License

Copyright (c) [2021] [Venkat Narayanan Balachandran]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

---

## Author Info

- LinkedIn - [Venkat_Narayanan_Balachandran](https://www.linkedin.com/in/venkat-balachandran)
