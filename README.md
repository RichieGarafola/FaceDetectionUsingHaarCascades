
# Face Detection and Classification Using Haar Cascades

This project demonstrates how to perform **face detection** using OpenCV’s **Haar Cascade Classifiers**. It processes an entire folder of images, detects faces, and organizes the results into *positives* and *negatives* based on detection success.

> Developed as part of Capella University coursework  
> Useful for anyone exploring face detection using classical computer vision techniques.

---

## Features

- Batch image processing
- Multi-cascade Haar face detection
- Classification into `Positives/` and `Negatives/`
- Face annotation with bounding boxes
- Organized output directory for review and inspection

---

## Project Structure

```bash
.
├── Assessment4_FaceDetection.ipynb       # Main notebook
├── haarcascades/                         # Folder with Haar XML files
├── dataset/                              # Your input images
├── output/
│   ├── Positives/                        # Detected faces (with bounding boxes)
│   └── Negatives/                        # No detected faces
├── requirements.txt
└── README.md
```

---

## How to Use

1. **Install dependencies** (recommended: Python 3.8+):

```bash
pip install -r requirements.txt
```

Or manually:

```bash
pip install opencv-python matplotlib
```

2. **Prepare folders:**
   - Place Haar XML files into a `haarcascades/` directory
   - Add test images into a `dataset/` folder

3. **Run the notebook:**

```bash
jupyter notebook FaceDetection.ipynb
```

You’ll be prompted for:
- Haar cascade folder path
- Dataset image path
- Output directory path

---

## Algorithms & Techniques

- **Grayscale Conversion**: Converts all images before detection
- **Haar Cascades**: Uses multiple pre-trained models:
  - `haarcascade_frontalface_default.xml`
  - `haarcascade_frontalface_alt2.xml`
  - `haarcascade_frontalface_alt_tree.xml`
  - `haarcascade_profileface.xml`
- **Image Resizing**: Downsizes large images to reduce memory usage
- **Face Detection**: Draws bounding boxes using `cv2.rectangle`
- **Output Sorting**:
  - Images with faces → `/Positives`
  - Images without faces → `/Negatives`

---

## Output Example

| Result Type | Example Description       |
|-------------|----------------------------|
| Positive    | Face detected and boxed    |
| Negative    | Image copied untouched     |

> *(Visual previews can be added if stored in output folders.)*

---

## Learning Objectives

- Understand how Haar Cascades detect human faces
- Apply classic CV techniques to bulk datasets
- Implement robust output validation and classification
- Gain exposure to OpenCV’s `CascadeClassifier` object

---

## License

This repository is for educational use.  
Attribution is appreciated if reused or adapted.

---

## Acknowledgements

- OpenCV team for Haar cascade XMLs  
- Capella University – CSC‑FPX4040

---
