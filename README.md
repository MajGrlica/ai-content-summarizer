# AI Web & YouTube Content Summarizer

A robust Python command-line tool that automatically extracts transcripts from YouTube videos or text articles from web pages, analyzes them using the Google Gemini API, and generates structured Markdown research summaries.

## Features

- **Dual Source Support:** Automatically detects whether a given URL is a YouTube video or a general web page.
- **YouTube Integration:** Pulls video transcripts using `youtube-transcript-api` and retrieves official video titles via `oembed`.
- **Web Scraping & Extraction:** Cleans and extracts readable article text using `trafilatura`.
- **Structured AI Analysis:** Leverages Gemini to produce a standardized report containing:
  - 🎯 Executive Summary
  - 🔑 Core Takeaways
  - 💡 Key Details & Context
  - ⚠️ Caveats & Limitations
- **Automated Directory Management:** Dynamically creates and references a local `summaries` folder relative to the script's path using `__file__`.
- **Interactive CLI Loop:** Continuously prompts for links until you choose to exit.

## Prerequisites

- Python 3.8+
- A Google Gemini API Key.

## Installation

1. Clone or download this project into your local workspace.
2. Ensure your folder contains your main script (`main.py`) and a `summaries` folder (the script will also create this automatically if missing).
3. Install the required dependencies using pip:
   ```bash
   pip install -r requirements.txt
   ```

## Configuration

Open your main script file and ensure your Google Gemini API key is configured:
```python
client = genai.Client(api_key="YOUR_API_KEY")
```

## Usage

Run the script from your terminal:
```bash
python main.py
```

- When prompted, paste a YouTube video link or a web article URL.
- Type `q` or `quit` to exit the application.
- Your generated research analysis will automatically be saved as a Markdown file inside the `summaries/` folder.
