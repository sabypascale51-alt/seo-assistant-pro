# 📊 Templates Google Sheets pour SEO Assistant Pro

Ce document contient des **templates prêts à l'emploi** pour organiser vos données SEO dans Google Sheets.

---

## 🎯 Template 1 : Tableau Principal de Mots-Clés

### Structure des colonnes

```
A: Mot-Clé | B: Volume | C: Difficulté | D: Intention | E: Type Traîne | F: Priorité | G: Statut | H: URL Cible | I: Date Ajout | J: Notes
```

### Exemple de données

| Mot-Clé | Volume | Difficulté | Intention | Type Traîne | Priorité | Statut | URL Cible | Date Ajout | Notes |
|---------|--------|------------|-----------|-------------|----------|--------|-----------|------------|-------|
| chaussures running femme | 5400 | 68 | Commercial | Moyenne | P1 | En cours | /chaussures-running-femme | 2026-02-02 | Créer page catégorie |
| comment choisir running | 880 | 24 | Informationnel | Longue | P1 | À faire | /blog/choisir-running | 2026-02-02 | Article prioritaire |
| chaussures trail 2026 | 720 | 42 | Commercial | Longue | P2 | À faire | /chaussures-trail | 2026-02-02 | |
| meilleures running femme | 1200 | 55 | Commercial | Moyenne | P1 | Terminé | /guide/meilleures-running | 2026-02-01 | Top 10 publié |

### Formules utiles à ajouter

**Colonne K : Score de Priorité** (calculé)
```
=IF(C2<30, IF(B2>1000, "⭐⭐⭐ EXCELLENT", "⭐⭐ BON"), IF(C2<60, "⭐ MOYEN", "❌ DIFFICILE"))
```

**Colonne L : Statut Visuel**
```
=IF(G2="Terminé", "✅", IF(G2="En cours", "🔄", "⏳"))
```

---

## 📅 Template 2 : Calendrier Éditorial

### Structure des colonnes

```
A: Date Publication | B: Titre Article | C: Mot-Clé Principal | D: Mots-Clés Secondaires | E: Type Contenu | F: Rédacteur | G: Statut | H: URL Finale | I: Performances
```

### Exemple de données

| Date Publication | Titre Article | Mot-Clé Principal | Mots-Clés Secondaires | Type | Rédacteur | Statut | URL | Performances |
|-----------------|---------------|-------------------|----------------------|------|-----------|--------|-----|--------------|
| 2026-02-05 | Guide Complet Running Femme 2026 | chaussures running femme | running, chaussures sport | Guide | Marie | En rédaction | /blog/guide-running-femme-2026 | - |
| 2026-02-08 | Top 10 Meilleures Running Trail | chaussures trail 2026 | trail, montagne, outdoor | Top 10 | Pierre | Planifié | /blog/top-10-trail-2026 | - |
| 2026-02-01 | Comment Choisir ses Running ? | comment choisir running | conseil, débutant, foulée | Tutoriel | Marie | Publié | /blog/choisir-running | 245 vues |

### Mise en forme conditionnelle

**Statut :**
- 🟢 "Publié" → Vert
- 🟡 "En rédaction" → Jaune
- 🔵 "Planifié" → Bleu
- 🔴 "En retard" → Rouge (si date < aujourd'hui et statut ≠ publié)

---

## 📈 Template 3 : Suivi des Positions Google

### Structure des colonnes

```
A: Mot-Clé | B: URL | C: Position Actuelle | D: Position -7j | E: Position -30j | F: Évolution | G: Impressions | H: Clics | I: CTR | J: Dernière MAJ
```

### Exemple de données

| Mot-Clé | URL | Position Actuelle | Position -7j | Position -30j | Évolution | Impressions | Clics | CTR | Dernière MAJ |
|---------|-----|-------------------|--------------|---------------|-----------|-------------|-------|-----|--------------|
| chaussures running femme | /chaussures-running-femme | 12 | 15 | 23 | ⬆️ +11 | 3.2K | 85 | 2.66% | 2026-02-02 |
| comment choisir running | /blog/choisir-running | 4 | 6 | 8 | ⬆️ +4 | 1.8K | 245 | 13.6% | 2026-02-02 |
| chaussures trail | /chaussures-trail | 18 | 16 | 15 | ⬇️ -3 | 950 | 22 | 2.3% | 2026-02-02 |

### Formules utiles

**Colonne F : Évolution automatique**
```
=IF(C2<D2, "⬆️ +"&(D2-C2), IF(C2>D2, "⬇️ -"&(C2-D2), "➡️ ="))
```

**Colonne I : CTR calculé**
```
=IF(G2>0, TEXT(H2/G2, "0.00%"), "N/A")
```

---

## 🔍 Template 4 : Analyse Concurrentielle

### Structure des colonnes

```
A: Concurrent | B: URL | C: Autorité Domaine (DA) | D: Mots-Clés Communs | E: Leurs Mots-Clés Uniques | F: Opportunités | G: Points Forts | H: Points Faibles
```

### Exemple de données

| Concurrent | URL | DA | Mots-Clés Communs | Mots-Clés Uniques | Opportunités | Points Forts | Points Faibles |
|-----------|-----|----|--------------------|-------------------|--------------|--------------|----------------|
| RunnerShop | runershop.com | 65 | 45 | chaussures marathon, chaussures compétition | Créer contenu "marathon" et "compétition" | Blog actif, gros backlinks | Site lent, peu de vidéos |
| SportPlus | sportplus.fr | 58 | 32 | chaussures crossfit, fitness | Cibler "crossfit running" | Large gamme produits | Navigation confuse, SEO faible |

---

## 🎨 Template 5 : Plan de Contenu Thématique

### Structure des colonnes

```
A: Thématique | B: Mot-Clé Pilier | C: Volume | D: Articles Support | E: Progression | F: Liens Internes | G: Performance Globale
```

### Exemple de données

| Thématique | Mot-Clé Pilier | Volume | Articles Support | Progression | Liens Internes | Performance |
|-----------|----------------|--------|-----------------|-------------|----------------|-------------|
| Chaussures Running | chaussures running | 22K | 1. Comment choisir<br>2. Top 10 femme<br>3. Top 10 homme<br>4. Entretien | 75% (3/4) | 12 liens créés | 1.2K visites/mois |
| Trail & Outdoor | chaussures trail | 8.5K | 1. Guide trail débutant<br>2. Comparatif 2026<br>3. Entretien trail | 33% (1/3) | 4 liens créés | 320 visites/mois |

---

## 📊 Graphiques Recommandés

### Graphique 1 : Évolution des Positions
- **Type :** Courbe
- **Axe X :** Dates
- **Axe Y :** Positions (inversé, 1 en haut)
- **Données :** Vos 10 mots-clés prioritaires

### Graphique 2 : Répartition par Intention
- **Type :** Camembert
- **Données :** Nombre de mots-clés par intention (Informationnel, Commercial, etc.)

### Graphique 3 : Volume vs Difficulté
- **Type :** Nuage de points
- **Axe X :** Difficulté
- **Axe Y :** Volume
- **Données :** Tous vos mots-clés

---

## 🔢 Formules Avancées

### 1. Calcul du Score de Priorité

```
=IF(AND(Volume>1000, Difficulté<40), "🏆 TOP PRIORITÉ", 
  IF(AND(Volume>500, Difficulté<60), "⭐ PRIORITÉ", 
  IF(Difficulté<30, "💎 QUICK WIN", "⏳ Long terme")))
```

### 2. Statut avec Alerte

```
=IF(Statut="À faire", IF(DateAjout<TODAY()-30, "🔴 EN RETARD", "⏳ Planifié"), 
  IF(Statut="En cours", "🟡 En cours", "✅ OK"))
```

### 3. ROI Estimé

```
=(Volume * CTR_Moyen * Taux_Conversion * Valeur_Conversion) / Coût_Production_Contenu
```

**Exemple avec valeurs :**
```
=(5400 * 0.05 * 0.02 * 50) / 200 = 1.35 → ROI de 135%
```

---

## 🎯 Mise en Forme Conditionnelle

### Règle 1 : Priorités
- **P1** → Fond rouge clair
- **P2** → Fond orange clair
- **P3** → Fond bleu clair

### Règle 2 : Difficulté
- **0-30** → Vert (facile)
- **31-60** → Orange (moyen)
- **61-100** → Rouge (difficile)

### Règle 3 : Statut
- **"Terminé"** → Texte vert + gras
- **"En cours"** → Texte orange
- **"À faire"** → Texte gris

---

## 📥 Import depuis SEO Assistant Pro

### Étapes d'import

1. **Dans l'application :**
   - Onglet Tableaux
   - Cliquez "Exporter vers Sheets"
   - Copiez les données

2. **Dans Google Sheets :**
   - Créez une nouvelle feuille
   - Collez en A1
   - Les données s'organisent automatiquement

3. **Personnalisation :**
   - Ajoutez les colonnes supplémentaires (URL Cible, Notes, etc.)
   - Appliquez la mise en forme conditionnelle
   - Créez vos graphiques

---

## 🔄 Synchronisation Régulière

### Workflow recommandé

**Quotidien :**
- Mise à jour des positions (via Search Console)
- Ajout de nouveaux mots-clés trouvés

**Hebdomadaire :**
- Export complet depuis l'app
- Mise à jour du calendrier éditorial
- Analyse des performances

**Mensuel :**
- Révision complète de la stratégie
- Nettoyage des données obsolètes
- Ajustement des priorités

---

## 💡 Astuces Pro Google Sheets

### 1. Créer des Vues Filtrées

**Menu Données > Créer un filtre > Vues filtrées**

Créez ces vues :
- 🔴 "Quick Wins" → Difficulté < 30
- ⭐ "Haute Priorité" → Priorité = P1
- ✅ "Publiés" → Statut = Terminé
- ⏳ "En Attente" → Statut = À faire

### 2. Protection des Formules

**Clic droit > Protéger la plage**
- Protégez les colonnes avec formules
- Permet de partager sans risque de casse

### 3. Notifications Automatiques

**Extensions > Apps Script**
```javascript
// Alerte si nouvelle position > 20
function checkPositions() {
  var sheet = SpreadsheetApp.getActiveSheet();
  var data = sheet.getDataRange().getValues();
  
  for (var i = 1; i < data.length; i++) {
    if (data[i][2] > 20) { // Colonne C = Position
      MailApp.sendEmail({
        to: "votre@email.com",
        subject: "Alerte SEO : Position faible",
        body: "Le mot-clé '" + data[i][0] + "' est en position " + data[i][2]
      });
    }
  }
}
```

---

## 🎓 Tutoriel Vidéo (Étapes Texte)

### Créer votre premier tableau en 5 minutes

**Minute 1 : Création**
- Ouvrez Google Sheets
- Créez une nouvelle feuille
- Nommez-la "Mots-Clés SEO"

**Minute 2 : Structure**
- Ajoutez les en-têtes de colonne (A-J)
- Appliquez un style (gras, fond coloré)
- Figez la première ligne

**Minute 3 : Import**
- Exportez depuis SEO Assistant Pro
- Collez dans A2
- Vérifiez l'alignement

**Minute 4 : Formules**
- Ajoutez la colonne "Score"
- Ajoutez la colonne "Statut Visuel"
- Copiez les formules vers le bas

**Minute 5 : Visualisation**
- Créez un graphique des positions
- Appliquez la mise en forme conditionnelle
- Sauvegardez et partagez

---

## ✅ Checklist Setup Complet

- [ ] Template Mots-Clés créé et importé
- [ ] Calendrier Éditorial configuré
- [ ] Suivi Positions mis en place
- [ ] Analyse Concurrents démarrée
- [ ] Formules installées et testées
- [ ] Mise en forme conditionnelle appliquée
- [ ] 2-3 graphiques créés
- [ ] Vues filtrées configurées
- [ ] Partage avec l'équipe effectué
- [ ] Processus de mise à jour défini

---

## 🔗 Ressources Complémentaires

- [Fonctions Google Sheets](https://support.google.com/docs/table/25273)
- [Apps Script Documentation](https://developers.google.com/apps-script)
- [SEO Reporting avec Sheets](https://www.searchenginejournal.com/google-sheets-seo/)

---

**Vous êtes prêt !** Vos tableaux Google Sheets sont maintenant parfaitement configurés pour travailler avec SEO Assistant Pro. 📊✨