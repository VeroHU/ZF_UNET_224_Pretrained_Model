# ZF_UNET_224 Pretrained Model
Modification of convolutional neural net "UNET" for image segmentation in Keras framework

## Requirements

Python 3.*, Keras 1.2, Theano 0.9

## Usage

```python
from zf_unet_224_model import ZF_UNET_224, dice_coef_loss, dice_coef
from keras.optimizers import Adam

model = ZF_UNET_224()
model.load_weights("zf_unet_224.h5")
optim = Adam()
model.compile(optimizer=optim, loss=dice_coef_loss, metrics=[dice_coef])

model.fit(...)
```

## Pretrained weights

Download: [Weights ~123 MB](https://mega.nz/#!eAY2WAJS!zsb9rq20gjaSWJECu6tGdTN9tG6ZzQk0KQvB8iG2sL4)

Weights were obtained with random image generator (generator code available here: train_infinite_generator.py). See example of images from generator below.

![Example of images from generator](https://github.com/ZFTurbo/ZF_UNET_224_Pretrained_Model/blob/master/ZF_UNET_Generator_Images_Example.png)

Dice coefficient for pretrained weights: ~0.999. See history of learning below:




