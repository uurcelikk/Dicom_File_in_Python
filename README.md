# Dicom File in Python

This repository serves as an example of working with DICOM files using Python, a common practice in the field of medical imaging. DICOM, which stands for Digital Imaging and Communications in Medicine, is a standard for storing images along with associated information such as patient data and imaging parameters. DICOM is widely used for the communication and management of medical imaging information and related data ([DICOM Standard](https://www.dicomstandard.org/about)).

## About DICOM

DICOM is a standardized file format used for storing and sharing medical images and other related data. Its standardization enables communication between various medical devices, making it an essential format for handling medical image data in hospitals and healthcare settings.

## Accessing DICOM Header Information

You can access DICOM tags by using hexadecimal encoded identifiers at the start of each line. For instance, to retrieve information about the image shape, you can use the following identifiers:

- (0028, 0010) Rows
- (0028, 0011) Columns
- (0018, 0015) Body Part Examined

The '0x' in front of the identifier signals the Python interpreter to interpret this value as hexadecimal. As an example, consider the following code snippet:

```python
print(dicom_file[0x0028, 0x0010])
print(dicom_file[0x0028, 0x0011])
print(dicom_file[0x0018, 0x0015])

# Alternatively, you can use the following syntax:
print('Rows: ', dicom_file.Rows)
print('Columns: ', dicom_file.Columns)
print('Body Part Examined: ', dicom_file.BodyPartExamined) 

