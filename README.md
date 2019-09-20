### Resources
- Implementations of **SRDRM** and **SRDRM-GAN** for underwater image super-resolution
- Implementation: TensorFlow >= 1.11.0, Keras >= 2.2, and Python 2.7
  

| Perceptual enhancement | Color and sharpness   | 
|:--------------------|:--------------------|
| ![det-1a](/data/fig1b.jpg) | ![det-1b](/data/col.jpg) | 


### FUnIE-GAN Pointers
- Paper: soon
- USR-248 dataset: http://irvlab.cs.umn.edu/resources/usr-248-dataset
- Bibliography entry for citation:
	```
	article{islam2019fast,
	    title={Fast Underwater Image Enhancement for Improved Visual Perception},
	    author={Islam, Md Jahidul and Xia, Youya and Sattar, Junaed},
	    journal={arXiv preprint arXiv:1903.09766},
	    year={2019}
	}
	```
#### Usage
- Download the data, setup data-paths in the training-scripts
- Use paired training for FUnIE-GAN/UGAN, and unpaired training for FUnIE-GAN-up/Cycle-GAN 
	- Checkpoints: checkpoints/model-name/dataset-name
	- Samples: data/samples/model-name/dataset-name
- Use the test-scripts for evaluating different models
	- A few test images: data/test/A (ground-truth: GTr_A), data/test/random (unpaired)
	- Output: data/output 
- Use the [measure.py](measure.py) for quantitative analysis based on UIQM, SSIM, and PSNR 
- A few saved models are provided in saved_models/

#### Constraints and Challenges
- Trade-offs between performance and running time. Requirements:
	- Running time >= 5 FPS on Jetson-TX2 
	- Model size <= 12MB (no quantization) 
- Challenges
	- Performance for 8x models
	- Inconsistent coloring, infrequent noisy patches

### Acknowledgements
- https://github.com/wandb/superres
- https://github.com/david-gpu/srez
- https://github.com/Mulns/SuperSR
- https://github.com/tensorlayer/srgan
- https://github.com/icpm/super-resolution
- https://github.com/alexjc/neural-enhance
- https://github.com/jiny2001/dcscn-super-resolution
- https://github.com/titu1994/Image-Super-Resolution
- https://github.com/PacktPublishing/Advanced-Deep-Learning-with-Keras




