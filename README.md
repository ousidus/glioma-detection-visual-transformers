# **glioma-detection-visual-transformers**

## **Project Overview**
This repository implements a glioma detection system using Visual Transformers. Gliomas are a type of tumor that occur in the brain and spinal cord. Early detection is crucial for improving treatment outcomes. Visual Transformers leverage attention mechanisms in image processing, offering improved performance over traditional methods like Convolutional Neural Networks (CNNs).
You can read about performance and results in my [Master diploma](https://www.overleaf.com/read/cfbyrxrjmvhv#932c28).


This project includes:
- **Data preparation**: MRI/CT images, data augmentation using GANs.
- **Model**: Visual Transformers for image classification.
- **API**: REST API for real-time glioma detection.

## **Installation Guide**
Follow these steps to set up the project locally:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/ousidus/glioma-detection-visual-transformers.git
   cd glioma-detection-visual-transformers
2. **Create a virtual environment (optional but recommended):**

    ```bash
    python3 -m venv venv
    source venv/bin/activate  # For Linux/Mac
    # or
    .\venv\Scripts\activate   # For Windows

3. **Install dependencies:**
    ```bash
    pip install -r requirements.txt

4. **Set up Docker (optional): If you want to run the project in a containerized environment, build and run the Docker image:**

    ```bash
    docker build -t glioma-detection .
    docker run -p 5000:5000 glioma-detection

## Usage
You can run the model or the REST API using the following instructions:

### Run the Model Locally
1. Ensure your environment is set up and dependencies are installed.

2. Train the model:
    ```bash
    Ensure your environment is set up and dependencies are installed.
3. Use the trained model to detect gliomas in images:
    ```bash
    python detect.py --image_path /path/to/image

### Run the REST API
1. Start the API server:
    ```bash
    python app.py  # Assumes Flask or FastAPI is being used
2. Send a POST request to the /detect endpoint with an MRI/CT image:

    ```bash
    curl -X POST http://localhost:5000/detect -F "image=@/path/to/image"

### Scheduled Tasks
To retrain the model periodically, use the following command:

    ```bash
    python retrain_model.py

## Contributing Guidelines
We welcome contributions from the community. To contribute:

1. Fork the repository.

2. Create a new branch for your feature or bug fix:
    ```bash
    git checkout -b feature-name

3. Ensure your code follows our coding standards:

* Use black for code formatting.
* Run flake8 for linting.
* Write unit tests for new features in the tests/ directory.

4. Submit a pull request to the main branch.

* Ensure that all tests pass before submitting.
* Provide a detailed description of your changes.

## License
This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for more details.

