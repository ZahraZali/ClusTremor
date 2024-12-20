# ClusTremor
[![DOI](https://zenodo.org/badge/512606155.svg)](https://zenodo.org/badge/latestdoi/512606155)

ClusTremor is an algorithm specifically designed for unsupervised clustering of seismic data, with a focus on tremor signals. Leveraging the power of deep learning and clustering techniques, we employ a deep clustering approach to effectively cluster volcanic tremors.

![Eruptive phases](https://github.com/ZahraZali/ClusTremor/assets/50201021/3e18f907-7dae-41cf-8ee1-cc869eac33c4)

Our methodology utilizes an autoencoder, allowing the model to learn meaningful feature representations while assigning clusters to them. This joint learning process ensures the extraction of informative representations that capture the underlying patterns in tremor signals and effectively cluster them.

To showcase the practical application of the ClusTremor algorithm, we provide an example of its effectiveness in clustering volcanic tremors during the 2021 Geldingadalir eruption in Iceland. This demonstration serves to highlight the algorithm's capability in capturing meaningful clusters in real-world scenarios.

With ClusTremor, researchers and seismologists can leverage its unsupervised clustering capabilities to gain insights into the behavior and patterns of tremors, enabling a deeper understanding of seismic activity.

## Citation
When using this model, please cite the following:

Zali, Z., Mousavi, S.M., Ohrnberger, M. et al. Tremor clustering reveals pre-eruptive signals and evolution of the 2021 Geldingadalir eruption of the Fagradalsfjall Fires, Iceland. Commun Earth Environ 5, 1 (2024). https://doi.org/10.1038/s43247-023-01166-w

Zahra Zali. (2023). ZahraZali/ClusTremor: ClusTremor (v1.0.0). Zenodo. https://doi.org/10.5281/zenodo.8386966

## ClusTremor Algorithm - Code Instruction

The complete code for the ClusTremor algorithm can be found in the ClusTremor.ipynb notebook located in the src folder. This notebook includes the implementation of the algorithm, including autoencoder construction and evaluation, clustering, and fine-tuning.

Here's a breakdown of the ClusTremor algorithm code:

1- Loading and Splitting Data:  The code begins by loading the input data and splitting it into training and test sets. This step ensures that you have separate datasets for training and evaluating the model.

2- Autoencoder Construction and Evaluation: We construct an autoencoder, which is a neural network architecture used for unsupervised learning and dimensionality reduction. It then evaluates the autoencoder's reconstruction performance using a loss function. Additionally, the input and output of the autoencoder are visualized to assess the quality of the reconstruction.

3- Clustering Initialization: We initialize the clustering process using the k-means algorithm. It assigns initial cluster labels to the data points based on the features or representations learned by the autoencoder.

4- Determining the Optimal Number of Clusters: We use the Calinski-Harabasz score defined as ratio of the sum of between-cluster dispersion and of within-cluster dispersion, to determine the optimal number of clusters. This step helps in finding an appropriate value for the number of clusters in the clustering process.

5- Integration of Clustering Layer: We integrate a clustering layer into the bottleneck layer of the autoencoder. This allows the model to simultaneously perform dimensionality reduction and clustering, leveraging the learned representations to separate data points into distinct clusters.

6- Fine-tuning with Clustering Loss: We fine-tune the model parameters using a loss functions. This loss function encourages the model to optimize both the reconstruction accuracy and the quality of the clustering assignments.


## Contact

* Developer: Zahra Zali, zali@gfz-potsdam.de
