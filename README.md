# MADDY Cloud AI

A free-hosting-friendly, API-free dashboard for launching your own official ChatGPT, Claude, Gemini accounts — and a configurable "Own AI" entry you can point to a self-hosted or third-party LLM endpoint (for example: a local instance of a 3rd-party model like "gpt-astro-6").

## What it does
- One responsive dashboard for official provider links.
- Prompt drafting and copying before opening the selected provider.
- Local prompt history saved in this browser using `localStorage`.
- Local activity meter counts prompts launched from the dashboard.
- No API keys, no backend, and no API billing.

## Extra: Own AI
This release adds an "Own AI" column you can configure from the dashboard. "Own AI" is a user-configured provider URL and label. It does not ship with any hosted LLM — you must provide the endpoint (for example, a local server or a public instance) that accepts web access from your browser. The UI ships with a default model name set to "gpt-astro-6" as an example, but that model endpoint is not provided by this repo.

Important: This project does not host or provide free access to third-party LLMs. If you want to run a model named "gpt-astro-6" you must host it yourself (on a machine you control, a cloud instance, or a third-party host that publishes an HTTP endpoint). The dashboard simply opens the configured URL in a new tab so you can paste your prompt there.

### Self-hosting hints for community LLMs
- Many open-source LLMs can be run locally or on cloud VMs — tools like Ollama, Hugging Face Inference Endpoints, or a simple HTTP wrapper around a model server can expose a web UI.
- If you host locally (http://localhost:PORT), set the Own AI URL to that address; you can also use a reverse proxy (Caddy, NGINX) or a tunneling service (ngrok) for remote access.
- Always secure any public endpoint you create and be mindful of resource/cost limits — large LLMs require significant RAM/GPUs.

## Deploy
You can host this app as a static site on Vercel (recommended in the original README) or GitHub Pages. No build step or server is required — just serve `index.html`.

To host on GitHub Pages (using the repository root):
1. Push these files to the repository `maddy-cloud-ai`.
2. In the repository Settings → Pages, select the branch `main` and root (/) as the source and save.
3. After a few minutes your site will be available at `https://<your-username>.github.io/maddy-cloud-ai`.

To host on Vercel follow the original README instructions.

## Files
- index.html — the single static app
- vercel.json — suggested Vercel settings

## License
You can add a license file if you want to publish this project under a particular license.
