# Chat2Go : mise en ligne (gratuit au départ)

## 1. Créer le projet Firebase
1. Va sur https://console.firebase.google.com et connecte-toi avec un compte Google.
2. « Ajouter un projet » → nom : chat2go → tu peux désactiver Google Analytics.
3. Sur la page du projet, clique sur l'icône **Web** (</>) → donne un nom → « Enregistrer l'application ».
4. Firebase affiche un bloc `firebaseConfig` : copie les valeurs.

## 2. Coller la configuration
Ouvre `index.html`, cherche `COLLE_ICI` et remplace les 4 valeurs
(apiKey, authDomain, projectId, appId) par celles de Firebase.

## 3. Activer les comptes
Menu **Authentication** → « Commencer » → méthode **Adresse e-mail/Mot de passe** → Activer.

## 4. Activer la base de données
Menu **Firestore Database** → « Créer une base de données » → mode production → choisis une région proche.
Onglet **Règles** → efface tout, colle le contenu de `firestore.rules` → **Publier**.

## 5. Mettre l'application en ligne (au choix)
- **Netlify Drop** : va sur https://app.netlify.com/drop et glisse-dépose le dossier `chat2go`.
- **Cloudflare Pages** ou **GitHub Pages** : même principe, tu envoies les fichiers du dossier.
Tu obtiens un lien en https:// (obligatoire pour la caméra et l'installation).

## 6. Autoriser ton lien dans Firebase
**Authentication** → onglet **Paramètres** → **Domaines autorisés** → ajoute le domaine de ton lien
(par exemple monapp.netlify.app).

## 7. Installer sur le téléphone
- **Android (Chrome)** : menu ⋮ → « Installer l'application » ou « Ajouter à l'écran d'accueil ».
- **iPhone (Safari)** : bouton Partager → « Sur l'écran d'accueil ».

## À savoir
- Les photos sont stockées en petit format directement dans la base (pas de Firebase Storage).
- Les messages et photos sont supprimés par l'application 5 secondes après que le destinataire les a vus.
  Ce n'est pas une sécurité absolue : une capture d'écran reste possible.
- Les limites et conditions de l'offre gratuite Firebase peuvent changer : vérifie-les dans la console.
- Pour aller plus loin (notifications, amis, App Store / Google Play), il faudra du développement en plus.
