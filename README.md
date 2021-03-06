# Neural Networks for EEG Decoding
Decode imagined movement classes from EEG data using various neural network architectures. Based off Final Project for C147 at UCLA. Further discussion in `NN_EEG_Paper.pdf`

Uses labeled EEG data from http://www.bbci.de/competition/iv/. Data is 4s of 22 channel EEG recordings from 9 total subjects who are imagining 1 of 4 movements

Compared convolutional neural network (CNN), recurrent neural network (RNN), and hybrid convolutional recurrent networks (CRNNs).

Achieved best performance with a CNN adapted to EEG data (EEG_CNN in `eeg_models.py`). This CNN was designed with temporal filters to allow it to learn the key information contained in the EEG frequency power spectrum and spatial filters to combine data from multiple electrodes.  This network can decode the chosen movement with approximately 70% accuracy using only 1.2 seconds of data, suggesting possibility for brain-computer interface applications with improvements. 

## Usage
***Run in Cloud:***

The notebook is designed to be run with a GPU on Google Colab which can be done simply at https://colab.research.google.com/github/kkapre/Neural-Networks-EEG-Decoding/blob/main/NN_EEG_Decoding.ipynb. Running the cells will request Google Drive access and will create a new folder in the drive where this repository will be cloned. 

***Run Locally:***

Git-LFS must be downloaded and installed before cloning. 

For installation instructions see https://docs.github.com/en/free-pro-team@latest/github/managing-large-files/installing-git-large-file-storage

On Linux you can also do

```
sudo apt-get install git-lfs
git lfs install
```

Clone the repository with 
```
git clone https://github.com/kkapre/Neural-Networks-EEG-Decoding.git
```

Then run `NN_EEG_Decoding.ipynb`, changing any code involving Google Drive. 

## References
[1] R. T. Schirrmeister, J. T. Springenberg, L. D. J. Fiederer,
M. Glasstetter, K. Eggensperger, M. Tangermann, F. Hutter,
W. Burgard, and T. Ball. Deep learning with convolutional
neural networks for EEG decoding and visualization. Human
Brain Mapping, 38(11):5391–5420, Aug. 2017.
