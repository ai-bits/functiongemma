# FunctionGemma
The Jupyter Lab notebook contains Python code for fully local Google FunctionGemma fine-tuning and performance checking, derived and fixed from [Google Colab example](https://github.com/google-gemini/gemma-cookbook/tree/main/FunctionGemma) and run on a PC with Linux or via WSL on Windows, an Nvidia RTX Pro 4500 Blackwell GPU (comparable to an RTX 5080, but 32GB v 16GB VRAM), taking 25 mins for 544 steps.  

Also sports code for converting / quantizing the last checkpoint from BF16 to the int8 liteRTLM format, suitable for edge computing and mobile devices like Android smart phones. (see Google AI Edge Gallery app from the Play Store)

Both model variants are available at [my Hugging Face repo](https://huggingface.co/gue22/functiongemma-270m-it-mobile-actions).

A lesser GPU might not be that worse, but my old NUC with an external 16GB RTX 5060 TI via Thunderbolt 3 was comparatively pathologically slower and showed rather 25h than 25". One factor (2) might be data-parallel execution on the GPU, its lower VRAM bandwidth, but there must be some major back and forth CPU <> GPU that the PCIe 5 machine was so much faster.
