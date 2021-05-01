# DF-GAN: Deep Fusion Generative Adversarial Networks for Text-to-Image Synthesis

### Datasets Preparation
1. Download the preprocessed metadata for [birds](https://drive.google.com/open?id=1O_LtUP9sch09QH3s_EBAgLEctBQ5JBSJ) [coco](https://drive.google.com/open?id=1rSnbIGNDGZeHlsUlLdahj0RJ9oo6lgH9) and save them to `data/`
2. Download the [birds](http://www.vision.caltech.edu/visipedia/CUB-200-2011.html) image data. Extract them to `data/birds/`
3. Download [coco](http://cocodataset.org/#download) dataset and extract the images to `data/coco/`
---
### Training

**Train DF-GAN models:**
  - For bird dataset: `python main.py --cfg cfg/bird.yml`
  - For coco dataset: `python main.py --cfg cfg/coco.yml`

- `*.yml` files are example configuration files for training/evaluation our models.


**Evaluate DF-GAN models:**

- To evaluate our DF-GAN on CUB, change B_VALIDATION to True in the bird.yml. and then run `python main.py --cfg cfg/bird.yml`
- To evaluate our DF-GAN on coco, change B_VALIDATION to True in the coco.yml. and then run `python main.py --cfg cfg/coco.yml`
- We compute inception score for models trained on birds using [StackGAN-inception-model](https://github.com/hanzhanggit/StackGAN-inception-model).
- We compute FID for CUB and coco using [DM-GAN/eval/FID](https://github.com/MinfengZhu/DM-GAN/tree/master/eval/FID). 

**Generation:**
- Check gensamples.txt
