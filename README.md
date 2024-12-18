# 🥔 Potato Disease Prediction

An AI-powered application that detects diseases in potato plants using deep learning. The system can identify Early
Blight, Late Blight, and Healthy potato plants from images with high accuracy.

## 🌟 Features

- Real-time disease prediction
- Support for both local model inference and TensorFlow Serving
- REST API implementation using FastAPI
- Cross-Origin Resource Sharing (CORS) support
- High accuracy disease classification
- Confidence score for predictions

## 🏗️ Project Structure

```
Potato_Disease_Prediction/
├── api/
│   ├── main.py                # FastAPI implementation with local model
│   └── main_tf_serving.py     # FastAPI implementation with TF Serving
├── saved_models/             # Directory containing trained models
│   ├── 1/
│   ├── 2/
│   └── 3/
├── training/
│   ├── PlantVillage/         # Dataset directory
│   ├── PlantVillage.zip      # Compressed dataset
│   └── training.ipynb        # Model training notebook
├── .gitignore
├── LICENSE
├── models.config
├── README.md
└── requirements.txt
```

## 🚀 Getting Started

### Prerequisites

- Python 3.7+
- TensorFlow 2.x
- FastAPI
- Uvicorn
- Pillow
- NumPy
- TensorFlow Serving (optional)

### Installation

1. Clone the repository:

```bash
git clone https://github.com/mustafoyev-202/Potato_Disease_Prediction.git
cd Potato_Disease_Prediction
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Start the API server:

For local model inference:

```bash
cd api
python main.py
```

For TensorFlow Serving:

```bash
cd api
python main_tf_serving.py
```

## 🔄 API Endpoints

### Health Check

```
GET /ping
Response: "Hello, I am alive"
```

### Disease Prediction

```
POST /predict
Request: Form-data with image file
Response: {
    "class": "Disease class name",
    "confidence": confidence_score
}
```

## 📊 Model Information

The model can predict three classes:

- Early Blight
- Late Blight
- Healthy

The prediction comes with a confidence score indicating the model's certainty about its prediction.

## 🔧 Configuration

### CORS Settings

The API allows requests from:

- http://localhost
- http://localhost:3000

You can modify the allowed origins in `main.py` or `main_tf_serving.py`.

### TensorFlow Serving

If using TensorFlow Serving, ensure the service is running at:

```
http://localhost:8501/v1/models/potatoes_model:predict
```

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the terms specified in the `LICENSE` file.

## 👥 Authors

- Baxtiyor - *Initial work*

## 🙏 Acknowledgments

- PlantVillage Dataset
- TensorFlow Team
- FastAPI developers

## 📫 Contact

Baxtiyor - baxtiyormustafoyev2006@gmail.com
Project
Link: https://github.com/mustafoyev-202/Potato_Disease_Prediction