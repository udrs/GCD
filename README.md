# Env 
pip install torch==2.1.2 torchvision==0.16.2 torchaudio==2.1.2 --index-url https://download.pytorch.org/whl/cu118

pip install -r requirement.txt

# Training 
python scripts/segmentation_train.py --data_dir xxx --out_dir xxx --image_size 256 --num_channels 128 --class_cond False --num_res_blocks 2 --num_heads 1 --learn_sigma True --use_scale_shift_norm False --attention_resolutions 16 --diffusion_steps 1000 --noise_schedule linear --rescale_learned_sigmas False --rescale_timesteps False --lr 1e-4 --batch_size 8

# Inference
python scripts/segmentation_sample.py  --data_dir xxx --out_dir xxx --model_path xxx --image_size 256 --num_channels 128 --class_cond False --num_res_blocks 2 --num_heads 1 --learn_sigma True --use_scale_shift_norm False --attention_resolutions 16 --diffusion_steps 1000 --noise_schedule linear --rescale_learned_sigmas False --rescale_timesteps False --num_ensemble 5

# Visualization:
![image](https://github.com/Udrs/DDPM-based-Change-Detection/blob/main/inference_vis_video/output_video2.gif)
![image](https://github.com/Udrs/DDPM-based-Change-Detection/blob/main/inference_vis_video/output_video4.gif)
---
![image](https://github.com/Udrs/DDPM-based-Change-Detection/blob/main/inference_vis_video/output_video5.gif)
![image](https://github.com/Udrs/DDPM-based-Change-Detection/blob/main/inference_vis_video/output_video6.gif)

See our other work within：https://github.com/sstary/SSRS


# notation

https://github.com/udrs/diffusion-framework-for-CD-/blob/fe64a6c1c0d58cfb45768de8a00ad2be151920fb/guided_diffusion/unet.py#L580
self.AB_Concator = Diff_Module(3, 2)  # add your novel diff module here into the diffusion model framework. you will obtain a good result. 


# Statement
The training file has been attached
I have not worked for the lab anymore. I dont have any time to maintain this project cause I worked in industy.
Thank you for your patience and understanding.
Tips: You can add your novel model following the "notation part" in the CD diffusion framework as your paper's innovation.
