# Data Anonymization Using Pseudonym System to Preserve Data Privacy

## Description

This project is a data anonymization tool that employs a pseudonym system to maintain data privacy. It features user registration and recognition through image processing and pseudonym generation. The system combines image processing techniques, secure hashing, and file storage via FTP to anonymize and authenticate users.

## Features

- **User Registration**: Register new users by processing images, generating pseudonyms, and storing them with associated messages.
- **User Recognition**: Authenticate users by verifying pseudonyms and retrieving their data from an FTP server.
- **Image Processing**: Utilizes Gaussian blur, median blur, grayscale conversion, CLAHE (Contrast Limited Adaptive Histogram Equalization), and edge detection.
- **Pseudonym Generation**: Creates a secure pseudonym using SHA256 hashing based on image processing results and user data.
- **FTP Integration**: Stores and retrieves pseudonym data on an FTP server.

## Installation

### Prerequisites

- Python 3.x
- Required Python libraries:
  - `numpy`
  - `opencv-python`
  - `scipy`
  - `ftplib` (part of the Python standard library)

You can install the required libraries using pip:

```bash
pip install numpy opencv-python scipy
```


## Usage

1. Run the script:
   ```bash
   python your_script_name.py
   ```
2. The GUI will appear with options for user registration and recognition.

### User Registration

- Enter the username and message.
- Click the "Registration Module" button.
- Select an image file for processing.

### User Recognition

- Enter the username.
- Click the "Recognition Module" button.
- Select an image file for processing.

## Functions

- `create_sha256_signature(key, message)`: Creates a SHA256 hash for the given message using the provided key.
- `upload()`: Opens a file dialog to select a file.
- `userRegister()`: Manages user registration by processing an image, generating a pseudonym, and uploading it to the FTP server.
- `userRecognition()`: Manages user recognition by retrieving pseudonym data from the FTP server and verifying it.

## FTP Configuration

- Update the FTP server details and credentials in the `userRegister` and `userRecognition` functions:
  ```python
  ftp = ftplib.FTP_TLS("ftp.drivehq.com")
  drivehq_username = 'your_username'
  drivehq_password = 'your_password'
  ```


## Acknowledgments

- Utilizes the OpenCV library for image processing and HMAC for secure pseudonym generation.
- Inspired by data privacy and security best practices.

