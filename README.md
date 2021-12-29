# Inter-individual deep image reconstruction
Data and demo code for Ho, Horikawa, Majima, and Kamitani (2022) [Inter-individual deep image reconstruction](). The preprint is availabe at bioRxiv (Ho et al., 2022, [Inter-individual deep image reconstruction]()).

## Requirements
- Python 2 or 3 (Python 2 is required for image reconstruction)
- Numpy
- Scipy
- Pandas
- bdpy: https://github.com/KamitaniLab/bdpy
- FastL2LiR: https://github.com/KamitaniLab/PyFastL2LiR


## Usage

### Training for neural code converter
Run the `ncc_training.py` to train the neural code converters for a pair of source and target subjects.

### DNN feature decoding from converted brain activities
Run the  `ncc_predict_feat.py` to predict the DNN features from the converted brain activities with the trained neural code converters. Pre-trained DNN feature decoders of the target subjects are necessary to run this script. We used the same methodology in the previous study for DNN feature decoding ([Horikawa & Kamitani, 2017, Generic decoding of seen and imagined objects using hierarchical visual features, Nat Commun.](https://www.nature.com/articles/ncomms15037)). Python code for the DNN feature decoding is available at GitHub:KamitaniLab/dnn-feature-decoding.

### Image reconstruction from decoded CNN features
We used the same methodology in the previous study for image reconstruction ([Deep image reconstruction from human brain activity](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1006633)). Please follow its instruction to setup the environment.

Run the `image_reconstruction/recon_image_Deeprecon_VGG19_DGN_GD.py` to reconstruct the natural images shown in the original paper. Run the `image_reconstruction/recon_image_colorShape_VGG19_NoDGN_LBFGS.py` to reconstruct the artificial images shown in the original paper.

## Data
Raw fMRI data: 
Preprocessed fMRI data and decoded CNN features:

## References
- Horikawa and Kamitani (2017) Generic decoding of seen and imagined objects using hierarchical visual features. Nature Communications 8:15037. https://www.nature.com/articles/ncomms15037
- Shen, Horikawa, Majima, and Kamitani (2019) Deep image reconstruction from human brain activity. PLOS Computational Biology. https://doi.org/10.1371/journal.pcbi.1006633