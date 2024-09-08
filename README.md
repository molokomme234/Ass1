Project Overview
This project implements an edge detection pipeline using a series of image processing techniques, including noise reduction, gradient calculation, non-maximum suppression, and thresholding. Additionally, a comparison is made between the custom pipeline and Canny edge detection, and evaluation metrics such as MSE, SSIM, and ORB feature matching are calculated for each image in the dataset. The results, including processed images and evaluation metrics, are saved to specific directories for further analysis.

Requirements
Before running the code, ensure that the following dependencies are installed in your environment:

Python 3.x
Jupyter Notebook
OpenCV (cv2)
NumPy
Matplotlib
scikit-image (skimage)
scikit-learn (sklearn)
To install the required packages, you can use the following commands in your terminal or Anaconda prompt:

bash
Copy code
pip install opencv-python-headless numpy matplotlib scikit-image scikit-learn
How to Run the Code
Download the Dataset:

Ensure that your dataset of retinal images (11 images) is located in a directory on your machine. In this case, the dataset should be stored in the directory:
makefile
Copy code
C:\Users\molok\OneDrive\Desktop\cos791
Open the Jupyter Notebook:

Open your terminal or Anaconda prompt and navigate to the project directory where the notebook file is located.
Launch Jupyter Notebook by running:
bash
Copy code
jupyter notebook
Load the Notebook:

Once Jupyter Notebook is running, navigate to the notebook file containing the edge detection pipeline code.
Open the notebook in the browser interface.
Modify Paths if Necessary:

Ensure that the paths to your image directory, results directory, and metrics directory are correctly set in the notebook. You can modify them if needed. The current paths are:
python
Copy code
image_dir = r'C:\Users\molok\OneDrive\Desktop\cos791'
results_dir = r'C:\Users\molok\OneDrive\Desktop\cos791\results'
metrics_dir = r'C:\Users\molok\OneDrive\Desktop\cos791\metrics'
Adjust these paths as per your system configuration.
Run the Notebook Cells:

Execute each cell of the notebook in sequence. The cells perform the following actions:
Load images from the dataset.
Apply the custom edge detection pipeline.
Apply Canny edge detection for comparison.
Calculate and save evaluation metrics (MSE, SSIM, ORB matches).
Save results (processed images and metrics) to the specified directories.
View the Results:

After the notebook finishes executing, you will find the processed images saved in the results directory and the corresponding metrics in the metrics directory. Each file will be saved with a unique name based on the image it corresponds to.
Directory Structure
The expected directory structure after running the notebook is as follows:

bash
Copy code
├── cos791
│   ├── results            # Directory for processed images
│   ├── metrics            # Directory for evaluation metrics
│   ├── image1.png         # Example image file
│   ├── image2.jpg         # Example image file
│   └── ...
Customization Options
Noise Reduction Method:

The noise reduction can be applied using Gaussian, median, or bilateral filtering. You can adjust this by modifying the method argument in the noise_reduction function.
Gradient Calculation Method:

The gradient calculation can be performed using Sobel, Prewitt, or Laplacian operators. This can be changed by altering the method argument in the gradient_calculation function.
Thresholding Values:

You can modify the lower and upper threshold values for edge detection in the apply_threshold and canny_edge_detection functions.
Evaluation Metrics
The following metrics are computed for each image:

Mean Squared Error (MSE): Measures the difference between the custom pipeline and Canny edge detection results.
Structural Similarity Index (SSIM): Evaluates the similarity between two images.
ORB Feature Matches: Counts the number of key feature matches between the two sets of edges.
Each metric is saved in a text file in the metrics directory for each image.
