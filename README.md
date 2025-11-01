# 🎨 Pix-Palette: K-Means Dominant Color Extractor

This project demonstrates the core concepts of **Unsupervised Machine Learning**, **Feature Engineering**, and **Data Reduction** by automatically extracting the dominant color palette from any input image, shrinking millions of color values to an interpretable few. The solution uses the **_K-Means Clustering_** algorithm to group millions of individual pixel colors into a specified number of representative colors, which are then displayed in a proportional palette with their RGB values.

* Unsupervised Learning: The model works entirely on its own, without needing to be "trained" on pre-labeled data. It discovers the patterns (the clusters of color) inherent in the image data.

* Feature Engineering: We tell the model to ignore where a pixel is located (its spatial coordinates) and focus only on its color value, which is the key feature needed to find the color groups.

* Data Reduction: The project shrinks a massive dataset (millions of colors) down to a small, meaningful set of colors (K=5), which is a core task in machine learning and data analysis.

## ✨ Final Showcase

Here is the dominant color palette extracted from a sample input image (using K=5 clusters), with the colors sorted by their frequency (proportion) in the image:

![Dominant Color Palette Output](showcase_palette_output.png)

## ⚙️ Technical Details

| Component | Technology / Concept | Key Takeaway |
| :--- | :--- | :--- |
| **Algorithm** | K-Means Clustering (Unsupervised Learning) | Learns patterns in data without pre-labeled categories. |
| **Data Prep** | NumPy `reshape` | Converts the 3D image array (Height x Width x RGB) into a 2D feature vector (Pixels x RGB). |
| **Sorting Stability** | Python List Sorting (`lambda`) | Ensures the visual output is consistent across runs by sorting colors based on frequency. |
| **Libraries** | `scikit-learn`, `NumPy`, `PIL`, `Matplotlib` | Standard tools for ML model building and visualization in Python. |

## 🚀 How to Run the Project

### Prerequisites

1.  **Python 3.x** installed.
2.  A **Virtual Environment (`venv`)** must be created and activated.
3.  Install dependencies: `pip install numpy Pillow scikit-learn matplotlib`

### Steps

1.  **Clone the Repository:**
    ```bash
    git clone https://github.com/drew-1618/K-Means_image_palette_extractor.git
    cd K-Means_image_palette_extractor
    # Activate your venv here
    ```

2.  **Add Your Image:**
    * Create a folder named `images/source/` in the project root.
    * Place your chosen image (e.g., `my_photo.jpg`) inside that folder.

3.  **Run the Notebook:**
    * Open `palette-extractor.ipynb` in VSCode or Jupyter.
    * Update the `IMAGE_PATH` variable to point to your file.
    * Run all cells to see the generated palette!
