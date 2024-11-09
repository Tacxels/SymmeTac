# SymmeTac
> This repo contains the details of SymmeTac, which is a high-efficiency photometric stereo method for camera-based tactile sensor.

[Symmetric Color LED Driven Effcient Photometric Stereo Reconstruction Methods for Camera-based Tactile Sensors](arxiv.org/abs/xxxx.xxxx)

## 1. Brife Review
To imporve the geometry (surface normal map) reconstruction efficiency of camera-based tactile sensor, we proosed SymmeTac. SymmeTac fully leverage the symmetric prior of light source and the spectral charictristics of CMOS to achieve highly efficient surface normal reconstruction. Specificly, the symmetric prior of light soruce can simplify the imaging process, and lead to a very simple equation for surface normal calculation; The red and blue channel of chormatic camera has little overtalk, which help us obtain two observations with one capture. <br><br>
<img src="./imgs/SymmeTacTeaser.jpg" width=400px />

## 2. Experiment Results
To evaluate the effectiveness of our method, we conduct simulation experiment on rendering images, and real-world experiments on robot.

### 2.1 Simulation 
To evaluate the performance on complex surface tactle details, we select 5 relief as test object. We use blender and Cycles engine to render images with diverse surface situation: lambertian, spatial-variable and channel-wise albedo (Lamb + **Alsp.**), shadow (Lamb + **Alsp.** + **Shad.**), and speculare reflection (Lamb + **Alsp.** + **Spec.**). <br>
<img src="./imgs/SimDataset.jpg" width=400px />

We choose typical photometric stereo algorithms: LSPS and RGB-PS, and compare their reconstruction results with our method.<br>
<img src="./imgs/CompAlgos8.jpg" width=400px />

The robustness under shadow and specular of our method are also evaluated.<br>
<img src="./imgs/CompRobust9.jpg" width=400px />



### 2.2 Real-world Experiments
