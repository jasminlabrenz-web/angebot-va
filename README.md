# Dein Angebot in 60 Minuten System – Bot

## Dateien

```
index.html                  → Die Bot-Seite
netlify/functions/chat.js   → Serverless Function (API-Key bleibt sicher)
netlify.toml                → Netlify Konfiguration
```

## Deployment auf Netlify

### 1. GitHub Repo erstellen
- Neues Repo anlegen z.B. `angebot-bot`
- Alle 3 Dateien hochladen (Struktur beibehalten!)

### 2. Netlify verbinden
- netlify.com → "Add new site" → "Import from Git"
- GitHub Repo auswählen
- Build-Einstellungen leer lassen (kein Build nötig)
- Deploy

### 3. API-Key als Environment Variable eintragen
- Netlify Dashboard → Site → Site configuration → Environment variables
- Neue Variable anlegen:
  - Key: `ANTHROPIC_API_KEY`
  - Value: dein Anthropic API-Key (sk-ant-...)
- Speichern + Site neu deployen (Deploys → Trigger deploy)

### 4. Custom Domain (optional)
- Netlify → Domain management → Add custom domain
- z.B. `angebot.jasminlabrenz.com`
- CNAME bei All-Inkl: `angebot` → deine-netlify-url.netlify.app

## Fertig!
Deine Userinnen öffnen die Seite und der Bot startet sofort.
Kein Login, kein API-Key-Eingabe, nichts.
