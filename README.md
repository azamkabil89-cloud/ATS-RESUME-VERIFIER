# ATS Resume Checker

A Streamlit app that reads a resume (PDF, DOCX, TXT), uses Google Gemini Flash to give an ATS score, and lists improvements.

## Run locally

```bash
pip install -r requirements.txt
streamlit run app.py
```

Get a free API key at https://aistudio.google.com/apikey. Paste it in the app, or create `.streamlit/secrets.toml`:

```toml
GEMINI_API_KEY = "your-key-here"
```

(Do not upload `secrets.toml` to GitHub.)

## Push to GitHub (website only)

1. Go to https://github.com and sign in, click **+** (top right) > **New repository**.
2. Name it `ats-resume-checker`, set Public, click **Create repository**.
3. Click **uploading an existing file**.
4. Drag in `app.py`, `requirements.txt`, `README.md`, then click **Commit changes**.

## Deploy on Streamlit Cloud

1. Go to https://share.streamlit.io and sign in with GitHub.
2. Click **Create app** > **Deploy a public app from GitHub**.
3. Choose your repository, branch `main`, main file `app.py`.
4. Open **Advanced settings** > **Secrets** and paste:
   `GEMINI_API_KEY = "your-key-here"`
5. Click **Deploy**. Your app gets a public link in a minute or two.
