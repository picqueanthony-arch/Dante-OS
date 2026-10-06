<div align="center">

# Dante OS

**Le launcher root qui rend son téléphone à son propriétaire.**<br>
*The root launcher that gives a phone back to its owner.*

[**Télécharger / Download**](https://github.com/picqueanthony-arch/Dante-OS/releases/latest) · [Français](#français) · [English](#english)

<img src="captures/01-bureau.jpg" width="190"> <img src="captures/02-pare-feu.jpg" width="190"> <img src="captures/03-filtre-dns.jpg" width="190"> <img src="captures/04-xray.jpg" width="190">

</div>

---

## Français

Dante OS est un **launcher Android** (bureau en pages, dock, dossiers, widgets, tiroir d'apps) auquel s'ajoute, sur un téléphone **rooté**, une boîte à outils pour voir et décider ce que fait ton téléphone : qui parle sur le réseau, ce qui est bloqué, ce que consomme la batterie, comment tourne le processeur.

Sans root, il reste un launcher complet, avec les outils qui n'en ont pas besoin. Aucun traqueur, aucune statistique, aucun compte.

### Ce qu'il y a dedans

| | Module | Root |
|---|---|:---:|
| 🧱 | **Pare-feu** : pour chaque app, Wi-Fi, données mobiles, itinérance, réseau local. Règles iptables, IPv4 et IPv6. | oui |
| 🛡️ | **Filtre DNS** : pubs, pisteurs et sites malveillants bloqués pour tout le téléphone, listes à jour, règles perso. | oui |
| 📡 | **XRay** : trafic réseau app par app, connexions, alertes (nouveau serveur, envoi inhabituel). | oui |
| ⚙️ | **Governor** : profils processeur et puce graphique (économie, équilibré, performance). | oui |
| 🔋 | **Battery Root** : courant, puissance, vraie capacité et santé de la batterie. | oui |
| 🔍 | **DEX Lab** : analyse locale des apps installées (source, autorisations, pisteurs, signature). | non |
| 📁 | **Fichiers** : explorateur, SMB, FTP, SFTP, USB, coffre, corbeille. | non |
| 🖥️ | **SSH** : terminal, fichiers distants, serveurs enregistrés (mots de passe chiffrés dans le Keystore Android). | non |
| 🎵 | **Sonic** : lecteur audio avec égaliseur et listes de lecture. | non |
| 📰 | **Actualités**, **Labo JSON**, **Private Node** (suivi de ton propre serveur), **Telemetry** (widgets), **Notifications** et **diagnostic** de l'appareil. | non |
| ⚙️ | **Réglages** : tous les réglages d'Android à plat, recherche directe, favoris, et un petit tableau de bord (batterie, température, mémoire, réseau, IP, état du DNS et du pare-feu). | oui |
| 🗂️ | **Multitâche** : tes modules et tes apps récents en cartes, avec leurs miniatures. Remplace l'écran Récents d'Android si tu le souhaites (option). | option |
| 📊 | **Barre Dante** : heure, notifications et état du téléphone par-dessus toutes les apps, glisser vers le bas pour ouvrir les panneaux (option). | oui |
| 📜 | **Logs appareil** : un logcat intégré, avec recherche et filtres, pour comprendre un souci ou le signaler. | non |
| 📖 | **Guide** : une encyclopédie intégrée de 75 fiches (gestes, modules, transparence totale). | non |

<div align="center">
<img src="captures/05-governor.jpg" width="190"> <img src="captures/06-battery-root.jpg" width="190"> <img src="captures/07-dex-lab.jpg" width="190"> <img src="captures/08-guide.jpg" width="190">
</div>

### Personnalisation

- **Le dock, à ta façon** : tu y poses les apps *et* les modules que tu veux, avec zoom et pastilles de notifications. En colonne à gauche ou à droite, en rangée en haut ou en bas.
- **Les icônes, une par une** : chaque app ou module peut prendre une icône d'un **pack d'icônes** installé (format Nova / ADW) ou **une image de ton téléphone** (PNG, JPEG…). Tu peux revenir à l'icône d'origine à tout moment.
- **Le bureau** : pages, dossiers, widgets Android, tiroir d'applications, fond d'écran.

### Transparence

Dante OS fait le contraire de ce qu'on voit d'habitude : il explique ce qu'il fait.

- **Aucun traqueur, aucune statistique.** Rien n'est envoyé « pour améliorer le service ».
- **Tes données restent sur le téléphone.** Dante n'appelle que ce dont il a besoin pour ce que *tu* lui demandes : les listes du filtre DNS, tes flux d'actualités, tes propres serveurs, et ton adresse IP publique seulement si tu touches « Afficher » dans Réglages.
- **Mots de passe chiffrés** dans le Keystore Android (AES-GCM).
- **Le multitâche lit la liste des apps ouvertes avec le root** (la même que celle de l'écran Récents d'Android) et les miniatures que le système garde déjà ; rien n'est envoyé.
- **Le root, pour voir et décider.** Chaque action sensible demande confirmation et se défait.
- Le Guide intégré liste, fiche par fiche, **ce que l'app lit, modifie et envoie**.

**Le code source n'est pas publié** (choix de l'auteur : l'outil touche au système). Ce que décrit le Guide se vérifie avec des outils Android ordinaires : liste des autorisations, trafic réseau, règles iptables.

Dante OS a été conçu, testé et corrigé par une seule personne, pendant huit mois, **avec l'aide d'une IA pour écrire le code**.

### Installer

Dante OS n'est pas sur le Play Store (root, filtrage réseau et accès aux apps ne sont pas compatibles avec ses règles).

**Avec Obtainium** (recommandé, il prévient des mises à jour) :
1. Installer [Obtainium](https://obtainium.imranr.dev/).
2. *Ajouter une app* → coller `https://github.com/picqueanthony-arch/Dante-OS`.

**À la main :** télécharger `Dante-OS-<version>.apk` dans la [dernière release](https://github.com/picqueanthony-arch/Dante-OS/releases/latest), vérifier l'empreinte (`sha256sum -c Dante-OS-<version>.apk.sha256`), installer.

Les mises à jour se font **par-dessus** : tes réglages sont gardés (même signature).

Au premier lancement, un accueil en 4 étapes fait le diagnostic du téléphone, te laisse choisir *Mode complet (root)* ou *Launcher seul*, et propose de définir Dante OS comme écran d'accueil. Pour revenir à ton ancien launcher : Réglages Android → Apps → Apps par défaut → Application d'accueil.

### Compatibilité

- **Android 10 ou plus.** Processeurs ARM 64 bits et 32 bits.
- Testé sur **OnePlus 13** (Android 15, root), **Galaxy Note 9** (Android 10, root) et **Galaxy Tab A 10.1** (Android 11, sans root). Ailleurs, certaines fonctions peuvent différer : le diagnostic de l'accueil te le dit.
- **Français et anglais** (réglable dans *À propos*).

### Un logcat intégré

*Logs appareil* est un **logcat maison**, comme la fenêtre Logcat d'Android Studio mais sur le téléphone (filtré sur Dante OS), sans PC ni adb.

- **DANTE** : l'activité des modules (pare-feu, filtre DNS, XRay, SSH, actualités, démarrages et plantages). **RAW** : le logcat brut de Dante OS lui-même (Android ne laisse une app lire que ses propres lignes : les journaux des autres apps ne sont jamais lus).
- **Recherche** dans les tags, les messages et les paquets ; filtres par gravité (I / W / E) et par source ; « critiques seulement ».
- Le bruit des services bavards est coupé par défaut (**CLEAN**). Pause, copie, **export JSON** en un geste.
- Les événements sont gardés sur le téléphone, même écran des logs fermé. Jamais de mot de passe, de clé ni de texte de notification. Rien n'en sort tant que tu ne le partages pas toi-même.

<div align="center">
<img src="captures/09-logs-dante.jpg" width="190"> <img src="captures/11-logs-xray.jpg" width="190"> <img src="captures/10-logs-raw.jpg" width="190">
</div>

### À savoir

- Fourni **« tel quel », sans garantie**. Dante OS ne s'impose aucune limite : une mauvaise règle de pare-feu ou de DNS peut couper ton réseau, un mauvais réglage peut rendre le téléphone instable, voire l'empêcher de démarrer (bootloop) ou lui faire perdre des données. **Tu es responsable de ce que tu actives ; l'auteur ne peut être tenu responsable des dommages.** Sauvegarde avant, et sache comment restaurer ton téléphone (mode sans échec de Magisk, image boot d'origine).
- Dante OS n'est pas un antivirus : ses audits informent, ils ne jugent pas.
- Il ne contourne aucune protection pour débloquer des fonctions payantes.
- Le nom « Dante OS » et son logo restent la propriété de l'auteur.

Un bug, une omission ? Ouvre *Logs appareil* (le logcat intégré), copie ou exporte le journal, et décris ce qui s'est passé (heure, module, ce que tu attendais) dans les [Issues](https://github.com/picqueanthony-arch/Dante-OS/issues).

Si Dante OS te sert, tu peux soutenir le projet : [PayPal](https://www.paypal.me/dante14250). C'est facultatif.

---

## English

Dante OS is an **Android launcher** (paged desktop, dock, folders, widgets, app drawer) with, on a **rooted** phone, a toolbox to see and decide what your phone does: who talks on the network, what gets blocked, what the battery really does, how the processor runs.

Without root it stays a complete launcher, with the tools that don't need it. No tracker, no statistics, no account.

### What's inside

| | Module | Root |
|---|---|:---:|
| 🧱 | **Firewall**: per app, Wi-Fi, mobile data, roaming, local network. iptables rules, IPv4 and IPv6. | yes |
| 🛡️ | **DNS filter**: ads, trackers and malicious sites blocked phone-wide, updated lists, custom rules. | yes |
| 📡 | **XRay**: per-app network traffic, connections, alerts (new server, unusual upload). | yes |
| ⚙️ | **Governor**: processor and GPU profiles (economy, balanced, performance). | yes |
| 🔋 | **Battery Root**: current, power, real capacity and battery health. | yes |
| 🔍 | **DEX Lab**: local analysis of installed apps (source, permissions, trackers, signature). | no |
| 📁 | **Files**: explorer, SMB, FTP, SFTP, USB, vault, trash. | no |
| 🖥️ | **SSH**: terminal, remote files, saved servers (passwords encrypted in the Android Keystore). | no |
| 🎵 | **Sonic**: audio player with equalizer and playlists. | no |
| 📰 | **News**, **JSON Lab**, **Private Node** (watch your own server), **Telemetry** (widgets), **Notifications** and device **diagnostics**. | no |
| ⚙️ | **Settings**: every Android setting flat, direct search, favorites, and a small dashboard (battery, temperature, memory, network, IP, DNS and firewall state). | yes |
| 🗂️ | **Multitasking**: your recent modules and apps as cards, with thumbnails. Can replace Android's Recents screen (option). | option |
| 📊 | **Dante bar**: clock, notifications and phone status over every app, swipe down to open the panels (option). | yes |
| 📜 | **Device logs**: a built-in logcat, with search and filters, to understand a problem or report it. | no |
| 📖 | **Guide**: a built-in encyclopedia of 75 pages (gestures, modules, total transparency). | no |

### Customization

- **The dock, your way**: put the apps *and* the modules you want in it, with zoom and notification badges. A column on the left or right, a row at the top or bottom.
- **Icons, one by one**: every app or module can take an icon from an installed **icon pack** (Nova / ADW format) or **an image from your phone** (PNG, JPEG…). You can go back to the original icon at any time.
- **The desktop**: pages, folders, Android widgets, app drawer, wallpaper.

### Transparency

Dante OS does the opposite of the usual: it explains what it does.

- **No tracker, no statistics.** Nothing is sent "to improve the service".
- **Your data stays on the phone.** Dante only contacts what it needs for what *you* ask: DNS filter lists, your news feeds, your own servers, and your public IP address only if you tap "Show" in Settings.
- **Encrypted passwords** in the Android Keystore (AES-GCM).
- **Multitasking reads the list of open apps with root** (the same one Android's Recents screen uses) and the thumbnails the system already keeps; nothing is sent.
- **Root to see and decide.** Every sensitive action asks for confirmation and can be undone.
- The built-in Guide lists, page by page, **what the app reads, changes and sends**.

**The source code is not published** (the author's choice: the tool touches the system). What the Guide describes can be checked with ordinary Android tools: permission list, network traffic, iptables rules.

Dante OS was designed, tested and fixed by one person over eight months, **with the help of an AI to write the code**.

### Install

Dante OS is not on the Play Store (root, network filtering and app access don't fit its rules).

**With Obtainium** (recommended, it tells you about updates):
1. Install [Obtainium](https://obtainium.imranr.dev/).
2. *Add app* → paste `https://github.com/picqueanthony-arch/Dante-OS`.

**By hand:** download `Dante-OS-<version>.apk` from the [latest release](https://github.com/picqueanthony-arch/Dante-OS/releases/latest), check the checksum (`sha256sum -c Dante-OS-<version>.apk.sha256`), install.

Updates install **over** the existing app: your settings are kept (same signature).

On first launch a 4-step welcome checks your phone, lets you pick *Full mode (root)* or *Launcher only*, and offers to set Dante OS as your home screen. To go back to your old launcher: Android Settings → Apps → Default apps → Home app.

### Compatibility

- **Android 10 or newer.** 64-bit and 32-bit ARM processors.
- Tested on **OnePlus 13** (Android 15, rooted), **Galaxy Note 9** (Android 10, rooted) and **Galaxy Tab A 10.1** (Android 11, not rooted). Elsewhere some features may differ: the welcome diagnostic tells you.
- **French and English** (switch in *About*).

### A built-in logcat

*Device logs* is a **homemade logcat**, like the Logcat window of Android Studio but on the phone (filtered on Dante OS), no PC or adb needed.

- **DANTE**: what the modules are doing (firewall, DNS filter, XRay, SSH, news, starts and crashes). **RAW**: the raw logcat of Dante OS itself (Android only lets an app read its own lines: the logs of other apps are never read).
- **Search** in tags, messages and packages; filters by severity (I / W / E) and by source; "critical only".
- The chatter of noisy services is muted by default (**CLEAN**). Pause, copy, **JSON export** in one tap.
- Events are kept on the phone, even with the logs screen closed. Never a password, a key or a notification text. Nothing leaves the phone unless you share it yourself.

<div align="center">
<img src="captures/09-logs-dante.jpg" width="190"> <img src="captures/11-logs-xray.jpg" width="190"> <img src="captures/10-logs-raw.jpg" width="190">
</div>

### Good to know

- Provided **"as is", without warranty**. Dante OS puts no limit on itself: a wrong firewall or DNS rule can cut your network, a wrong setting can make the phone unstable, even keep it from booting (bootloop) or lose data. **You are responsible for what you enable; the author cannot be held responsible for any damage.** Back up first, and know how to restore your phone (Magisk safe mode, stock boot image).
- Dante OS is not an antivirus: its audits inform, they do not judge.
- It does not bypass protections to unlock paid features.
- The name "Dante OS" and its logo remain the property of the author.

A bug or an omission? Open *Device logs* (the built-in logcat), copy or export the log, and describe what happened (time, module, what you expected) in the [Issues](https://github.com/picqueanthony-arch/Dante-OS/issues).

If Dante OS is useful to you, you can support the project: [PayPal](https://www.paypal.me/dante14250). It's optional.
