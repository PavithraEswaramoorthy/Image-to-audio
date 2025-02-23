# Image-to-Audio Converter

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![OpenCV](https://img.shields.io/badge/OpenCV-4.x-green)
![Tesseract](https://img.shields.io/badge/Tesseract-OCR-lightgrey)

A Python-based utility that converts text-containing images to audio files using OCR and text-to-speech synthesis.

## Features
- **Image Processing**: Supports common formats (JPG, PNG, BMP)
- **OCR Integration**: Uses Tesseract for text extraction
- **Audio Generation**: Converts extracted text to MP3/WAV audio
- **Multi-language Support**: Works with English text (extendable to other languages)

## Requirements
- Python 3.8+
- Tesseract OCR 5.0+
- Required Python packages:

  ```bash
  pip install pillow pytesseract gtts opencv-python
  ```

## Usage
1. **Install Tesseract**:
   - Windows: [Installation guide](https://github.com/UB-Mannheim/tesseract/wiki)
   - Linux: `sudo apt install tesseract-ocr`

2. **Run the script**:
   ```python
   from image_to_audio import convert_image_to_audio
   
   convert_image_to_audio(
       input_path='sample.jpg',
       output_audio='output.mp3',
       language='eng'
   )
   ```

## Key Functions
- `preprocess_image()`: Enhances image readability using OpenCV
- `extract_text()`: Performs OCR using pytesseract
- `text_to_speech()`: Converts text to audio using gTTS

## Example
Input `sample.jpg`:
```
Hello World!
This text will be converted to audio.
```

Output `output.mp3` will contain spoken version of the extracted text.

## Limitations
- Requires clear text in images
- Accuracy depends on image quality
- Currently optimized for printed English text

## License
GNU GENERAL PUBLIC LICENSE. See [LICENSE](LICENSE) for details.

## Acknowledgments
- Tesseract OCR engine
- Google Text-to-Speech (gTTS)
- OpenCV community
