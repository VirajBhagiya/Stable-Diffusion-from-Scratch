# Stable-Diffusion-from-Scratch 🚀 

Welcome to the **Stable Diffusion from Scratch** repository! This project is a step-by-step implementation of Stable Diffusion using **PyTorch**. This repo aims to help understand and build a foundational diffusion model from the ground up. 🧠💻

## 📖 Overview

Stable Diffusion is a cutting-edge **image generation model** that produces high-quality visuals from textual descriptions. This repository demystifies the inner workings of Stable Diffusion by providing a clear and modular implementation.

## 🛠 Features

- 🖼️ **Image Generation**: Generate images from text prompts.  
- ⚙️ **Customizable Parameters**: Easily adjust parameters like steps, strength and guidance scale.  
- ➕ **Positive & Negative Prompts**: Fine-tune results by specifying desired and undesired features.  
- 📂 **Image Paths**: Option to specify paths for input images for conditional generation.  

## 🚀 Getting Started

### 🔧 Prerequisites:
Ensure you have the following installed:  
- Python 3.8+ 🐍  
- GPU with CUDA support (optional) 🖥️

### 📂 Required Files and Data:
Before running the notebook, ensure you download the necessary files:

1. Tokenizer Files:
    - Download `vocab.json` and `merges.txt` from [Hugging Face: Stable Diffusion v1-5 Tokenizer](https://huggingface.co/stable-diffusion-v1-5/stable-diffusion-v1-5/tree/main/tokenizer).
    - Save them in the `data` folder:
    ``` bash
    /data/vocab.json  
    /data/merges.txt
    ```

2. Model Weights:
    - Download `v1-5-pruned-emaonly.ckpt` from [Hugging Face: Stable Diffusion v1-5](https://huggingface.co/stable-diffusion-v1-5/stable-diffusion-v1-5/tree/main).
    - Save it in the `data` folder:
    ``` bash
    /data/v1-5-pruned-emaonly.ckpt
    ```

### 📂 Installation

1. Clone this repository:  
   ``` bash
   git clone https://github.com/VirajBhagiya/Stable-Diffusion-from-Scratch.git
   cd Stable-Diffusion-from-Scratch
   ```

2. Install dependencies:  
   ``` bash
   pip install -r requirements.txt
   ```

3. Open and run the generator notebook:  
   ``` bash
   jupyter notebook generator.ipynb
   ```

## 🚀 How to Use

1. Setup Parameters:
    - Modify the prompt for desired outputs.
    - Adjust parameters like `cfg_scale`, `strength`, `num_inference_steps`, and `sampler`.

2. Run the Notebook:
    - Execute all cells, and the generated image will be displayed as output.

### 🔧 Adjustable Parameters

| **Parameter**          | **Description**                                                                                  |
|------------------------|--------------------------------------------------------------------------------------------------|
| `prompt`              | Main textual input to describe the desired output image.                                         |
| `uncond_prompt`       | Negative prompt to exclude undesired features.                                                   |
| `cfg_scale`           | Classifier-free guidance scale; higher values prioritize matching the prompt. Default: 8.        |                                                        |
| `num_inference_steps` | Number of steps for the diffusion process. Higher values produce finer results. Default: 50.      |
| `strength`            | Determines how strongly the input image influences the output (for Image-to-Image). Default: 0.9 |
| `seed`                | Controls randomness for reproducible results. Default: 42.                                       |


## 🤝 Contributing
 
1. Fork the repository 🍴  
2. Create a feature branch: `git checkout -b feature-name`  
3. Commit your changes: `git commit -m 'Add feature'`  
4. Push to the branch: `git push origin feature-name`  
5. Open a pull request 🛠️

## 🌐 References

- 📄 Original Paper: ["High-Resolution Image Synthesis with Latent Diffusion Models"](https://arxiv.org/abs/2112.10752)  
- 🛠️ PyTorch Documentation: [pytorch.org](https://pytorch.org/)
- 🤗 Transformers Library: [Hugging Face](https://huggingface.co/)
- 🔗 [hkproj/pytorch-stable-diffusion](https://github.com/hkproj/pytorch-stable-diffusion): Repository used for inspiration and adaptation.

## 📑 Feedback

If you have any questions or feedback, feel free to reach out by opening an issue or submitting a pull request!