# Starý Jičín – Komunitní aplikace

Bezplatná PWA aplikace pro obec Starý Jičín.

---

## Soubory v tomto balíčku

- `index.html` – hlavní aplikace
- `manifest.json` – nastavení PWA
- `sw.js` – offline podpora
- `ikona.png` – znak obce **(tento soubor musíte přidat sami!)**

---

## Krok 1 – Připravte Google Sheets tabulku

1. Otevřete svou tabulku na **sheets.google.com**
2. Ujistěte se, že má záhlaví: `Nadpis | Popis | Datum | Obec | Kategorie | Předseda`
3. Klikněte na **Sdílet** → nastavte "Kdokoli s odkazem může zobrazit"
4. Zkopírujte ID tabulky z URL adresy:
   - URL vypadá takto: `https://docs.google.com/spreadsheets/d/**TOTO_JE_ID**/edit`
   - Zkopírujte část mezi `/d/` a `/edit`

---

## Krok 2 – Vložte ID do aplikace

1. Otevřete soubor `index.html` v textovém editoru (Poznámkový blok)
2. Najděte řádek: `const SHEET_ID = 'ZDE_VLOZTE_ID_TABULKY';`
3. Nahraďte `ZDE_VLOZTE_ID_TABULKY` skutečným ID vaší tabulky
4. Uložte soubor

---

## Krok 3 – Přidejte znak obce

1. Přejmenujte soubor se znakem obce na `ikona.png`
2. Vložte ho do stejné složky jako `index.html`

---

## Krok 4 – Zveřejněte aplikaci na GitHub Pages (zdarma)

1. Vytvořte účet na **github.com** (zdarma)
2. Klikněte na **"New repository"**
3. Pojmenujte ho: `stary-jicin-app`
4. Nahrajte všechny soubory (index.html, manifest.json, sw.js, ikona.png)
5. Jděte do **Settings → Pages → Source: main branch**
6. Za chvíli bude aplikace dostupná na adrese:
   `https://vase-uzivatelske-jmeno.github.io/stary-jicin-app`

---

## Jak obyvatelé nainstalují aplikaci

**Android (Chrome):** Menu ⋮ → "Přidat na plochu"  
**iPhone (Safari):** Tlačítko sdílení □↑ → "Přidat na plochu"

---

## Jak předsedové zadávají oznámení

Předsedové zadávají oznámení přímo do Google Sheets tabulky.
Změny se v aplikaci zobrazí automaticky (při každém otevření aplikace).

Doporučený formát data: `RRRR-MM-DD` (např. `2026-06-14`)
