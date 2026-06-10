# T.ai — Minimal AI Search Assistant

T.ai is a lightweight AI alternative to Google Search.  
It’s designed to be fast, simple, and customizable — you bring your own Gemini API key, T.ai handles the rest.

> Made by **Ka Hei Chan** with help from **Gemini 3 Pro**.  
> Current internal version: **v12 (Internal Beta)**

---

## Features

- **Ask T.ai anything**  
  A single, clean text box: type a query and get an AI‑generated answer.

- **Image input**  
  Drag and drop an image to let T.ai analyse or describe it (where supported by the model / API).

- **Pluggable Gemini backend**  
  - Uses your own **Gemini API key** (not hard‑coded).
  - Default model: `gemma-4-31b-it` (editable in settings).

- **Personality presets**  
  - `Sassy & Bold`
  - `Normal & Fast`  
  The personality influences tone, not facts.

- **Personalisation panel**  
  Optional fields to lightly tune responses:
  - Name
  - Age
  - Gender
  - “Important things T.ai should know” free‑text field

- **Search engine compatible**  
  Can be set as a custom search engine with:
  `/?q=%s`

- **Fully client‑side UI**  
  HTML/CSS/JS front‑end intended for static hosting (e.g. Neocities).  
  No server‑side logging of queries is performed by T.ai itself.

---

## How It Works

1. You provide a **Gemini API key** in the settings panel.
2. T.ai uses that key in the browser to call the Gemini API.
3. The selected **model** and **personality** are sent as part of the prompt.
4. Answers are rendered directly in the page.

> ⚠️ T.ai is experimental. Answers may be incomplete, inaccurate, or unsafe.  
> Always fact‑check important information and use your own judgement.
---

## Usage

- Type your question in the “Ask T.ai anything” input.
- Press Enter or click the submit button.
- Wait for T.ai to stream or display a response.
- Optionally, drop an image into the “Drop image here” area to ask questions about the image (if implemented with your model).

You can set T.ai as a browser search engine with the URL:

https://globot.neocities.org/t.ai/?q=%s


---

## Security & Privacy

- T.ai is designed as a client‑side tool. There is no custom backend in this repo.
- All communication with Gemini happens directly from your browser to Google’s servers using your key.
- Do not:
  - Hard‑code API keys.
  - Commit `.env` or config files containing secrets.
- T.ai does not:
  - Intentionally log or store your queries on any server run by this project.
  - Take responsibility for how third‑party APIs (like Gemini) handle your data.

Review Google’s documentation and policies for how they process and store prompts and responses.

For more details, see the in‑app Terms and Conditions and Privacy Policy link.

---

## Limitations

- Answers can be wrong or misleading.
- Safety filters depend on the Gemini model and configuration.
- Certain features (e.g. images, streaming responses) may require:
  - specific browser capabilities, or
  - additional configuration in the code.

Always test with non‑sensitive, low‑risk queries first.

---

## Roadmap / Ideas

Some potential improvements:

- Conversation history with context window.
- “Search + AI” hybrid mode (web results + model reasoning).
- More personality presets and fine‑tuning of style.
- Keyboard shortcuts for power users.
---

---

## License

MIT License
Copyright (c) 2025 Ka Hei Chan

---

## Disclaimer

T.ai is an experimental tool and does not provide professional advice of any kind.  
By using T.ai, you agree that you are responsible for verifying information and for any decisions made based on its output.
