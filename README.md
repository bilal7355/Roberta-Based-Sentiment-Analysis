# RoBERTa-Based Sentiment Analysis

This repository provides a framework for performing sentiment analysis using a fine-tuned RoBERTa model. The project includes a Jupyter notebook for model training and evaluation, as well as a Flask web application for deploying the model as a web service.

## Repository Structure

- `roberta_based_sentiment_analysis.ipynb`: Jupyter notebook containing the code for training and evaluating the RoBERTa model.
- `app.py`: Flask application script for serving the trained model as a web service.
- `templates/`: Directory containing HTML templates for the web application's user interface.

## NOTE: Use Virtual Environment to not face dependency issues

1. **Create a Virtual Enviornment**:
   ### Windows:
   ```bash
   python -m venv myenv
   ```
   ### Mac:
   ```bash
   python3 -m venv myenv
   ```
2. **Activate the Virtual Enviornment**(In cmd or VS Code):
   ### Windows:
   ```bash
   myenv\Scripts\activate
   ```
   ### Mac:
   ```bash
   source myenv\bin\activate
   ```
   
## Prerequisites

Before running the code, ensure you have the following installed:

- Python 3.6 or higher
- Required Python packages listed in `requirements.txt`

Install the necessary packages using:

```bash
pip install -r requirements.txt
```
   
## Deploying the Model

To deploy the trained model as a web service:

1. **Run the Flask Application**: Start the Flask web server:
   ### Windows:
   ```bash
   python app.py
   ```
   ### Mac:
   ```bash
   python3 app.py
   ```

   The application will be accessible at `http://127.0.0.1:5000/`. You can input text through the web interface to receive sentiment predictions from the model.

## Notes

- Ensure that the model and tokenizer are saved and loaded correctly to avoid compatibility issues.
- The `app.py` script is configured to load models saved in the Hugging Face Transformers format. If you encounter issues with loading models in different formats (e.g., `model.safetensors`), consider converting or saving the model in a compatible format.

For more detailed information and troubleshooting, refer to the official [Hugging Face Transformers documentation](https://huggingface.co/transformers/). 
