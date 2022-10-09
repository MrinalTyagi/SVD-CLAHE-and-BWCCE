# SVD CLAHE Boosting and Balanced Loss Function for COVID-19 Detection from an Imbalanced CXR Dataset

by
Santanu Roy,
Mrinal Tyagi,
Vibhuti Bansal,
Vikas Jain

This paper has been published under Computers in Biology and Medicine(Elsevier Q1). [Manuscript Link](https://www.sciencedirect.com/science/article/pii/S0010482522008009?via%3Dihub)

> In this paper we proposed an augmented dataset by employing the data augmentation technique "SVD-CLAHE Boosting". This dataset is more balanced dataset than any existing CXR dataset.
> In this paper we have also proposed a Balanced WCCE loss function, incorporated in CNN models, in order to alleviate class imbalance problem. We have assigned bias weights of BWCCE based on probabilistic intuition.

### Methodology
![Methodology](https://user-images.githubusercontent.com/21031150/194777662-559a3581-dd8e-40fd-b26c-36dea8f13e30.jpg)

<table border="0">
 <tr>
    <td align="center" padding="0"><h3>ResNet50 Results</h3></td>
    <td align="center" padding="0"><h3>VGG19 Results</h3></td>
 </tr>
 <tr>
    <td><img src="https://user-images.githubusercontent.com/21031150/194777717-84afda3e-f5a6-484f-bbdf-b022831f3ae0.jpg"></td>
    <td><img src="https://user-images.githubusercontent.com/21031150/194777719-be1eac58-d374-4698-b026-0db2e7505574.jpg"></td>
 </tr>
</table>

## Abstract

> Covid-19 disease has had a disastrous effect on the health of the global population, for the last two years. Automatic early detection of Covid-19 disease from Chest X-Ray (CXR) images is a very crucial step for human survival against Covid-19. In this paper, we propose a novel data-augmentation technique, called SVD-CLAHE Boosting and a novel loss function Balanced Weighted Categorical Cross Entropy (BWCCE), in order to detect Covid 19 disease efficiently from a highly class-imbalanced Chest X-Ray image dataset. Our proposed SVD-CLAHE Boosting method is comprised of both oversampling and under-sampling methods. First, a novel Singular Value Decomposition (SVD) based contrast enhancement and Contrast Limited Adaptive Histogram Equalization (CLAHE) methods are employed for oversampling the data in minor classes. Simultaneously, a Random Under Sampling (RUS) method is incorporated in major classes, so that the number of images per class will be more balanced. Thereafter, Balanced Weighted Categorical Cross Entropy (BWCCE) loss function is proposed in order to further reduce small class imbalance after SVD-CLAHE Boosting. Experimental results reveal that ResNet-50 model on the augmented dataset (by SVD-CLAHE Boosting), along with BWCCE loss function, achieved 95% F1 score, 94% accuracy, 95% recall, 96% precision and 96% AUC, which is far better than the results by other conventional Convolutional Neural Network (CNN) models like InceptionV3, DenseNet-121, Xception etc. as well as other existing models like Covid-Lite and Covid-Net. Hence, our proposed framework outperforms other existing methods for Covid-19 detection. Furthermore, the same experiment is conducted on VGG-19 model in order to check the validity of our proposed framework. Both ResNet-50 and VGG-19 model are pre-trained on the ImageNet dataset. We publicly shared our proposed augmented dataset on Kaggle website (https://www.kaggle.com/tr1gg3rtrash/balanced-augmented-covid-cxr-dataset), so that any research community can widely utilize this dataset. Our code is available on GitHub website online (https://github.com/MrinalTyagi/SVD-CLAHE-and-BWCCE).

## Software implementation

All source code used to generate the results in the paper are available in the directory.
The calculations and figure generation are all run on
[Colab Service](https://colab.research.google.com/notebooks/intro.ipynb).


## Getting the code

You can download a copy of all the files in this repository by cloning the
[git](https://github.com/MrinalTyagi/SVD-CLAHE-and-BWCCE.git) repository:

    git clone https://github.com/MrinalTyagi/SVD-CLAHE-and-BWCCE.git

or [download a zip archive](https://github.com/MrinalTyagi/SVD-CLAHE-and-BWCCE/archive/refs/heads/main.zip).


## Dependencies

You'll need a working Python environment to run the code.
The recommended way to set up your environment is through the
[Anaconda Python distribution](https://www.anaconda.com/download/) which
provides the `conda` package manager.
Anaconda can be installed in your user directory and does not interfere with
the system Python installation.
The required dependencies are specified in the file `environment.yml`.

We use `conda` virtual environments to manage the project dependencies in
isolation.
Thus, you can install our dependencies without causing conflicts with your
setup (even with different Python versions).

Run the following command in the repository folder (where `environment.yml`
is located) to create a separate environment and install all required
dependencies in it:

    conda env create


## Reproducing the results

Before running any code you must activate the conda environment:

    source activate ENVIRONMENT_NAME

or, if you're on Windows:

    activate ENVIRONMENT_NAME

This will enable the environment for your current terminal session.
Any subsequent commands will use software that is installed in the environment.

For reproducing the results, execute the Jupyter notebooks individually.

To do this, you must first start the notebook server by going into the
repository top level and running:

    jupyter notebook

This will start the server and open your default web browser to the Jupyter
interface. In the page, go into the respective folder and select the
notebook that you wish to view/run.

The notebook is divided into cells (some have text while other have code).
Each cell can be executed using `Shift + Enter`.
Executing text cells does nothing and executing code cells runs the code
and produces it's output.
To execute the whole notebook, run all cells in order.


## License

All source code is made available under a BSD 3-clause license. You can freely
use and modify the code, without warranty, so long as you provide attribution
to the authors.
