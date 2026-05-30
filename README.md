# Qwen3-TTS-Darija-1hour

A Darija Moroccan Arabic text-to-speech project based on **Qwen3-TTS-12Hz-1.7B-Base**, fine-tuned with **LoRA** on atlasia/DODa-audio-dataset M2.


## Overview
This project fine-tunes Qwen3-TTS on a Darija dataset and provides inference through a simple Gradio interface.

## Base Model
- [`Qwen/Qwen3-TTS-12Hz-1.7B-Base`](https://huggingface.co/Qwen/Qwen3-TTS-12Hz-1.7B-Base)
  
## Hugging Face 
- ['loubna1101/Qwen3-TTS-1hour'](https://huggingface.co/loubna1101/Qwen3-TTS-1hour)
## Fine-tuning Method
- LoRA fine-tuning
- Single-speaker custom voice
- 24kHz audio
- Speaker name used during training: `male-2`

## Dataset Preparation
The training pipeline:
1. Resamples audio to 24kHz
2. Extracts codec tokens 
3. Fine-tunes Qwen3-TTS with LoRA

## Training Setup
- Batch size: `1`
- Learning rate: `5e-5`
- Epochs: `10`

## Repository Contents
- `inference.ipynb`: inference workflow
- `app.py`: Gradio demo
- `requirements.txt`: dependencies

## Model Files
The trained LoRA adapter and custom speaker embedding are hosted on Hugging Face.

## Inference
The model is loaded as:
- base model from Qwen
- LoRA adapter from this project
- custom speaker embedding from this project

## Authors
- loubna haouach
- chaimae haddouche

## Disclaimer
This project is for research and educational purposes. Please ensure you have the right to use and publish the voice data used for fine-tuning.

## Credits
- Qwen team for Qwen3-TTS
- atlasIA for the Doda dataset
- Hugging Face ecosystem
