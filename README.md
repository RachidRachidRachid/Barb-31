# BARBER PRO DZ 💈

Application web PWA de réservation pour salon de coiffure — gratuite, responsive, installable, sans backend (100% localStorage).

## 📁 Structure du projet

```
BARBER-PRO/
├── index.html      → Site client complet (HTML + CSS + JS intégrés dans un seul fichier)
├── admin.html      → Espace administrateur complet (HTML + CSS + JS intégrés dans un seul fichier)
├── manifest.json   → Configuration PWA (doit rester un fichier séparé, obligatoire pour l'installation)
├── sw.js           → Service worker / mode hors-ligne (doit rester un fichier séparé, obligatoire par les navigateurs)
└── icons/          → Icônes PWA (192px / 512px, standard + maskable)
```

> Tout le CSS et le JavaScript du projet sont directement intégrés dans `index.html` et `admin.html` (balises `<style>` et `<script>`) — il n'y a plus de dossiers `css/` ni `js/`. Seuls `manifest.json`, `sw.js` et les icônes restent en fichiers séparés, car c'est une exigence technique des navigateurs pour qu'une PWA soit installable.

## 🔑 Connexion admin par défaut

- URL : `admin.html`
- Identifiant : `admin`
- Mot de passe : `admin123`

⚠️ Changez ce mot de passe dans **Paramètres** dès la mise en ligne. Cette authentification est côté navigateur (pas de serveur) — suffisante pour un usage interne simple, mais ne protège pas des données sensibles.

## 💰 Tarifs préchargés

| Prestation | Prix |
|---|---|
| Coupe Homme | 500 DA |
| Coupe Enfant | 450 DA |
| Soin Protéiné | 2000 DA |
| Kératine | 2000 DA |
| Séchage + Lissage | 300 DA |
| Gommage | 300 DA |
| Nettoyage de Peau | 250 DA |

Modifiable à tout moment dans **Admin → Prestations**.

Coiffeurs préchargés : **Rachid Mgh** et **Louay** (modifiable dans **Admin → Coiffeurs**).
Réseaux sociaux préchargés dans **Admin → Paramètres** (Facebook/Instagram : Rachid Mgh, Snapchat : Louay Louay) — à corriger avec vos vrais liens si besoin.

## 🚀 Déploiement sur GitHub Pages (gratuit)

1. Créer un compte sur [github.com](https://github.com)
2. Cliquer sur **New repository**, nommer par exemple `BARBER-PRO`
3. Envoyer **tous les fichiers de ce dossier** (glisser-déposer sur GitHub ou via Git)
4. Aller dans **Settings → Pages**
5. Source : **Deploy from a branch** → Branche `main` → dossier `/(root)` → **Save**
6. Après 1-2 minutes, le site est en ligne à :
   `https://VotreNom.github.io/BARBER-PRO/`

## 📱 Installer comme application

Une fois le site en ligne (PWA nécessite HTTPS, GitHub Pages le fournit automatiquement) :
- **Android / Chrome** : bouton "Installer" qui apparaît dans le site, ou menu ⋮ → *Ajouter à l'écran d'accueil*
- **iPhone / Safari** : bouton Partager → *Sur l'écran d'accueil*
- **PC (Chrome/Edge)** : icône d'installation dans la barre d'adresse

## ⚙️ Personnalisation rapide

- **Nom, slogan, adresse, téléphone, réseaux sociaux** → Admin → Paramètres
- **Horaires d'ouverture** → Admin → Horaires
- **Photos de la galerie** → Admin → Galerie (coller une URL d'image)
- **Coiffeurs / prestations / prix** → Admin → Coiffeurs / Prestations

## 💾 Sauvegarde des données

Toutes les données (réservations, clients, coiffeurs...) sont stockées **dans le navigateur** (localStorage), propre à chaque appareil/navigateur. Pensez à faire un export régulier :
- Admin → Paramètres → **Export Excel / PDF / Sauvegarde JSON**

## 🛠️ Technologies utilisées

HTML5 · CSS3 · JavaScript (ES6) · localStorage · Chart.js · FullCalendar · SheetJS · jsPDF · Font Awesome · PWA (manifest + service worker)

---

Fait avec ✂️ pour **BARBER PRO DZ**.
