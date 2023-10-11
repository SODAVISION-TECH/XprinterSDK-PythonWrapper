# XprinterSDK-PythonWrapper

## Description

A Python interface for interacting with printers using the Xprinter SDK. This project provides a Pythonic way to control printer operations such as printing text, images, and QR codes.

## Requirements

- Python 3.6 and above
- Xprinter SDK DLL files, downloaded from Xprinter website.
- ctypes library

## Features

- Initialize printer
- Open printer port
- Print text and images
- Set font and text alignment
- Print QR codes
- Cut paper

## Installation

1. Make sure you have Python installed on your machine.
2. Download the Xprinter SDK and locate the DLL files.
3. Clone this repository or download the Python script.

## Usage

### Import the necessary libraries

```python
from ctypes import CDLL, c_void_p, c_int, c_char_p, c_wchar_p
```

### Initialize the Printer

```python
printer = InitPrinter("")
ret = OpenPort(printer, "USB,")
```

### Print Text

```python
print_text(printer, b"Hello, World!")
```

### Print Image

```python
print_image(printer, 'path/to/image.png', 0)
```

### Print QR Code

```python
PrintSymbol(printer, 49, b"qrcode-data", 48, 10, 10, 1)
```

## Troubleshooting

If you encounter any errors, check the error codes returned by the SDK functions and refer to the SDK documentation for guidance.

## Contributions

Feel free to fork this repository and submit pull requests. You can also report any issues you find.

## Contact

For any questions, issues, or support, feel free to reach out at tech@sodavision.com.

## License

This project is licensed under the MIT License - see the LICENSE.md file for details.
