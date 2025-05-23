# Neural Style Transfer

This project implements **Neural Style Transfer (NST)** using PyTorch. NST is a technique that merges the **content** of one image with the **style** of another, resulting in a visually compelling hybrid. This repository uses a structured dataset with separate folders for content and style images.

## 📁 Directory Structure

├── data/
│ ├── content/ # Folder containing content images (e.g., landscapes, portraits)
│ └── style/ # Folder containing style images (e.g., artworks, patterns)
├── Neural_Style_Transfer_Divided.ipynb # Jupyter Notebook for style transfer
├── README.md


## 🎯 Objective

The goal is to create a new image that preserves the **high-level structure** (content) of a content image while adopting the **aesthetic characteristics** (style) of a style image. This is accomplished by optimizing a target image to minimize the content and style losses, computed via feature maps from a pretrained VGG-19 network.

## 📚 Approach

- **Feature Extraction**: Use a pretrained VGG-19 network to extract features at different layers.
- **Loss Functions**:
  - *Content Loss*: Measures how different the content of the target image is from the original content image.
  - *Style Loss*: Measures the difference in style by comparing the Gram matrices of feature activations.
- **Optimization**: The target image is initialized as a copy of the content image and iteratively updated to minimize total loss.

## 🛠️ Installation

Install required dependencies using pip:
pip install torch torchvision matplotlib pillow
Jupyter Notebook is also required. Install it if needed:
pip install notebook

## 🚀 Usage
Clone the repository:
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
Place your content and style images inside:
data/content/
data/style/
Open and run the notebook in Jupyter:
jupyter notebook Neural_Style_Transfer_Divided.ipynb
Select one content image and one style image in the notebook.

Configure hyperparameters such as:

Number of iterations

Style/content weights

Output image size

Run the cells to generate the stylized image.

## ⚙️ Parameters to Tune
num_steps: Number of optimization steps

content_weight: Weight for content loss

style_weight: Weight for style loss

image_size: Output resolution (limited by GPU memory)

## 🧩 Notes
Ensure that image files are valid formats such as .jpg, .png.

GPU acceleration is highly recommended for performance.

The notebook supports batching multiple combinations if modified.

## 📝 License
This project is licensed under the MIT License. You are free to use, modify, and distribute it with proper attribution.

## 🙏 Acknowledgments
Based on the pioneering work of Leon A. Gatys et al. (paper link).

Utilizes PyTorch's implementation of VGG-19 for feature extraction.
