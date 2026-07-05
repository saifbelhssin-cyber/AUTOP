# 🚗 AUTOP - Plateforme de Demande de Devis

**AUTOP** est une plateforme web moderne et responsive pour la gestion de demandes de devis de pièces automobiles. Elle permet aux clients de soumettre facilement des demandes de devis et aux professionnels de gérer ces demandes via un espace d'administration.

## ✨ Fonctionnalités

### Pour les clients (index.html)
- ✅ **Formulaire intuitif** - Interface simple et épurée
- 📱 **Responsive** - Fonctionne sur tous les appareils
- 🔧 **Gestion de pièces** - Ajouter/supprimer plusieurs pièces
- 📎 **Upload de fichiers** - Joindre images et documents (jusqu'à 10 fichiers, 5MB max)
- 🔍 **Suivi en temps réel** - Numéro de suivi unique généré automatiquement
- 📤 **Partage facile** - Envoyer par Email ou WhatsApp
- 💾 **Données locales** - Stockage sécurisé en localStorage

### Pour les professionnels (admin.html)
- 📊 **Tableau de bord** - Statistiques en temps réel
- 📋 **Liste des demandes** - Toutes les demandes avec détails
- 🔍 **Recherche** - Filtrer par nom, email, téléphone ou n° de suivi
- 👁️ **Visualisation détaillée** - Voir tous les détails d'une demande
- 📥 **Export** - Télécharger les données en JSON
- 🗑️ **Gestion** - Supprimer les demandes individuellement

## 📁 Structure des fichiers

```
AUTOP/
├── index.html          # Page d'accueil et formulaire client
├── admin.html          # Espace professionnel
├── style.css           # Feuille de style (séparé)
├── script.js           # Logique JavaScript (séparé)
├── _config.yml         # Configuration GitHub Pages
└── README.md           # Cette documentation
```

## 🚀 Déploiement sur GitHub Pages

1. **Activer GitHub Pages** dans les paramètres du repository
2. **Sélectionner** la branche `main`
3. **Publier** vers `/root`
4. **Accéder** à : `https://saifbelhssin-cyber.github.io/AUTOP/`

## 📖 Guide d'utilisation

### Pour les clients

1. **Remplir les informations personnelles**
   - Nom complet
   - Email
   - Téléphone

2. **Ajouter les informations du véhicule**
   - Marque (ex: Renault)
   - Modèle (ex: Clio)
   - Année
   - Kilométrage (optionnel)

3. **Ajouter les pièces demandées**
   - Cliquer sur "+ Ajouter une pièce"
   - Remplir : Désignation, Référence OEM, Quantité, Urgence
   - Ajouter autant de pièces que nécessaire

4. **Optionnel : Ajouter des fichiers**
   - Images ou documents justificatifs
   - Maximum 10 fichiers, 5 MB chacun

5. **Soumettre la demande**
   - Cliquer "Envoyer mon devis"
   - Recevoir un numéro de suivi unique (ex: DEM-20260705-001)
   - Partager via Email ou WhatsApp

6. **Suivre sa demande**
   - Utiliser le numéro de suivi en haut de la page
   - Voir l'état d'avancement

### Pour les professionnels

1. **Accéder à l'espace pro**
   - Cliquer sur "Espace Pro" ou accéder directement à `admin.html`

2. **Consulter le tableau de bord**
   - Voir les stats : Total, Aujourd'hui, Cette semaine, Pièces totales

3. **Gérer les demandes**
   - **Rechercher** : Utiliser la barre de recherche
   - **Voir détails** : Cliquer sur le bouton 👁️
   - **Supprimer** : Cliquer sur 🗑️

4. **Exporter les données**
   - Cliquer sur "📥 Exporter"
   - Télécharger un fichier JSON avec toutes les demandes

5. **Réinitialiser les données**
   - Cliquer sur "🗑️ Effacer" pour supprimer toutes les demandes
   - ⚠️ Action irréversible

## 🔒 Sécurité

- ✅ **Données locales** - Aucun envoi vers un serveur externe (localStorage)
- ✅ **Validation côté client** - Vérification des entrées
- ✅ **Limitations** - Max 10 fichiers, 5 MB par fichier
- ⚠️ **Note** : Pour une utilisation professionnelle, configurer un backend secure

## 📱 Responsive Design

L'application est optimisée pour :
- 📱 Mobiles (320px+)
- 📱 Tablettes (768px+)
- 💻 Desktops (1200px+)

## 🎨 Couleurs et branding

- **Couleur principale** : #d32f2f (Rouge AUTOP)
- **Couleur secondaire** : #b71c1c (Rouge foncé)
- **Accent** : Bleu #1976d2

## 🔄 Format des données

### Demande stockée (localStorage)
```json
{
  "trackingNumber": "DEM-20260705-001",
  "nom": "Jean Dupont",
  "email": "jean@example.com",
  "telephone": "+216 98 774 525",
  "marque": "Renault",
  "modele": "Clio",
  "annee": "2020",
  "kilometrage": "50000",
  "message": "Urgence réparation",
  "pieces": [
    {
      "designation": "Plaquettes de frein",
      "reference": "ABC123",
      "quantite": "2",
      "urgence": "Urgent ⚡"
    }
  ],
  "files": [
    {
      "name": "photo.jpg",
      "size": 2048,
      "type": "image/jpeg",
      "data": "data:image/jpeg;base64,..."
    }
  ],
  "timestamp": "2026-07-05T12:00:00.000Z"
}
```

## 📞 Contacts AUTOP

- **Téléphone 1** : +216 98 774 525
- **Téléphone 2** : +216 98 171 411
- **Email** : comptoir.distribution@autop.tn
- **WhatsApp** : https://wa.me/21698774525

## 📋 Numéro de suivi

Format automatique : `DEM-YYYYMMDD-###`

Exemple : `DEM-20260705-001`
- **DEM** : Préfixe (Demande)
- **20260705** : Date (YYYYMMDD)
- **001** : Numéro aléatoire (001-999)

## 🔧 Développement

### Ajouter une nouvelle fonctionnalité

1. Modifier les fichiers appropriés (HTML, CSS, JS)
2. Tester en local
3. Commiter les changements
4. GitHub Pages se met à jour automatiquement

### Technologies utilisées

- **HTML5** - Structure sémantique
- **CSS3** - Design responsive avec Grid/Flexbox
- **JavaScript Vanilla** - Aucune dépendance
- **localStorage** - Stockage des données
- **GitHub Pages** - Hébergement statique gratuit

## 📄 License

© 2026 AUTOP. Tous droits réservés.

## 🤝 Support

Pour toute question ou problème :
- 📧 Email : comptoir.distribution@autop.tn
- 📱 WhatsApp : +216 98 774 525
- 📞 Téléphone : +216 98 171 411

---

**Dernière mise à jour** : 5 juillet 2026
**Version** : 1.0.0
