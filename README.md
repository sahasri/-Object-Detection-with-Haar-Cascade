# Object-Detection-with-Haar-Cascade
This project uses OpenCV's Haar Cascade for face detection and performs hyperparameter tuning to improve detection accuracy. 
## Approach

The face detection model used here is a pre-trained Haar Cascade classifier, which operates by scanning the input image in a sliding window approach.

### 1. Hyperparameter Tuning
To improve detection accuracy, the project employs hyperparameter tuning on parameters such as `scaleFactor`, `minNeighbors`, and `minSize`.
  - `scaleFactor` : Image scaling factor.
  - `minNeighbors` : Minimum number of neighbors for a rectangle to retain it.
  - `minSize` : Minimum size of the bounding box for detection.
    
The evaluation of the model's performance is based on:

- **True Positives (TP)**: Correctly detected faces in images with faces.
- **False Positives (FP)**: Non-face images incorrectly classified as containing faces.
- **True Negatives (TN)**: Correctly identified non-face images.
- **False Negatives (FN)**: Faces missed in images containing faces.

The accuracy is calculated as:

   $$ \text{Accuracy} = \frac{TP + TN}{TP + TN + FP + FN} $$

The tuning function iterates through different combinations of parameters to find the best configuration for maximizing accuracy.

### 2. Dataset

This project uses two datasets:
- **Face Dataset**: This dataset consists only of faces of humans.
- **Non-Face Dataset**: This dataset consists of images of flowers, airplanes, motorcycles, nature, dogs, and cats, which are not considered faces of humans..

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/sahasri/Object-Detection-with-Haar-Cascade.git
   cd Object-Detection-with-Haar-Cascade
2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
3. Download dataset: The required datasets are included in the repository as zip files. 
- **faces-dataset.zip**: This zip file contains 200 images of faces of human.
- **non-faces_dataset.zip**: This zip file contains 200 images of non-faces, such as flowers, airplanes, motorcycles, nature, dogs, and cats.


 ## File Structure
```bash
Object-Detection-with-Haar-Cascade/                     
├── faces_dataset/                          
│   ├── 001.jpg
│   ├── 002.jpg
│   └── ...

├── non_faces_dataset/                      
│   ├── 001.jpg
│   ├── 002.jpg
│   └── ...

├── Object-Detection-with-Haar-Cascade.ipynb  
├── requirements.txt                                                     
└── README.md                   
