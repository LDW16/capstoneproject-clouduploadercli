# Capstone Project: CloudUploader CLI

## Overview
The CLI Uploader Tool is a command-line utility for encrypting files and uploading them to Google Cloud Storage. It offers features such as file encryption, shareable link generation, file synchronization, and error handling, ensuring a smooth and secure upload process.

## Prerequisites
Python 3.x

Google Cloud SDK

OpenSSL

## Installation
Python: Ensure Python 3.x is installed on your system. You can download it from python.org.

Google Cloud SDK: Follow the instructions here to install the Google Cloud SDK.

OpenSSL: OpenSSL should be pre-installed on most systems. Verify by running openssl version in your terminal.

## Setup
Clone the repository:
git clone https://github.com/lwil16/cliuploader.git

cd cliuploader

Install dependencies:
pip install -r requirements.txt

Authenticate with Google Cloud:
gcloud auth login

gcloud config set project YOUR_PROJECT_ID

## Usage
The tool can be used to upload files or directories to Google Cloud Storage, with optional encryption and shareable link generation.

### Basic Command

./cliuploader path/to/... --storage STANDARD --share --encrypt

### Options

--storage [STORAGE_CLASS]: Sets the storage class (e.g., STANDARD, NEARLINE, COLDLINE, ARCHIVE).

--share: Generates a shareable link for each uploaded file.

--encrypt: Encrypts the file before uploading using OpenSSL.

## Troubleshooting
### Common Issues

#### Google Cloud SDK Not Installed:

Error: gcloud: command not found

Solution: Ensure Google Cloud SDK is installed and added to your PATH.

#### Authentication Error:

Error: You are not logged in. Please run: $ gcloud auth login

Solution: Authenticate with Google Cloud by running gcloud auth login.

#### File Not Found:

Error: No such file or directory

Solution: Verify the file path is correct and the file exists.

#### Encryption Issues:

Error: OpenSSL command not found

Solution: Ensure OpenSSL is installed and available in your PATH. Verify by running openssl version.

#### Invalid Command Line Arguments:

Error: –share is not a valid file or directory

Solution: Ensure you are using double hyphens (--) for options, e.g., --share.

## Logs and Feedback
The tool provides success or error messages for each file upload and displays progress. Check these messages for detailed information on the upload status and any issues encountered.
