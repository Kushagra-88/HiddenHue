# Image Steganography

## Introduction

The **Image Steganography** project is a Python-based graphical user interface (GUI) application that allows users to hide and retrieve text-based information within digital images using the **Least Significant Bit (LSB) substitution** method. This technique provides a method for secure communication by embedding data into image files, ensuring that the visual appearance of the image remains virtually unchanged.

## Features

- **Text Encoding:** Hide sensitive information within an image (PNG, JPEG) using the LSB substitution technique.
- **Text Decoding:** Extract the hidden text from an encoded image.
- **Supported Image Formats:** PNG, JPEG.
- **User-Friendly Interface:** Easy-to-use GUI for encoding and decoding messages.
- **Secure Communication:** Provides an accessible method of data concealment and secure communication.

## How It Works

### Least Significant Bit (LSB) Method

The LSB method is a simple yet effective steganography technique. It works by modifying the least significant bit of pixel values in the image to embed secret data.

For example, if a pixel's RGB value is `(11011011, 10101010, 11110000)`, the LSB of each value can be modified without visibly altering the color. If we want to encode the binary value `101`:

- Red (R) value: `1101101**1**` becomes `1101101**0**`
- Green (G) value: `1010101**0**` stays the same
- Blue (B) value: `1111000**0**` stays the same

This process is repeated across the image pixels until the entire message is encoded.

## Requirements

To run this project, you need the following:

- Python 3.x
- `tkinter` for GUI
- `PIL` (Pillow) for image processing

Install dependencies with:

```bash
pip install pillow
