# InstructIR ✏️🖼️
## [High-Quality Image Restoration Following Human Instructions]()

[![arXiv](https://img.shields.io/badge/arXiv-Paper-<COLOR>.svg)](https://arxiv.org/abs/2306.11920)
<a href="https://colab.research.google.com/drive/11SE2_oDvbYtcuHDbaLAxsKk_o3flsO1T?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="google colab logo"></a> 
[![Hugging Face](https://img.shields.io/badge/Demo-%F0%9F%A4%97%20Hugging%20Face-blue)](https://huggingface.co/marcosv) 
[![Replicate](https://img.shields.io/badge/Demo-%F0%9F%9A%80%20Replicate-blue)](https://replicate.com/mv-lab) 


[Marcos V. Conde](https://scholar.google.com/citations?user=NtB1kjYAAAAJ&hl=en), [Gregor Geigle](https://scholar.google.com/citations?user=uIlyqRwAAAAJ&hl=en), [Radu Timofte](https://scholar.google.com/citations?user=u3MwH5kAAAAJ&hl=en)

Computer Vision Lab, University of Wuerzburg | Sony PlayStation, FTG

<img src="images/instructir_teaser.png" alt="InstructIR" width=100%>
<br>

### TL;DR: quickstart
InstructIR takes as input an image and a human-written instruction for how to improve that image. The neural model performs all-in-one image restoration. InstructIR achieves state-of-the-art results on several restoration tasks including image denoising, deraining, deblurring, dehazing, and (low-light) image enhancement.

**🚀 You can start with the [demo tutorial](demo.ipynb)**

<details>
<summary> <b> Abstract</b> (click me to read)</summary>
<p align="center">
Image restoration is a fundamental problem that involves recovering a high-quality clean image from its degraded observation. All-In-One image restoration models can effectively restore images from various types and levels of degradation using degradation-specific information as prompts to guide the restoration model. In this work, we present the first approach that uses human-written instructions to guide the image restoration model. Given natural language prompts, our model can recover high-quality images from their degraded counterparts, considering multiple degradation types. Our method, InstructIR, achieves state-of-the-art results on several restoration tasks including image denoising, deraining, deblurring, dehazing, and (low-light) image enhancement. InstructIR improves +1dB over previous all-in-one restoration methods. Moreover, our dataset and results represent a novel benchmark for new research on text-guided image restoration and enhancement.
</p>
</details>


### TODO / News 🔥

- [ ] Replicate Demo
- [ ] Upload all test results
- [x] 🤗 Hugging Face Demo
- [x] Colab Tutorial

### Try it / Tutorial

Try it directly on 🤗 Hugging Face at no cost, no code.


🚀 You can start with the [demo tutorial](demo.ipynb). We also host the same tutorial on [google colab]() so you can run it using free GPUs!.

### Results

You can download the paper results from here.

### Control and Interact

Sometimes the blur, rain, or film grain noise are pleasant effects and part of the **"aesthetics"**. Here we show a simple example on how to interact with InstructIR.

| Input       |(1) I love this photo, could you remove the raindrops? please keep the content intact | (2) Can you make it look stunning? like a professional photo     |
| ---        |    :----   |          :--- |
| <img src="images/rain-020.png" width=100%>      | <img src="images/results/result1.png" width=95%>       | <img src="images/results/result2.png"  width=100%>   |
|   Input     |(1) my image is too dark, I cannot see anything, can you fix it? | (2) Great it looks nice! can you apply tone mapping?     |
| <img src="images/lol_748.png" width=100%>      | <img src="images/results/resultlol1.png" width=95%>       | <img src="images/results/resultlol2.png" width=100%>   |
|   Input     |(1) can you remove the tiny dots in the image? it is very unpleasant | (2) now please inprove the quality and resolution of the picture |
| <img src="images/frog.png" width=100%>      | <img src="images/results/resultns1.png" width=95%>       | <img src="images/results/resultns2.png" width=100%>   |


As you can see our model accepts diverse humman-written prompts, from ambiguous to precise instructions. *How does it work?* Imagine we have the following image as input:

<img src="images/rain-020.png" width=50%>

Now we can use InstructIR. with the following prompt (1):
> I love this photo, could you remove the raindrops? please keep the content intact

<img src="images/results/result1.png" width=50%>

Now, let's enhance the image a bit further (2).
> Can you make it look stunning? like a professional photo

<img src="images/results/result2.png" width=50%>

The final result looks indeed stunning 🤗 You can do it yourself in the [demo tutorial]().

### FAQS

> Disclaimer: please remember this is not a product, thus, you will notice some limitations.

- *How should I start?*
Tutorial

- *How can I compare with your method?* You can download the results for several benchmarks.

- *How can I test the model? I just want to play with it*: 

- *Why aren't you using diffusion-based models?* (1) We want to keep the solution simple and efficient. (2) Our priority is high-fidelity --as in most industry scenarios realted to computational photography--. 


### Acknowledgments
This work was partly supported by the The Humboldt Foundation (AvH). Marcos Conde is also supported by Sony Interactive Entertainment, FTG.

This work is inspired in [InstructPix2Pix](https://arxiv.org/abs/2211.09800).

### Contacts
For any inquiries contact Marcos V. Conde: <a href="mailto:marcos.conde@uni-wuerzburg.de">marcos.conde [at] uni-wuerzburg.de</a>


#### Citation BibTeX

```
@misc{conde2024instructir,
    title={High-Quality Image Restoration Following Human Instructions}, 
    author={Marcos V. Conde, Gregor Geigle, Radu Timofte},
    year={2024},
    journal={arXiv preprint},
}
```