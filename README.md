# Logging library – Winston

Tässä tehtävässä toteutetaan lokitus Node.js-sovellukseen käyttäen Winston-kirjastoa (v3.11.0). Sovellus kirjoittaa lokiviestejä konsoliin ja tiedostoihin eri tasoilla (info, warn, error).

## Vaatimukset
- Node.js 18+
- Winston 3.11.0

## Asennus ja käynnistys
1. Kloonaa repo: `git clone <url>`
2. `npm install`
3. `mkdir -p logs` (jos ei automaattisesti)
4. `node src/main.js`

## Projektin rakenne
.
├── .gitignore
├── package.json
├── package-lock.json
├── README.md
└── src
    ├── logger.js
    └── main.js


- **logger.js**: Winston-konfig (JSON + timestamp, console + error.log + combined.log).
- **main.js**: Testaa log-tasot (`log()` ja shortcutit).

## Lokit
- Konsoli: Kaikki viestit.
- `logs/error.log`: Vain error-tasot.
- `logs/combined.log`: Kaikki.

Esimerkki:
{"level":"info","message":"This is an informational message.","timestamp":"2026-03-03T12:39:29.121Z"}
{"level":"error","message":"This is an error message.","timestamp":"2026-03-03T12:39:29.123Z"}

## Huomioita
- `.gitignore` estää node_modules/ ja logs/ -kansiot gitissä.
- Testattu Node 18+, toimii ulkoisessa ympäristössä.