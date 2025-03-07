Text-to-Title Flask API

This is a Flask-based API for generating concise titles from input text using a fine-tuned transformer model.

🚀 Features

Uses google/roberta2roberta_L-24_gigaword model for title generation

Flask API with a /generate-title endpoint

Supports CORS for cross-origin requests

Simple JSON input & output

📌 Installation

1️⃣ Clone the Repository

git clone https://github.com/mortiestmorty1/text-to-title-flask-api.git
cd text-to-title-flask-api

2️⃣ Install Dependencies

Make sure you have Python 3.8+ installed. Then run:

pip install -r requirements.txt

3️⃣ Download & Place the Model

Ensure that the models directory contains the necessary model files (model.safetensors, tokenizer files, etc.). If missing, download the model from Hugging Face:

from transformers import AutoModelForSeq2SeqLM, AutoTokenizer
model_name = "google/roberta2roberta_L-24_gigaword"
tokenizer = AutoTokenizer.from_pretrained(model_name)
model = AutoModelForSeq2SeqLM.from_pretrained(model_name)
model.save_pretrained("./models")
tokenizer.save_pretrained("./models")

▶️ Running the API

Start the Flask server:

python app.py

The API will be available at:

http://127.0.0.1:5002

📡 API Usage

Endpoint: /generate-title

Method: POST

Request:

{
  "text": "The economy is expected to grow by 5% next year."
}

Response:

{
  "title": "Economy Growth Expected Next Year"
}

🛠️ Contributing

Fork the repository

Create a new branch (git checkout -b feature-name)

Commit your changes (git commit -m "Added new feature")

Push to your branch (git push origin feature-name)

Open a Pull Request

📜 License

This project is licensed under the MIT License.

Happy coding! 🚀

