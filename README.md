# Fine-grained Appearance Transfer with Diffusion Models

The *official* repository for Fine-grained Appearance Transfer with Diffusion Models.

## News
- 2023.11  Code will be released coming soon.

## Fine-grained Appearance Transfer

![framework](figs/teaser_1.gif) 

![framework](figs/teaser_2.gif)

The results of fine-grained appearance transfer using our method. The leftmost column displays the source images. On the right, the output images achieved by detailed appearance transfer corresponding to the target images (outlined in black), while preserving structural integrity. The examples at the bottom demonstrate our method's capability to transfer across various domains and categories.

## Pipeline

![framework](figs/pipeline.png)

This figure illustrates our pipeline, commencing with null-text inversion applied to the source image <em>I</em>, creating a latent path for reconstructing the image. During the diffusion denoising stage, Latent Deviation is performed, leading to a modified image that aligns with the target image <em>T</em>. Specifically, the process begins with semantic alignment in the <em>x<sub>0</sub></em> space between <em>x<sub>0</sub><sup>src</sup></em> and <em>x<sub>0</sub><sup>tar</sup></em>, where <em>x<sub>0</sub><sup>tar</sup></em> is obtained through DDIM inversion with <em>T</em>. Based on semantic relations, features from <em>x<sub>0</sub><sup>tar</sup></em> are transferred to <em>x<sub>0</sub><sup>src</sup></em>, guided by an attention mask of <em>I</em>, resulting in <em>x'<sub>0</sub></em>. Finally, <em>x'<sub>0</sub></em> is processed in the latent space to synthesize the final modified image.
