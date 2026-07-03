# Zeljko Tripcevski — Portfolio Site

Statički sajt (samo HTML/CSS, bez build koraka). Sadržaj:

```
portfolio_site/
├── index.html
├── style.css
├── .nojekyll
└── img/
    ├── zvol-truenas.jpg
    ├── ollama-webui-apps.jpg
    ├── openwebui-chat.jpg
    ├── winbox-devices.jpg
    ├── lora-nodes.jpg
    ├── rooftop-antenna.jpg
    └── meshcore-map.jpg
```

## Deploy na GitHub Pages — korak po korak

### 1. Napravi novi repozitorijum na GitHub-u
- Idi na github.com → **New repository**
- Ime npr. `portfolio` (ili `zeljko-tripcevski.github.io` ako želiš da sajt bude na `https://<username>.github.io` bez dodatnog path-a)
- Public, bez README-a (imamo već fajlove)

### 2. Otpremi fajlove
Najlakše preko browsera:
- Otvori repo → **Add file → Upload files**
- Prevuci **sadržaj** `portfolio_site` foldera (index.html, style.css, .nojekyll, img/) — ne sam folder, nego fajlove unutra, tako da `index.html` bude u root-u repoa
- Commit

Ili preko terminala, ako imaš git instaliran:
```bash
cd portfolio_site
git init
git add .
git commit -m "Initial portfolio site"
git branch -M main
git remote add origin https://github.com/<username>/<repo>.git
git push -u origin main
```

### 3. Uključi GitHub Pages
- U repou: **Settings → Pages**
- Pod "Build and deployment" → Source: **Deploy from a branch**
- Branch: **main**, folder: **/ (root)**
- Save

### 4. Sačekaj 1–2 minuta
GitHub će ti dati link, obično:
```
https://<username>.github.io/<repo>/
```
(ili `https://<username>.github.io/` ako je repo nazvan `<username>.github.io`)

## Napomena o fontovima
Sajt učitava Google Fonts (JetBrains Mono, IBM Plex Sans) preko CDN-a — radiće normalno na pravom hostingu jer browser korisnika ima internet, čak i ako lokalni pregled bez mreže padne na fallback font.

## Ažuriranje sadržaja kasnije
Sav tekst je direktno u `index.html` (nema CMS-a) — otvoriš fajl, izmeniš, commit + push, GitHub Pages se sam ažurira za par sekundi do minut.
