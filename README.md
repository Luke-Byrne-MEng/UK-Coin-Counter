# UK-Coin-Counter
During this project an attempt was made to perform object detection and classification using OpenCV and python. The goal was to detect UK coins within images, and then classify them based on their value. For the sample set images the program acheived an average detection accuracy of 95.75%. (median 100%), and an average classification accuracy of 69.68% (median 71.11%). These results reinforce the general consensus that classical techniques are best suited for object detection within highly controlled or static environments, however machine learning techniques are often requred to perform accuracte classifcation. Please see the [full report](https://github.com/Luke-Byrne-uni/UK-Coin-Counter/blob/main/Coin-Counter-Report.pdf) for details.

First, the program takes in images from the user. These images are pre-processed to make binarization easier. Binary masks are created via thresholding of different image channels. These binaries are used to perform watershed segmentation to identify objects. The objects identified are then kept or discarded based on their shape, reasoning that UK coins are almost perfectly circular and do not have holes in them. The program then tries to find 50 pences within the remaining coins via line detection. All other coins are classified based on colour, and their size relative to the 50 pences.

# Use
This project was developed in Google Collab, as a Jupyter Notebook. To view the notebook please visit [this link](https://colab.research.google.com/github/Luke-Byrne-uni/UK-Coin-Counter/blob/main/Coin-Counter-Notebook.ipynb#scrollTo=V1_U_kb8t7nz) or [this link](https://nbviewer.jupyter.org/github/Luke-Byrne-uni/UK-Coin-Counter/blob/main/Coin-Counter-Notebook.ipynb). The image set used for development and testing is availble in this repo as coins.zip

# Results

![image](https://user-images.githubusercontent.com/72700318/119027728-9888b700-b99e-11eb-9de6-9ea2d62b6cef.png)
![image](https://user-images.githubusercontent.com/72700318/119027902-c40ba180-b99e-11eb-95ce-5de8e5f0b980.png)

