# Classical Piano Composer

This project allows you to train a neural network to generate midi music files 

## Requirements

* Python 3.x
* Installing the following packages using pip:
	* Music21
	* Keras
	* Tensorflow-gpu
	* h5py

## Training

To train the network you run **lstm.py**.

To specify a source dir use --dir SOURCE 

To specify number of epochs use --epochs EPOCHS
E.g.

```
python lstm.py --dir cmajor --epochs 50
```
To import "old weights" change Line 125 in lstm.py and guide it to the weights file.

The network will use every midi file in ./midi_songs to train the network. 

**NOTE**: Weights are saved in output/SOURCE/weights-improvement-EPOCHS-LOSS-bigger.hdf files

## Generating music

Once you have trained the network you can generate text using **predict.py**

First set the specific weights File in Line 70 in predict.py

Then run the file
E.g.

```
python predict.py
```
**NOTE**: If the network structure has been changed, it must also be changed here.

the output will be saved as "output.mid"