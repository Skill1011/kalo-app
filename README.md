# Kalo Kalorientracker

Kalo ist eine Web-App zum Kalorienzählen. Sie läuft in jedem Browser, am Handy und am PC, und lässt sich wie eine normale App auf den Home-Bildschirm legen. Sie funktioniert auch offline.

**Funktionen:** persönliches Kalorienziel (Mifflin-St-Jeor), Makros, über 60 Lebensmittel mit Foto, eigene Gerichte mit Foto, Favoriten, Training, Schritte, Wasser, Gewichtsverlauf, Wochenstatistik, BMI, Backup als Datei.

**Daten:** Alles wird nur im Browser des jeweiligen Geräts gespeichert (`localStorage`). Es gibt keinen Server und kein Konto. Über *Einstellungen → Backup* lassen sich die Daten als Datei sichern und auf ein anderes Gerät übertragen.

## Lokal testen

Dafür muss [Node.js](https://nodejs.org) installiert sein. Im Ordner `Kalo` ausführen:

```
node server.js
```

Dann im Browser http://localhost:5173 öffnen.

Du kannst `index.html` auch einfach doppelt anklicken. Dann funktionieren aber Offline-Modus und Installation nicht.

## Veröffentlichen (kostenlos)

Die App besteht nur aus statischen Dateien. Jeder Hoster für statische Webseiten funktioniert.

**Netlify Drop (am einfachsten, ohne Programmierkenntnisse)**
1. https://app.netlify.com/drop öffnen und kostenlos anmelden.
2. Den ganzen Ordner `Kalo` in das Fenster ziehen.
3. Netlify gibt dir eine Adresse wie `https://kalo-xyz.netlify.app`. Diesen Link kannst du teilen. Den Namen kannst du in den Site-Einstellungen ändern.

**GitHub Pages**
1. Neues Repository auf GitHub anlegen und alle Dateien aus `Kalo` hochladen.
2. *Settings → Pages → Branch: main / root* wählen.
3. Die App läuft dann unter `https://<dein-name>.github.io/<repo>/`.

**Vercel:** Auf https://vercel.com ein neues Projekt anlegen und den Ordner hochladen, ohne Framework-Einstellung.

## Auf dem Handy installieren

- **iPhone (Safari):** Teilen-Symbol → „Zum Home-Bildschirm“
- **Android (Chrome):** Menü ⋮ → „App installieren“ oder „Zum Startbildschirm hinzufügen“

## Updates

Nach Änderungen an `index.html` oder `icons/` in `sw.js` die Zeile `const CACHE = 'kalo-v2'` hochzählen, zum Beispiel auf `kalo-v3`. Dann laden installierte Apps die neuen Dateien.

## Bildnachweis

Die Fotos stammen von [Unsplash](https://unsplash.com), stehen unter der Unsplash-Lizenz (frei nutzbar, auch kommerziell, ohne Namensnennung) und werden direkt vom Unsplash-Bildserver geladen.
