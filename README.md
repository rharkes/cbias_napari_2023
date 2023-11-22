# CBIAS Napari 2023
Learning napari. 11-nov-2023 at the Crick Institute in London.

## Why I would like to run Napari
One word: Deeplearning. It all lives in Python, so moving from FIJI to Napari will hopefully streamline things in our workflows. Almost all our users are on windows 10 native, so I hope to get things running on that and not go to WSL2. 

## What have I done? (installation)
* Install Python 3.11 to `C:\Program Files\Python\Python311`
* (optional) Create this repository on github
* (optional) Clone it to my local drive
* Create a python 3.11 venv in a new folder
  * Open cmd run `cd C:\Program Files\Python\Python311`
  * Run `python -m venv C:\GitRepos\cbias_napari_2023\venv`
* Activate the new venv
  * Open cmd and run `C:\GitRepos\cbias_napari_2023\venv\Scripts\activate.bat`
* Go to the projectfolder `cd C:\GitRepos\cbias_napari_2023\`
* (optional) CellPose on GPU:
  * Install PyTorch 2.1.1 and cuda 12.1: `pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121`
  * Test in a console if GPU is found: 
  ```
  import torch
  torch.cuda.device_count()
  ```
* (optional) StarDist on GPU
  * [I gave this up. They only support <2.11 of tensorflow.](https://www.tensorflow.org/install/pip#windows-native) But that's fine, stardist is also fast on CPU.
* Install napari: `pip install napari[all]`
* Install jupyter notebook: `pip install notebook`
* Start jupyter notebook: `jupyter notebook`
* Test the [example notebook](notebooks/First_Test.ipynb) and see that napari starts
* Install stardist and cellpose plugin via the Napari GUI
  (note: I did this before the workshop. At the workshop it turned out they recommend conda.)

## What I should have done (installation)
* Install miniconda
* Start Anaconda Prompt (miniconda3)
* Set mamba as solver: `conda config --set solver libmamba`
* Create new environment
* Install Napari

## Using napari

### Plugins we used:
* pystackreg
* convpaint
* aicsimageio
* napari-animation 
* nd-cropper
