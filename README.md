# Image_denoising_using_UNET
This repo includes the image denoising technique using Unet architecture. 
So here I trained the model on 2 types of noises, one is poisson and other one is speckle noise (gamma distribution). 
The data is generated by me. 

After training the model I found a slight increase in PSNR and SSIM values, when compared clean images with noisy and predicted image.
In the code you can also see the MSE for the clean and predicted images.

I was not targetting any random gamma noise, first I fitted a gamma distribution to my "noise only" frames, later when I got the parameters of
gamma distribution, then I added that noise to images. 
The training time for the above code was around 15 hours on GeForce RTX 3090, if you are using Geforce RTX 2080 then it will take around 27-28 hours. 


If you want to train this model on your noise, then what you can do is pick any standard dataset and add the noise to those standard images. 
later you can send both noisy and clean images to the architecture.

Note: If you are dealing with medical images, and you pick a standard data set as celeb, then unet will try to learn the features of faces instead of medical image features. Hence try to generate data using combination of different datasets, later you can always finetune using actual data.

If anyone want code for adding noise or have any doubt regarding the architecture, then can contact me on the below mail addresses:

shivhareanshul78@gmail.com
anshulshivha@iisc.ac.in
