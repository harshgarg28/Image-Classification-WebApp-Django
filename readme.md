**Image Classification Webapp using Django**

Welcome! This README file will guide you through steps to run this webapp in local machine

### Prerequisites
- Python (3.6 or higher)
- Django
- TorchVision
- Torch
- Whitenoise (for serving static files)
- Gunicorn (for deploying to production)

* Clone this GitHUb repository to local storage

### Installation

1. Install Django, TorchVision, and Torch using pip:
    ```
    pip install django torchvision torch
    ```

2. Inside the GitHub folder run the following command to initialize
    ```
    python manage.py startapp image_classification
    ```

3. Run the Django development server:
    ```
    python manage.py runserver
    ```
   This will start the development server on `localhost:8000`.

4. Navigate to `localhost:8000` in your web browser to access the web application.

### Model
This Image Classification Webapp uses a DenseNet neural network pretrained on the ImageNet dataset to classify uploaded images. This functionality is contained within the image_classification/views.py module. When running the app first time it will download the pretrained model.

### classify--image.ipynb
this file contains a Resnet model trained using SAM optimizer, that I trained at first but later when its performance was bad, I used a pretrained DenseNet model because of lack of time and computational resources(because Google Colab credits were exhauseted). The performance of final model is satidfactory compared to the model I trained.
