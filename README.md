# Digital Media Integrity Checker

Digital Media Integrity Checker is an AI-powered Python tool designed to detect manipulated or forged images. It uses a combination of digital forensics techniques to check image authenticity and highlight suspicious regions. This project integrates methods such as double JPEG compression detection, CFA artifact analysis, and copy-move forgery detection to ensure comprehensive analysis of digital images.

# Features

Double JPEG Compression Detection – Identifies whether an image has been compressed multiple times, a common sign of forgery.

CFA (Color Filter Array) Artifact Detection – Detects inconsistencies in the sensor pattern to help identify tampered areas.

Copy-Move Forgery Detection – Locates regions that have been duplicated and moved within an image.

Noise Analysis – Detects unusual noise patterns indicative of manipulation.

Visual Output – Annotated images are saved for easy identification of suspicious regions.

# Project Structure
Digital-Media-Integrity-Checker/
│
├── images/                # Place images here to test

├── output/                # Processed images and results are saved here

├── src/                   # Python scripts for detection

│   ├── detect.py          # Main script to run all checks

│   ├── double_jpeg_compression.py

│   ├── copy_move_detection.py

│   ├── image_object.py

│   └── blocks.py

├── README.md              # This file

## Installation

Clone the repository

git clone https://github.com/sonalm3214/Digital-Media-Integrity-Checker.git
cd Digital-Media-Integrity-Checker


## Create and activate a virtual environment

# Windows:

python -m venv venv
venv\Scripts\activate


# Linux / macOS:

python -m venv venv
source venv/bin/activate


## Install all required Python libraries in one command

pip install numpy scipy opencv-python matplotlib pandas tqdm scikit-learn


This installs all dependencies needed for running the Digital Media Integrity Checker.

## Usage

Add your images to the images/ folder.

# Run the detection script:

cd src
python detect.py ../images/image.jpg


# Check the output:

# Terminal will show:

Double JPEG compression status (Single compressed / Double compressed)

CFA artifact count

output/ folder will contain annotated images highlighting suspicious regions (especially for copy-move detection).

# Tips

Ensure all dependencies are installed in your virtual environment.

Use high-quality images for better detection results.

The tool is designed for research, forensic analysis, and learning purposes.
