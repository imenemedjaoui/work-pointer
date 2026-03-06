# 🗓️ Work Pointer

> Application web de pointage de présence — légère, locale et sans dépendance.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![ExcelJS](https://img.shields.io/badge/ExcelJS-217346?style=flat-square&logo=microsoftexcel&logoColor=white)
![No backend](https://img.shields.io/badge/backend-aucun-22c55e?style=flat-square)

<a href="https://imenemedjaoui.github.io/work-pointer/" target="_blank"><img src="https://img.shields.io/badge/🚀_Essayer_en_ligne-imenemedjaoui.github.io-3b82f6?style=for-the-badge" alt="Essayer en ligne" /></a>

---

## 📌 Présentation

**Work Pointer** est une application single-file permettant d'enregistrer sa présence quotidienne. Les données sont persistées localement dans un fichier `pointage.json` via la **File System Access API** — aucun serveur, aucun backend, aucune installation requise.

---

## ✨ Fonctionnalités

| # | Fonctionnalité | Détail |
|---|---|---|
| 🔵 | **Pointage unique par jour** | Un seul enregistrement autorisé par journée |
| 📅 | **Calendrier mensuel interactif** | Navigation mois par mois avec les flèches ‹ › |
| 💾 | **Persistance JSON locale** | Écriture directe dans `pointage.json` sur le disque |
| 🔄 | **Fallback localStorage** | Sauvegarde automatique dans le navigateur si aucun fichier n'est lié |
| 📊 | **Export XLSX** | Génération d'un fichier Excel stylisé (thème sombre) directement depuis le navigateur |
| 💰 | **Calcul du revenu estimé** | Saisie du taux journalier (TJ) avec choix de devise parmi 33 monnaies — total calculé instantanément |
| 📱 | **Design responsive** | Interface adaptée mobile et grands écrans |
| 🌑 | **Thème sombre** | Dark mode intégré, aucune configuration requise |

---

## 🚀 Démarrage

Aucune installation nécessaire. Ouvrir directement dans un navigateur :

```bash
# Cloner le dépôt
git clone https://github.com/imenemedjaoui/work-pointer.git

# Ouvrir l'application
open index.html
```

> ⚠️ La sauvegarde JSON via **File System Access API** est supportée sur **Chrome** et **Edge** uniquement.
> Sur Firefox, les données sont automatiquement conservées dans le **localStorage**.

---

## 📖 Guide d'utilisation

**1. Lier un fichier de données 📂**

Cliquer sur **"Lier pointage.json"** pour sélectionner ou créer le fichier de sauvegarde sur le disque. L'indicateur passe au 🟢 une fois le fichier lié. Cette étape n'est requise qu'une seule fois — le lien est mémorisé entre les sessions.

**2. Pointer sa présence 🔵**

Cliquer sur le bouton **POINTER**. Il bascule sur **POINTÉ** pour la journée en cours et ne peut plus être activé jusqu'au lendemain.

**3. Consulter l'historique 📅**

Naviguer dans le calendrier via les flèches. Les jours pointés sont mis en évidence en bleu, le jour courant est encadré.

**4. Exporter en XLSX 📊**

Cliquer sur **"Exporter XLSX"** pour télécharger un fichier Excel `pointage.xlsx`. Le fichier reprend le thème sombre de l'application — fond noir, cellules bleues pour les jours pointés — et liste chaque jour avec sa date, son nom, son mois et son numéro de semaine.

**5. Estimer son revenu 💰**

Saisir un **taux journalier (TJ)** dans le champ dédié et sélectionner une devise parmi 33 disponibles (EUR, USD, GBP, CHF, MAD, TND, DZD, AED, JPY...). Le total est recalculé instantanément à chaque frappe sur la base des jours pointés.

---

## 📁 Structure du projet

```
work-pointer/
├── index.html        # Application complète (HTML + CSS + JS vanilla)
└── pointage.json     # Fichier de données généré à la première utilisation
```

---

## 🗂️ Format des données

```json
{
  "jours": [
    "2026-01-26",
    "2026-01-27",
    "2026-02-03"
  ],
  "mis_a_jour": "2026-03-06T10:42:00.000Z"
}
```

Les dates sont stockées au format **ISO 8601** (`YYYY-MM-DD`) et triées chronologiquement.

---

## 🛠️ Stack technique

| Technologie | Rôle |
|---|---|
| HTML5 / CSS3 / JS Vanilla | Interface et logique applicative |
| [File System Access API](https://developer.mozilla.org/en-US/docs/Web/API/File_System_Access_API) | Lecture et écriture du fichier JSON local |
| IndexedDB | Persistance du handle de fichier entre les sessions |
| localStorage | Fallback de sauvegarde |
| [ExcelJS](https://github.com/exceljs/exceljs) | Génération du fichier XLSX stylisé côté client |

---

## 👩‍💻 Auteure

**Imène MEDJAOUI** 🫧

---

## 📄 Licence

Ce projet est distribué sous licence **MIT**. Vous êtes libre de l'utiliser, le modifier et le redistribuer.
