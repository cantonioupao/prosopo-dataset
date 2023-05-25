# Prosopo dataset
Prosopo (means ”face” in Greek) and consists of 1600 high-quality ”in-the-wild” real RGB face images , manually selected from the FFHQ dataset.Most of the images, include frontal view face images with challenging light conditions, face accessories like glasses where most of the face geometry can be obtained.  The dataset constists of all the corresponding ground truth depth maps, as well as the eg3d latent code and face meshes, which were obtained from EG3D. In order to obtain all this ground truth data, we had to use a GAN inversion technique such as PTI, to project each image to the generators latent space. The purpose of this dataset, is to hopefully assist other researches in the community and be used an evaluation tool for common baselines.

![prosopo](https://github.com/cantonioupao/prosopo-dataset/assets/47451846/092ce063-fffb-42ca-b67c-5996a5a93ee2)

The dataset has been used to extensively evaluate the performance of the 2 frameworks that were developed, as part of the task of 3D face reconstruction from a single image. The first framework leverages directly the depth maps from EG3D and is trained on predicting depth values for the corresponding input face image. The depth regression framework, along with the various model architectures implemented, can be found [here](https://github.com/cantonioupao/face-depth-3D-reconstruction). The second framework, obtains the [EG3D](https://github.com/NVlabs/eg3d) latent code from an input face image, using a trained code regressor. Then the intermediate latent code, is fed into a later stage of the EG3D generator, to generate the 3D face mesh, of the corresponding input face image. The code regressor, along with the various model architectures implemented, can be found [here](https://github.com/cantonioupao/eg3d-code-regressor)



Overall, this dataset, can be used for either evaluation or training of single-view face 3D reconstruction models. More details about the dataset or the download link, can be found [here](https://www.kaggle.com/datasets/cantonioupao/prosopo-a-face-dataset-for-3d-reconstruction). 



