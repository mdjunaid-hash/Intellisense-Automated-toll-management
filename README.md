# Intellisense-Automated-toll-management
-IntelliSense with an Automatic Number Plate Recognition system could imply adding intelligent features to the toll collection process. This might involve using machine learning algorithms or advanced analytics to optimize toll Wait time, detect anomalies, or enhance overall system efficiency.

-Tools & technologies used: Python Language, Server on MongoDB, Backend Web development, ESP32 Micrcontroller, Wireless
Communication, Data Transfering.

# Automated Toll Billing System

This repository provides an automated system for processing vehicle toll data, including image processing, Optical Character Recognition (OCR), data extraction, and automated email notifications. The system integrates with Google Drive for file storage and utilizes several Python libraries for its operations.

## Installation

### Prerequisites
- Python 3.x
- Required Libraries: `openpyxl`, `opencv-python`, `pytesseract`, `numpy`, `pydrive`, `Pillow`, `reportlab`
- Tesseract OCR installed
- Google Drive API credentials

### Installing Libraries
Install the required libraries using `pip`:
```bash
pip install openpyxl opencv-python pytesseract numpy pydrive Pillow reportlab
```

### Tesseract OCR Configuration
Download and install Tesseract OCR, then set the path in the script:
```python
pytesseract.pytesseract.tesseract_cmd = r'C:\Program Files\Tesseract-OCR\tesseract.exe'
```

### Google Drive API Setup
- Set up Google Drive API and download `client_secrets.json`.
- Place `client_secrets.json` in the root directory of the project.

## Usage

1. **Download Images**:
    - Configure `folder` and `download_directory` in the script for Google Drive folder ID and local directory.
2. **Process Images**:
    - The script processes images to extract vehicle number plates.
3. **Generate Excel and PDF**:
    - Saves extracted data in an Excel file and converts it to a PDF.
4. **Upload to Google Drive**:
    - Uploads the PDF to a specified Google Drive folder.
5. **Send Email**:
    - Sends an email with the PDF attached to the vehicle owner's email address.

### Running the Script
Execute the script to start the process:
```bash
python toll_billing_system.py
```

## Features

- **Image Processing**: Crops, enlarges, and enhances vehicle images for better OCR accuracy.
- **OCR**: Extracts text from processed images using Tesseract OCR.
- **Data Handling**: Saves extracted data to Excel, converts to PDF, and uploads to Google Drive.
- **Email Notification**: Sends an automated email with the toll bill.

## Project Structure

```
|-- toll_billing_system.py  # Main script
|-- client_secrets.json  # Google API credentials
|-- README.md  # Project README
```

## License

This project is licensed under the MIT License. See the LICENSE file for details.
