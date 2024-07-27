# Quiz Manager and Streamlit Quiz Application

## Description

This project is an interactive quiz application built with Streamlit, leveraging natural language processing and document processing capabilities. It allows users to generate quizzes based on uploaded documents, creating an engaging and dynamic learning experience.

Key features:
- Document ingestion and processing
- Quiz generation based on document content
- Interactive quiz interface with multiple-choice questions
- Navigation between questions
- Immediate feedback on answers

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Dependencies](#dependencies)
- [Configuration](#configuration)
- [Contributing](#contributing)
- [License](#license)

## Installation

1. Clone the repository:
   ```
   git clone https://github.com/your-username/quiz-manager-streamlit.git
   cd quiz-manager-streamlit
   ```

2. Set up a virtual environment (optional but recommended):
   ```
   python -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   ```

3. Install the required dependencies:
   ```
   pip install -r requirements.txt
   ```

4. Set up Google Cloud credentials:
   - Create a Google Cloud project and enable the necessary APIs (e.g., TextEmbedding API)
   - Download the JSON key file for your service account
   - Set the `GOOGLE_APPLICATION_CREDENTIALS` environment variable to the path of your JSON key file:
     ```
     export GOOGLE_APPLICATION_CREDENTIALS="/path/to/your/keyfile.json"
     ```

## Usage

1. Start the Streamlit application:
   ```
   streamlit run main.py
   ```

2. Open your web browser and navigate to the URL displayed in the terminal (usually `http://localhost:8501`)

3. Use the application:
   - Upload PDF documents for ingestion
   - Enter a topic for the quiz
   - Select the number of questions
   - Click "Submit" to generate the quiz
   - Answer the questions and navigate through the quiz
   - Receive immediate feedback on your answers

## Project Structure

```
quiz-manager-streamlit/
├── main.py
├── requirements.txt
├── README.md
├── tasks/
│   ├── task_1/
│   │   └── task_1.py
│   ├── task_2/
│   │   └── task_2.py
│   ├── task_3/
│   │   └── task_3.py
│   ├── task_4/
│   │   └── task_4.py
│   ├── task_5/
│   │   └── task_5.py
│   ├── task_6/
│   │   └── task_6.py
│   ├── task_7/
│   │   └── task_7.py
│   ├── task_8/
│   │   └── task_8.py
│   ├── task_9/
│   │   └── task_9.py
│   └── task_10/
│       └── task_10.py
└── venv/
```

## Dependencies

- streamlit
- google-cloud-aiplatform
- chromadb
- langchain
- PyPDF2

For a complete list of dependencies and their versions, see `requirements.txt`.

## Configuration

Update the `embed_config` dictionary in `main.py` with your Google Cloud project details:

```python
embed_config = {
    "model_name": "textembedding-gecko@003",
    "project": "YOUR-PROJECT-ID-HERE",
    "location": "us-central1"
}
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
