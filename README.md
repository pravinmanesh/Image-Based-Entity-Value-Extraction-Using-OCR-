# **Image-Based Entity Value Extraction Using OCR**

This repository contains a Python project that utilizes Optical Character Recognition (OCR) to extract specific entity values (like voltage, wattage, weight, dimensions, etc.) from product images. The extracted values are compared with actual values for accurate predictions, with a focus on handling various units of measurement and converting them into human-readable formats.

## **Key Features**

- **OCR Integration**: Leverages the Tesseract OCR engine to extract text from images using custom configuration settings.
- **Entity Value Extraction**: Implements a robust regex-based approach to extract numerical values and associated units like "cm", "kg", "W", etc., for various product attributes (e.g., voltage, item weight, item volume, height, width, depth).
- **Unit Normalization**: Includes a unit conversion system that standardizes different formats (e.g., converting “cm” to “centimetre”) and processes them for consistency.
- **Dynamic Dataset Handling**: Loads product images and metadata from a CSV file, processes each image, and generates predictions in a structured format.
- **Support for Multiple Entities**: Handles different entity types (like voltage, wattage, item volume, dimensions) and applies specific extraction patterns for each.
- **Error Handling**: Includes exception handling to ensure smooth execution even when encountering invalid image links or incorrect formats.

## **Project Structure**

- **`ocr_image`**: Function to extract text from an image using Tesseract OCR.
- **`extract_entity_value`**: Function to extract numerical values and units from the text and handle both single values and ranges.
- **`convert_unit_to_words`**: Function that converts units like "cm", "kg", etc., into their word equivalents for easier interpretation.
- **Dataset Processing**: The project reads a CSV file containing image links and metadata, downloads images, applies OCR, extracts entity values, and converts them into a human-readable format.
- **Predictions**: The results are stored in a new CSV file, which contains the extracted predictions in word format.

## **Technologies Used**

- **Python**: Core programming language.
- **OpenCV**: Image processing.
- **Pytesseract**: OCR engine.
- **Regex**: Extracting numerical values and associated units.
- **Pandas**: Dataset handling and CSV manipulation.
