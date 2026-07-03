================================================================================
              WEB RADIO PLAYER - GUIDE D'INSTALLATION PWA
================================================================================

CONTENU DES FICHIERS
--------------------
- index.html       : Application web (player radio)
- manifest.json    : Configuration de l'application installable
- sw.js            : Service Worker (fonctionnement hors-ligne)
- icon-192.png     : Icône 192x192 pixels
- icon-512.png     : Icône 512x512 pixels
- README.txt       : Ce fichier

--------------------------------------------------------------------------------

HÉBERGEMENT REQUIS
------------------
Tous ces fichiers doivent être hébergés sur un serveur web accessible en HTTPS.
(Le protocole HTTPS est OBLIGATOIRE pour les PWA et Service Workers)

OPTIONS D'HÉBERGEMENT RECOMMANDÉES :

1. GitHub Pages (Gratuit)
   - Créer un repository GitHub
   - Activer GitHub Pages dans Settings > Pages
   - Push tous les fichiers dans la branche gh-pages ou main

2. Netlify (Gratuit, recommandé)
   - Aller sur https://www.netlify.com
   - Drag & drop le dossier contenant tous les fichiers
   - Déployement automatique avec HTTPS

3. Serveur personnel (NAS, Raspberry Pi, etc.)
   - Installer un certificat SSL (Let's Encrypt gratuit)
   - Configurer Apache/Nginx pour servir les fichiers

--------------------------------------------------------------------------------

INSTALLATION SUR iOS (iPhone/iPad)
----------------------------------
1. Ouvrez Safari et allez à l'adresse de votre Web Radio Player
2. Attendez que la page soit complètement chargée
3. Appuyez sur le bouton de partage (carré avec flèche vers le haut)
4. Faites défiler et tapez sur "Ajouter à l'écran d'accueil"
5. Modifiez le nom si souhaité, puis tapez "Ajouter"
6. L'icône apparaîtra sur votre écran d'accueil
7. Appuyez dessus pour lancer l'application !

NOTE : Safari est obligatoire sur iOS. Les autres navigateurs ne permettent pas
l'installation d'applications sur l'écran d'accueil.

--------------------------------------------------------------------------------

INSTALLATION SUR ANDROID (Chrome)
---------------------------------
1. Ouvrez Chrome et allez à l'adresse de votre Web Radio Player
2. Attendez que la page soit complètement chargée
3. Une bannière devrait apparaître en bas de l'écran :
   "Ajouter Web Radio Player à l'écran d'accueil"
4. Tapez sur "Installer" (ou les 3 points > "Ajouter à l'écran d'accueil")
5. L'application apparaîtra dans votre liste d'applications

ALTERNATIVE :
- Tapez sur les 3 points verticaux (⋮) en haut à droite
- Sélectionnez "Ajouter à l'écran d'accueil" ou "Installer l'application"

--------------------------------------------------------------------------------

FONCTIONNEMENT HORS-LIGNE
-------------------------
Une fois installée, l'interface de l'application fonctionne hors-ligne.
Vous verrez alors un message dans le player indiquant l'état de connexion.

NOTE : La lecture des radios nécessite une connexion internet active.
Le contenu audio n'est pas mis en cache.

--------------------------------------------------------------------------------

TEST EN LOCAL (localhost)
-------------------------
Pour tester avant de déployer :
1. Installez un serveur web local (ex: Live Server sur VS Code, ou python -m http.server)
2. Ouvrez http://localhost:8000 dans votre navigateur
3. Note : Le service worker peut nécessiter Chrome avec certains flags activés

--------------------------------------------------------------------------------

DÉPANNAGE
---------
- L'application ne s'installe pas ?
  → Vérifiez que vous êtes bien en HTTPS (pas HTTP)

- L'icône n'apparaît pas sur iOS ?
  → Assurez-vous d'utiliser Safari, pas Chrome ou Firefox

- L'application ne se lance pas en plein écran ?
  → Fermez complètement Safari et rouvrez-le

================================================================================
