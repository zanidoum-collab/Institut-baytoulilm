# Institut-baytoulilm

## Formulaire d'inscription

La page `Inscription` utilise maintenant un formulaire integre au site.

- Le dossier DOCX est genere dans le navigateur depuis `travail/teamplate_inscription.docx`.
- La template actuelle prevoit 5 enfants maximum.
- Les enfants sont envoyes avec une ligne Google Sheet par enfant.
- Le script Google Apps Script a copier cote Google est dans `travail/google-apps-script-inscriptions.js`.

### Activer Google Sheet

1. Creer un Google Sheet pour les inscriptions.
2. Ouvrir `Extensions > Apps Script`.
3. Coller le contenu de `travail/google-apps-script-inscriptions.js`.
4. Remplacer `REMPLACER_PAR_ID_DU_GOOGLE_SHEET` par l'ID du Google Sheet.
5. Deployer le script en `Web app`, accessible a `Tout le monde`.
6. Copier l'URL du Web App.
7. Dans `index.html`, renseigner cette URL dans `INSCRIPTION_CONFIG.appsScriptUrl`.

Sans cette URL, le site genere le DOCX mais n'envoie pas encore les donnees dans Google Sheet.
