# Pack & Shop – Neues GitHub-Repository einrichten

## ⚠️ WICHTIG ZUERST: Deine 2 Supabase-Schlüssel eintragen
Diese Datei hat noch PLATZHALTER. Ohne deine Schlüssel funktioniert das Teilen (Sync) nicht.

1. Öffne `index.html` in einem Texteditor.
2. Suche (Strg+F) nach: `HIER_PROJECT_URL`
3. Du findest diese zwei Zeilen:

   const SUPABASE_URL      = "HIER_PROJECT_URL_EINFUEGEN";
   const SUPABASE_ANON_KEY = "HIER_ANON_PUBLIC_KEY_EINFUEGEN";

4. Ersetze NUR den Text zwischen den Anführungszeichen "" durch deine echten Werte
   (aus Supabase → Project Settings → API):
   - Project URL  → erste Zeile  (beginnt mit https://, endet auf .supabase.co, KEIN / am Ende)
   - Publishable / anon Key → zweite Zeile
5. Speichern.

Beispiel danach:
   const SUPABASE_URL      = "https://deinprojekt.supabase.co";
   const SUPABASE_ANON_KEY = "sb_publishable_xxxxxxxxxxxxx";

(Die Supabase-Datenbank-Tabelle ist schon eingerichtet – das SQL musst du NICHT erneut ausführen,
 solange du dasselbe Supabase-Projekt nutzt.)

## Schritt 1 – Neues Repository erstellen
1. Auf github.com → oben rechts "+" → "New repository".
2. Name z. B. "pack-shop".  Auf "Public" lassen.  → "Create repository".

## Schritt 2 – Dateien hochladen
1. Im neuen Repo: "uploading an existing file" anklicken
   (oder "Add file" → "Upload files").
2. ALLE Dateien aus diesem Ordner zusammen reinziehen:
   - index.html   ← die Hauptdatei (mit deinen eingetragenen Schlüsseln!)
   - manifest.webmanifest
   - sw.js
   - icon-192.png, icon-512.png, icon-512-maskable.png, icon-180.png
   - logo.svg
   - netlify.toml   (schadet nicht, wird von GitHub ignoriert)
3. Unten auf "Commit changes" klicken.

WICHTIG: Es darf nur EINE index.html geben. Keine "index (1).html".

## Schritt 3 – GitHub Pages aktivieren
1. Im Repo → "Settings" → links "Pages".
2. Bei "Branch": "main" auswählen → "Save".
3. Nach 1–2 Minuten erscheint oben: "Your site is live at https://….github.io/pack-shop/"
4. Diese Adresse ist deine App – sie teilst du mit Freunden.

## Schritt 4 – Testen
1. Adresse öffnen.
2. F12 → "Console": Es darf NICHT stehen "Supabase nicht konfiguriert".
   Wenn doch → Schlüssel in index.html nochmal prüfen (Schritt oben).
3. App auf zwei Geräten öffnen → 👥 → "✨ Neuen Code erstellen" → Code teilen → testen.

## Wenn weiter die alte Version erscheint
- Hart neu laden: Strg+F5 (PC) / Tab schließen und neu öffnen (Handy).
- App vom Home-Bildschirm entfernen und neu hinzufügen (löscht den alten Service Worker).
- Inkognito-Fenster öffnen (ignoriert Cache) – zeigt es dort die neue Version, war es nur Cache.
