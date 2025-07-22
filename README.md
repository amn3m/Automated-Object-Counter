# Object Counter Application using Digital Image Processing

This project is an automated object counting application that leverages fundamental digital image processing techniques to count objects in both static images and real-time video streams. It was developed to provide a fast, accurate, and efficient alternative to traditional manual counting methods.

## Project Overview

Traditional object counting—whether it's coins, machine parts on a conveyor belt, or cells in a petri dish—is often time-consuming, laborious, and prone to human error. This application solves that problem by automating the process using computer vision. By implementing a pipeline of image processing techniques, the system can distinguish objects from the background and count them with high accuracy. The application features a simple user interface for easy operation, allowing users to analyze either a pre-existing image or a live feed from a webcam.

## Key Features

*   **Static Image Counting:** Upload an image file (e.g., JPG, PNG) to count the objects within it.
*   **Real-Time Video Counting:** Use a connected webcam to perform live object counting in a video stream.
*   **Simple User Interface:** A clean and straightforward GUI for easy interaction.
*   **Accurate Detection:** Utilizes thresholding and contour detection to effectively identify and count objects.
*   **Versatile Application:** Can be adapted to count various types of objects, such as coins, cells, or industrial parts.

## Methodology & Technologies

The application follows a standard digital image processing workflow to identify and count objects.

### Development Flowchart
1.  **Image Acquisition:** The process starts with loading an image from a file or capturing a frame from a video stream.
2.  **Preprocessing:** The captured image is converted to grayscale to simplify subsequent processing steps.
3.  **Thresholding:** A binary threshold is applied to the grayscale image to separate the foreground objects from the background. This creates a black-and-white image where objects are clearly distinguished.
4.  **Contour Detection:** The application then finds the contours (i.e., the boundaries) of the white objects in the binary image. Each distinct contour is assumed to be a separate object.
5.  **Object Counting:** The system counts the number of contours detected.
6.  **Display Results:** The original image is displayed with the detected contours drawn around each object, and the final count is presented to the user.

### Technologies Used
*   **Language:** Python
*   **Libraries:**
    *   **OpenCV:** For all core image processing tasks (preprocessing, thresholding, contour detection) and video stream handling.
    *   **Tkinter (or similar):** For creating the graphical user interface.

## How to Use

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/amn3m/Automated-Object-Counter.git
    ```
2.  **Install the dependencies:**
    ```bash
    pip install opencv-python
    ```
3.  **Run the application:**
    ```bash
    python main.py
    ```
4.  **Using the GUI:**
    *   Click the **"Upload Image"** button to select an image file from your computer. The application will process it and display the result.
    *   Click the **"Start Video Stream"** button to begin real-time object counting using your webcam.

## Sample Result

Here is a sample screenshot of the application after processing an image of coins.

<img width="1002" height="848" alt="Screenshot 2024-05-25 135034" src="https://github.com/user-attachments/assets/8c76b9e7-f462-4b84-ae01-52948496bd00" />
