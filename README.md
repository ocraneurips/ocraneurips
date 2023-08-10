### This repository contains code for the Object-centric Relational Abstraction (OCRA) model.

## Requirements
* python 3.9.7
* NVIDIA GPU with CUDA 11.0+ capability
* torch==1.11.0
* torchvision==0.12.0
* glob
* PIL==8.4.0
* numpy==1.20.3
* einops==0.4.1


### ART

The pretrained slot attention model for the ART dataset is given under `weights/slot_attention_autoencoder_6slots_clevrdecoder_morewarmup_lowerlr_nolrdecay_64dim_128res_random_spatial_heldout_unicodes_resizedcropped_continuetraining_run_1_best.pth.tar`

To train on Same/different task with $m=95$ run `python train_ocra_sd.py --batch_size 16  --img_size 128 --num_epochs 600 --m_holdout 95 --run '1'` 

To train on Relational match-to-sample task with $m=95$ run `python train_ocra_rmts.py --batch_size 16  --img_size 128 --num_epochs 400 --m_holdout 95 --run '1'` 

To train on Distribution-of-3 task with $m=95$ run `python train_ocra_dist3.py --batch_size 16  --img_size 128 --num_epochs 400 --m_holdout 95 --run '1'` 

To train on Identity rules task with $m=95$ run `python train_ocra_dist3.py --batch_size 16  --img_size 128 --num_epochs 100 --m_holdout 95 --run '1' --task 'identity_rules' --test_gen_method 'subsample'` 

### SVRT

The pretrained slot attention model for the SVRT dataset using 500 samples for each task is given under `weights/slot_attention_autoencoder_augmentations_6slots_clevrdecoder_morewarmup_lowerlr_nolrdecay_64dim_128res_grayscale_svrt_alltasks_num_images_250_run_1_more_x3_continuetraining_best.pth.tar`

The pretrained slot attention model for the SVRT dataset using 1000 samples for each task is given under `weights/slot_attention_autoencoder_augmentations_6slots_clevrdecoder_morewarmup_lowerlr_nolrdecay_64dim_128res_grayscale_svrt_alltasks_num_images_500_run_1_more_more_continuetraining_best.pth.tar`

Download the SVRT dataset using (https://fleuret.org/cgi-bin/gitweb/gitweb.cgi?p=pysvrt.git;a=summary)

### CLEVR-ART

<!--
**ocraneurips/ocraneurips** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
