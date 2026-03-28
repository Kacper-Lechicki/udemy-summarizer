# Udemy Summarizer

Paste a Udemy lesson URL and get a structured summary powered by OpenAI.

The notebook extracts the lecture transcript via the Udemy API, cleans it, and feeds it to GPT-4o-mini to produce concise, actionable notes.

## How it works

1. **Parse** the lesson URL to extract the course slug and lecture ID
2. **Fetch** the auto-generated transcript through the Udemy API
3. **Summarize** the transcript into a structured format:
   - Lesson Goal
   - Key Concepts
   - Main Takeaways
   - Shortened Content
   - Practical Application

## Setup

**Prerequisites:** Python 3.13+, [uv](https://docs.astral.sh/uv/)

```bash
# Install dependencies
uv sync

# Configure API keys
cp .env.example .env
# Edit .env with your OpenAI API key and Udemy Bearer token
```

### Getting your Udemy token

1. Log in to Udemy in your browser
2. Open DevTools (F12) → Network tab
3. Navigate to any course page
4. Find a request to `udemy.com/api-2.0/` and copy the `Authorization: Bearer <token>` value

## Usage

Open `notebook.ipynb`, set `LESSON_URL` to any lecture you're enrolled in, and run all cells.

## License

MIT
