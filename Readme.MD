# 🤖 Diffusion Model Meme Generator

A **Streamlit-based web application** that uses **Stable Diffusion** and **LoRA weights** to generate custom memes by combining a text-to-image prompt with user-provided overlay text.


### Main Application Interface
![Main application interface](assets/Screenshot_meme_app.png)

## 📋 Table of Contents

* [About The Project](#️-about-the-project)
* [Built With](#️-built-with)
* [Getting Started](#️-getting-started)

  * [Prerequisites](#prerequisites)
  * [Installation](#installation)
* [Usage](#️-usage)
* [Features](#-features)
* [License & Credits](#-license--credits)
* [Acknowledgements](#-acknowledgements)

---

## ℹ️ About The Project

This project is a **powerful yet easy-to-use meme generator** built with **Python** and **Streamlit**. It leverages **diffusion models** (specifically *Stable Diffusion v1.4*) enhanced with **LoRA (Low-Rank Adaptation)** weights to create high-quality, stylized images from text prompts.

The application then automatically overlays user-provided text onto the generated images, with proper styling and outlines for readability, turning any idea into a shareable meme.

---

## 🛠️ Built With

This project utilizes several key technologies:

* **Streamlit** – For the interactive web application interface.
* **Hugging Face diffusers** – For the text-to-image generation pipeline.
* **PyTorch** – Backend for model operations.
* **Pillow (PIL)** – For image manipulation and text overlay.
* **Stable Diffusion v1.4** – The base diffusion model.
* **rschroll/maya_model_v1_lora** – LoRA weights for stylistic fine-tuning.

---

## 🚀 Getting Started

Follow these steps to set up the project locally.

### Prerequisites

* Python 3.8 or newer
* pip (Python package installer)
* A **CUDA-enabled GPU** (recommended for faster performance; CPU mode supported but slower)
* The `arial.ttf` font file (standard on Windows/macOS; on Linux, install via `sudo apt-get install ttf-mscorefonts-installer` or update the font path in code)

### Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/Otto-Destiny/meme-generator-with-stable-diffusion-model.git
   cd your-project-directory
   ```

2. **Create and activate a virtual environment:**

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   ```

3. **Install dependencies:**

   ```bash
   pip install streamlit torch diffusers transformers Pillow safetensors
   ```

   > Note: `transformers` and `safetensors` are required for the diffusers pipeline.

---

## 🖥️ Usage

Run the Streamlit app from your terminal:

```bash
streamlit run app.py
```

Your default browser will open automatically (usually at [http://localhost:8501](http://localhost:8501)).

### App Controls

* **Number of Images:** Select how many meme variants to generate (1–10).
* **Text-to-Image Prompt:** Describe your background image (e.g., *"A confused golden retriever looking at a laptop"*).
* **Text to Display:** Enter your meme text (e.g., *"WHAT IS CODE?"*).

Click **Generate Images** and wait for the model to do its magic!

> The first run will take longer as models and weights are downloaded. Thanks to Streamlit’s `@st.cache_resource`, subsequent generations will be much faster.

Your generated memes will appear on the main page, ready to save and share.

---

## ✨ Features

* **Simple Streamlit UI** – Clean and responsive.
* **Advanced Image Generation** – Combines Stable Diffusion + LoRA for enhanced visuals.
* **Automatic Text Overlay** – Adds outlined text for readability.
* **Batch Generation** – Create up to 10 memes at once.
* **Smart Caching** – Model loads only once per session.
* **Hardware Agnostic** – Uses GPU if available; falls back to CPU.

---

## 📜 License & Credits

This project is presented as part of coursework for **WorldQuant University**.
It is covered by WorldQuant University’s academic and licensing policies. These may restrict sharing, redistribution, or commercial use. Please treat this repository as an **educational and portfolio example only**.

The project code and framework are licensed under the **Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License**.

To view a copy of this license, visit:
[http://creativecommons.org/licenses/by-nc-nd/4.0/](http://creativecommons.org/licenses/by-nc-nd/4.0/)

---

## 🙏 Acknowledgements

* **WorldQuant University** – For the educational program and project structure.
* **Hugging Face** – For the `diffusers` library and hosting of models.
* **Stable Diffusion creators** – For the foundational model.
* **rschroll** – For the `maya_model_v1_lora` LoRA weights.

---
