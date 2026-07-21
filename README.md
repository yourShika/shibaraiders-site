# Shibaraiders «SHIBA» — FC-Website

Statische Website der Freien Gesellschaft **Shibaraiders** (Alpha [Light]) — gehostet über GitHub Pages, mit automatisch aktualisierter Mitgliederliste vom Lodestone.

## Auf GitHub veröffentlichen

1. Neues Repository anlegen (z. B. `shibaraiders-site`).
2. **Alle Dateien dieses Ordners** ins Repository pushen (inkl. des versteckten Ordners `.github/`!).
3. Im Repo: **Settings → Pages → Source: "Deploy from a branch"**, Branch `main`, Ordner `/ (root)` wählen.
4. Nach ca. 1 Minute ist die Seite unter `https://<dein-name>.github.io/shibaraiders-site/` erreichbar.

## Automatische Mitgliederliste

- Die Seite lädt beim Öffnen `members.json` und zeigt alle Mitglieder mit Rang, Level und Lodestone-Avatar (Fallback).
- Die GitHub Action `.github/workflows/update-members.yml` ruft **täglich um 03:17 UTC** die Mitgliederliste vom Lodestone ab und committet Änderungen in `members.json`. Neue Mitglieder erscheinen also automatisch.
- Manuell aktualisieren: Tab **Actions → "Mitgliederliste vom Lodestone aktualisieren" → Run workflow**.
- Falls die Action beim allerersten Mal nicht läuft: **Settings → Actions → General → Workflow permissions → "Read and write permissions"** aktivieren.

## Ränge

Die Rangbeschreibungen (Kaiser Shiba = Owner, Shogun, NekoPaw, Mascot, Gokiburi) sind in `index.html` hinterlegt — unbekannte neue Ränge werden als „Mitglied" angezeigt.

## Bilder

- `assets/crest.png` — FC-Logo
- `assets/akeno.png` — Portrait des Owners (wird statt des Lodestone-Avatars angezeigt)
- Weitere Portraits: einfach `LOCAL_AVATARS` in `index.html` erweitern (`'<Lodestone-Charakter-ID>': 'assets/datei.png'`).

## Rechtliches

Inoffizielle Community-Seite. FINAL FANTASY XIV © SQUARE ENIX CO., LTD. Diese Seite steht in keiner Verbindung zu Square Enix.
