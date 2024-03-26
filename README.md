# Traffic Law Violation Detection System
## Introduction
The Vehicle Plate Number Recognition (VPNR) system is an advanced real-time application designed to automatically detect and recognize vehicle license plates. The primary goal is to identify vehicles that are in violation of traffic regulations using image processing techniques. The system captures an image of the vehicle, processes it to extract the license plate number, and displays it on a webpage accessible through an IP address. Implementation of this system can significantly contribute to road safety enhancement and traffic control in the burgeoning smart cities.

## Dataset
The dataset used for this project is sourced from Kaggle and includes 433 annotated images of car license plates. These annotations consist of bounding box coordinates identifying the location of the license plates within each image. Access to the dataset can be found at https://www.kaggle.com/andrewmvd/car-plate-detection.

## Methodology
The methodology of the VPNR system involves several key stages, as outlined below:

1) Vehicle's Number Plate Detection: Initial detection of the license plate within vehicle images and marking the detected region with a green rectangle.
2) Pre-processing Image: The image is converted to grayscale to simplify the recognition of the number plate.
3) Segmentation of Image: The grayscale image is segmented into multiple parts to facilitate easier analysis of each character on the license plate.
4) Training Model: A Convolutional Neural Network (CNN) model is created and trained to recognize and interpret the characters on the license plates.
5) Getting Vehicle's Info: The trained model is tested through an API that fetches the vehicle owner's information.

## Fetching Vehicle Details Using API
Vehicle details are obtained by querying an external API with the recognized license plate number. The API, provided by RegCheck, returns XML data, which is then parsed into a dictionary and subsequently converted into JSON format for easier manipulation and display of relevant vehicle information.
