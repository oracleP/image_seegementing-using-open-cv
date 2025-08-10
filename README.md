#i mage_segementing - using-open-cv
🧠 Image Segmenting using OpenCV
This project demonstrates various image segmentation techniques using OpenCV and Matplotlib in Python. It includes adaptive thresholding, simple thresholding, watershed segmentation, contour detection, morphological operations, and K-Means clustering for identifying and separating visual components from images (like coins or shapes).

🧰 Techniques Used
Simple Thresholding

Adaptive Thresholding (Mean & Gaussian)

Morphological Operations (Opening, Dilation)

Distance Transform

Watershed Algorithm

Contour Detection & Labeling

K-Means Clustering

📁 Folder Structure
image_seegementing-using-open-cv/
│
├── images/                     # Sample input images (currency.png, shape.png, etc.)
├── segment_image.py           # All segmentation logic
├── utils.py                   # Optional helper functions
├── requirements.txt
└── README.md
📦 Installation
Clone the repository

git clone https://github.com/your-username/image_seegementing-using-open-cv.git
cd image_seegementing-using-open-cv
Create a virtual environment (optional)

python -m venv venv
source venv/bin/activate      # Windows: venv\Scripts\activate
Install dependencies

pip install -r requirements.txt
requirements.txt
opencv-python
numpy
matplotlib
🚀 Usage
You can run segment_image.py or copy/paste sections for testing.

python segment_image.py
Or run segmentation cells in a Jupyter Notebook.
🖼️ Examples & Output
🔹 Original vs Segmented (KMeans)
plt.figure(figsize=(12,7))
plt.subplot(1,2,1)
plt.imshow(image)
plt.title("Original image")

plt.subplot(1,2,2)
plt.imshow(segmented_image)
plt.title("Segmented image")
plt.show()
🔹 Coin Detection with Watershed
plt.figure(figsize=(15,10))
plt.subplot(1,3,1)
plt.imshow(image)
plt.title("Original image")

plt.subplot(1,3,2)
plt.imshow(original_image)
plt.title("Labeled Coins")

plt.subplot(1,3,3)
plt.imshow(coin_mask)
plt.title("Final coin mask")
plt.show()
🔹 Adaptive Thresholding
plt.imshow(adaptive_m, cmap='gray')
plt.title("Adaptive Mean Thresholding")

plt.imshow(adaptive_g, cmap='gray')
plt.title("Adaptive Gaussian Thresholding")
🧪 Supported Image Files
currency.png — For coin segmentation (Watershed)

shape.png — For KMeans segmentation

pics.jpg — For simple/adaptive thresholding

Make sure to store your images in a local images/ folder or update the image paths accordingly.

🔧 Core Functions
cv2.threshold()

cv2.adaptiveThreshold()

cv2.morphologyEx()

cv2.distanceTransform()

cv2.findContours()

cv2.kmeans()

cv2.watershed()

📌 Notes
Circularity is calculated to identify coin-like objects:

circularity = 4 * π * (area / perimeter²)
KMeans clustering reshapes the image into pixel vectors and then re-labels them.

Distance transform is used to refine the foreground for Watershed.

🤝 Contributing
Found a bug or have a cool feature to add? Feel free to submit a pull request or open an issue.
