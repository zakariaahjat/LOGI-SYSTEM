# 📦 Gestion Logitech — Stock & Ventes

Système de gestion Logitech : consolidation automatique de plusieurs fichiers Excel (stock, ventes mensuelles, prix, fournisseur) en **un fichier maître** structuré.

👉 **Ouvrir le site : https://comparateur-ventes.vercel.app/**

## Table maître générée (colonnes exactes)

| Colonne | Source |
|---|---|
| Code | SKU / référence (détectée auto) |
| EAN | Code-barres (texte, zéros préservés) |
| Nom | Désignation produit |
| Mon Stock | Stock actuel |
| Quantité Mois 1/2/3 | Ventes des 3 derniers mois (fichiers Mois_XX) |
| Moyenne des Mois | **Formule Excel `=(E+F+G)/3`** |
| Prix de Vente / Prix d'Achat | Prix distincts, jamais fusionnés |
| Quantité Fournisseur | Quantité fournisseur |

## Fonctions

- Détection automatique des colonnes **français/anglais** (qt, quantité, stock, prix vente/achat, fournisseur…)
- Fusion par **EAN / Code / SKU** — un produit = une ligne
- Produits d'un seul fichier conservés · cellules inconnues vides (jamais inventées)
- **Conflits** (valeurs contradictoires) : marqués en orange + feuille `Conflits`
- Feuille `Mapping` : traçabilité colonne fichier → colonne maître
- Filtres Excel + autofilter + largeurs auto

## Fichiers

- `index.html` — système v2 (Gestion Stock & Ventes)
- `ancien.html` — l'ancien comparateur simple (3 mois)
- `xlsx.full.min.js` — bibliothèque SheetJS (lecture/écriture Excel)

## Local

Ouvrir `index.html` (double-clic) — fonctionnel hors ligne.
