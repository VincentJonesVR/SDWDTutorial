# Installing Stable Diffusion GUI (as well as the anime focused Waifu-Diffusion model)
This tutorial covers two topics: 
1.	Where to find, download, and install Stable Diffusion (specifically cmdr2’s Stable Diffusion UI).

2.	Where to find, and download the Waifu-Diffusion model, as well as how to use that in place of the standard Stable Diffusion model.

<b>It is worth noting that this does require an Nvidia GPU. Technically it can be run on your CPU instead, but it will be *very* slow.</b>

<b><i>Stable Diffusion UI by cmdr2: https://github.com/cmdr2/stable-diffusion-ui

Waifu-Diffusion Model by hakurei: https://huggingface.co/hakurei/waifu-diffusion</i></b>

## Installing cmdr2’s Stable Diffusion UI
This is a straightforward process. 

1.	Head to the github link for Stable Diffusion UI and choose your download. Extract that zip to the root of one of your drives. 

        Example: C:\stable-diffusion-ui 

<b>Do not extract it deeper into your drive to avoid possible issues.</b>

2.	Run “Start Stable Diffusion UI.cmd”.

After you do this, a command prompt window will open and begin to download and install dependencies. This may take some time, depending on your internet connection and computer. It may appear to have stopped, but just leave it to do its thing. 

Eventually, your web browser will open to “localhost:9000”. That page will be your control panel for Stable Diffusion. 

3.	If you do not intend to use Stable Diffusion for anime style art, this is where the tutorial ends for you. Otherwise continue on.



## Installing hakurei’s Waifu-Diffusion
Stable Diffusion’s model tends to handle anime style art rather poorly. Waifu-Diffusion was trained off 56k images from the Japanese image board <i>Danbooru</i> to remedy this. 

When adding the Waifu-Diffusion model with this UI, you have two options.

1.	If you plan on using Stable Diffusion to generate non-anime images as well as use Waifu-Diffusion for anime images, you will want a duplicate Stable Diffusion folder. 

       In this circumstance, I would recommend giving it a name like “waifu-diffusion-ui” to avoid confusion. 

2.	If you plan on using Waifu-Diffusion ONLY, without using the standard Stable Diffusion model, you may continue these steps in the “stable-diffusion-ui” folder you set up in the first section of this tutorial.

For the sake of this tutorial, I will be using the path “C:/stable-diffusion-ui”

1.	Access the link above for Waifu-Diffusion and click the link marked “Original PyTorch Model Download Link”. 
This will download a file named “wd-v1-2-full-ema.ckpt” weighing in at a hefty 7.5gb. This is the Waifu-Diffusion model.

2.	<b>Ensure that Stable Diffusion is not currently running.</b> If it is, close both the webpage control panel and the command prompt instance.

3.	Navigate to the “stable-diffusion” folder inside of your Stable Diffusion UI folder.

        Example: C:\stable-diffusion-ui\stable-diffusion

4.	Inside of this folder you will find a file called “sd-v1-4.ckpt”. This is the standard Stable Diffusion model. You may either:

       Delete this file, <b>OR</b>

       Change the extension to something like <i>.ckptOLD</i>, if you’d like to keep it.

5.	Paste <i>wd-v1-2-full-ema.ckpt</i> into this folder, and rename it <i>sd-v1-4.ckpt</i> to match the file that was there before.

6.	Back out to <stable-diffusion-ui> and run “Start Stable Diffusion UI.cmd”.

Once the webpage has opened and the text at the top reads “Stable Diffusion is ready”, you are all set to start generating images. 

## Important To Note
Stable Diffusion UI has many built in features and options. I very highly recommend you read up on some of those options at the page linked. 

Some options should not be used while using Waifu-Diffusion. These include:

<b>1. Fix incorrect faces and eyes (uses GFPGAN)</b> 

   (This tries to correct the issues often seen with faces in AI generated images, but as it is based around real faces, it does not help when using Waifu-Diffusion)

<b>2. Upscale the image to 4x resolution using RealESRGAN_x4plus</b> 

   (Use the drop down to change that to <b>RealESRGAN_x4plus_anime_6b</b> instead.


