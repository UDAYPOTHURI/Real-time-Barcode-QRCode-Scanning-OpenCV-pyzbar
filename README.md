# Real-time-Barcode-QRCode-Scanning-OpenCV-pyzbar

This project uses OpenCV and pyzbar to perform real-time barcode and QR code scanning on a video stream from a webcam.

## Installation

To use this project, you'll need to have OpenCV and pyzbar installed. You can install them using pip:

pip install opencv-python

pip install pyzbar

You'll also need to download the `Real-time-Barcode-QRCode-Scanning-OpenCV-pyzbar.ipynb` file from the GitHub repository. You can do this by clicking on the "Code" button on the repository page and selecting "Download ZIP". Once you've downloaded and unzipped the file, you can open it in a Jupyter notebook.

## Usage

To use this project, simply run the `Real-time-Barcode-QRCode-Scanning-OpenCV-pyzbar.ipynb` file in a Jupyter notebook. The code will access your webcam and display a video stream with barcodes and QR codes detected in real-time.

Here's a detailed explanation of how the code works:

1. The code starts by importing the necessary libraries: `cv2` and `pyzbar`.
2. It then accesses the webcam using `cv2.VideoCapture()`.
3. A while loop is entered that runs until the user presses the "q" key.
4. Inside the loop, a frame is read from the webcam using `.read()`.
5. Barcodes and QR codes are detected in the frame using `pyzbar.decode()`.
6. If any barcodes or QR codes are detected, their coordinates are obtained from the returned list.
7. A for loop is entered that iterates over each detected barcode or QR code.
8. Inside the for loop, a rectangle is drawn around each barcode or QR code using `cv2.rectangle()`.
9. The data contained in each barcode or QR code is displayed on the frame using `cv2.putText()`.
10. The type of each barcode or QR code (e.g., "QRCODE", "EAN13") is also displayed on the frame using `cv2.putText()`.
11. The frame is displayed using `cv2.imshow()`.
12. The code waits for 1 millisecond for a key press using `cv2.waitKey()`. If the "q" key is pressed, the while loop is exited.
13. After exiting the while loop, the webcam is released using `.release()` and all windows are destroyed using `cv2.destroyAllWindows()`.
