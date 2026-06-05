# Content Kommissar — Website

Statische Onepage-Website für [content-kommissar.de](https://content-kommissar.de).  
Kein Framework, kein Build-Schritt — einfach öffnen und deployen.

## Dateien

```
index.html   – Komplette Website (eine Seite)
styles.css   – Alle Styles (Dark Theme, responsive)
script.js    – Minimales JS (Nav, Accordion, Scroll-Animationen)
README.md    – Diese Datei
```

---

## 1. Lokal öffnen

Einfach `index.html` im Browser öffnen:

```bash
# Option A: Doppelklick auf index.html im Finder
# Option B: Im Terminal mit dem Live-Server von VS Code (empfohlen)
cd "Website Content Commisar"
# Dann in VS Code: Rechtsklick auf index.html → "Open with Live Server"
```

Oder direkt mit Python:

```bash
python3 -m http.server 8080
# → http://localhost:8080
```

---

## 2. Auf GitHub hochladen

```bash
# Neues Repository anlegen (z. B. auf github.com/[dein-name]/content-kommissar)
git init
git add index.html styles.css script.js README.md
git commit -m "Initial release: Content Kommissar website"
git remote add origin https://github.com/[dein-name]/content-kommissar.git
git push -u origin main
```

---

## 3. Auf Vercel deployen

**Option A – Per GitHub (empfohlen):**

1. Gehe zu [vercel.com](https://vercel.com) und melde dich an
2. Klicke auf „Add New Project"
3. Wähle dein GitHub-Repository aus
4. Framework: **Other** (kein Build-Schritt nötig)
5. Klicke auf „Deploy" — fertig

Jedes neue `git push` auf `main` löst automatisch ein Re-Deploy aus.

**Option B – Per Vercel CLI:**

```bash
npm i -g vercel
vercel
# Fragen mit Enter bestätigen
```

---

## 4. Domain content-kommissar.de verbinden

### In Vercel:
1. Gehe im Vercel-Dashboard zu deinem Projekt → **Settings → Domains**
2. Trage ein: `content-kommissar.de` und `www.content-kommissar.de`
3. Vercel zeigt dir DNS-Einträge an (A-Record oder CNAME)

### Beim Domain-Registrar (z. B. INWX, Strato, Namecheap):
- **A-Record:** `@` → IP-Adresse von Vercel (z. B. `76.76.21.21`)
- **CNAME:** `www` → `cname.vercel-dns.com`

DNS-Änderungen können bis zu 24 Stunden dauern. Vercel stellt automatisch ein kostenloses SSL-Zertifikat aus.

---

## Anpassungen

| Was                   | Wo                              |
|-----------------------|---------------------------------|
| E-Mail-Adresse        | `index.html` – alle `mailto:`-Links |
| Preise                | `index.html` – Section `#angebote`  |
| Farben                | `styles.css` – `:root` Variablen    |
| Impressum/Datenschutz | Eigene Seiten `impressum.html` und `datenschutz.html` anlegen |

---

## Kontakt

**content-kommissar.de** — kontakt@content-kommissar.de
