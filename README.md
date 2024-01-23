# Lip Syncing with Face Restoration

## Overview

This repository contains a system to generate high quality lip-synced videos using the Wav2Lip and GFPGAN models. The process involves generating English audio using text-to-speech model and genarating input image using diffusion model then creating corresponding high quality lip-synced videos by processing the frames using GFPGAN model.

## Steps

1. **Text-to-Speech (TTS) Audio Generation:**

   - English TTS: Utilizes gTTS (Google Text-to-Speech) to convert English text to audio.

2. **Image Generation:**

   - Uses the Diffusion Model to generate images from text.
     
3. **Wav2Lip Lip Sync Video Generation:**

   - Processes the generated image and audio with Wav2Lip to create a lip-synced video.
     - Example command: `python3.7 inference.py --checkpoint_path checkpoints/wav2lip_gan.pth --face generated_image.png --audio English_audio.wav --outfile lip_sync_video.mp4`

4. **GFPGAN Face Restoraion:**

   - Processes the frames from the lip-synced video to to generate realistic and high-quality results.

5. **Dependencies:**

   - gTTS, transformers, sentencepiece for TTS.
   - Diffusion Models for image generation.
   - Wav2Lip for lip-sync video generation.
   - GFPGAN for face restoration and generate high quality images.

6. **Acknowledgments:**

   - Wav2Lip model by [Wav2Lip Repo](https://github.com/Rudrabha/Wav2Lip).
   - GFPGAN model by [GFPGAN Repo](https://github.com/TencentARC/GFPGAN).

7. **Conclusion:**

   - This repository provides an end-to-end solution for generating lip-synced videos with text-to-speech audio. Feel free to explore different inputs and experiment with the provided model.

## Note
The test samples are in data_samples directory and the results in results directory
