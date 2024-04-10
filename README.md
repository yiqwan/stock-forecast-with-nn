# Stock Price Forecasting with Neural Networks

This is a stock price forecasting project done with different neural networks during the module CZ4042 Neural Networks &amp; Deep Learning in NTU

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. You should already have cloned this repository to your device.

### Prerequisites

Before you begin, ensure you have met the following requirements:
* You have installed the latest version of Python.
* You have a Windows/Linux/Mac machine. This code is tested on Python 3.11.3, Apple M1 13.6.1 (22G313).

### Virtual environment

#### For MacOS
1. Navigate to your project directory: Use the cd command to change to your project directory. Replace /path/to/your/project with the actual path to your project directory.

`cd /path/to/your/project`

2. Create a virtual environment: Run the following command to create a virtual environment named venv within your project directory. You can replace venv with any name you prefer for your virtual environment.

`python3 -m venv venv`

3. Activate the virtual environment: To start using the virtual environment, you need to activate it with the following command:

`source venv/bin/activate`

4. After this command, you can install all the dependencies by running the following command in your terminal:

`pip install -r requirements.txt`

This command will automatically install all the dependencies listed in the requirements.txt file.

5. Deactivate the virtual environment: (only when you stop running any files)

`deactivate`

#### For Windows

Similar steps but different command.

1. Navigate to your project directory:

`cd \path\to\your\project`

2. Create a virtual environment:

`python -m venv venv`

3. Activate the virtual environment:

`.\venv\Scripts\activate`

4. Install dependencies:

`pip install -r requirements.txt`

5. Deactivate the virtual environment only when you don't need to run any files:

`deactivate`

### Configuration

After installing the dependencies, you need to set up the environment variable required for the project:

1. Create a file named .env in the root directory of the project.
2. Add the following line to the .env file:

`ROOT_DIR={Your root folder}`

This will set the ROOT_DIR environment variable to your root folder's name, which the project requires for proper execution.

### Setting Up the Device for PyTorch

The project uses PyTorch for model training and inference. Depending on your system, you might want to change the device PyTorch uses:

For Windows/Linux Users: It's recommended to use CUDA if you have a compatible NVIDIA GPU for faster computation. Update the DEVICE setting in model.ipynb as follows:

`DEVICE = torch.device('cuda' if torch.cuda.is_available() else 'cpu')`

For macOS Users: Due to the lack of NVIDIA GPU support, it's recommended to remain using the CPU or Apple's Metal if compatible. The default setting should work fine, but you can explicitly set it to CPU as follows:

`DEVICE = torch.device('cpu')`

### Running the Project

To run the project, open the model.ipynb notebook in Jupyter Notebook or JupyterLab and follow the instructions within.