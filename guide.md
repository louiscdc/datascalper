# Petit guide de tes données

![brrrr data](https://media1.tenor.com/images/9e99c0822ebb042fcb7fbb1fb757d88c/tenor.gif)


*V.0.1 -04-2021*

## 1. Objectif
Rassembler des outils et techniques simples à utiliser pour une large audience, souhaitant un meilleur contrôle sur leur identité numérique.
Les solutions présentées sont dirigées vers une utilisation classique du web et de ses ressources, pour un public large.

### 2. Définition
Un outil est présenté comme respectueux des données personnelles lorsqu'il ne concede aucune information [PII](https://en.wikipedia.org/wiki/Personal_data) a des fins commerciales, et cevers des entreprises tierces mais aussi dans sa propre branche.
Le modèle open source se rappproche le plus d'une éthique des données, mais il faut faire attention sa dénomination, car souvent le code de l'outil client est ouvert, mais pas celui du serveur.


# Vie Privée + Sécurité = ☯️

## Quelques questions à se poser:

1. Pourquoi une application de messagerie a besoin de connaître ma date de naissance ?
2. Pourquoi il est obligatoire d'entrer son numéro de cellulaire dans un compte d'e-commerce ?

Ces questions sont au coeur de la réflexion de l'utilisation des services du web, de leur influence sur nos pratiques et même de la sécurité de nos données. Il est essentiel de comprendre la multitude de moyens visants à collecter des informations profitables.

Chaque outil est relativement sécurisé (dans la mesure du possible), mais possèdent tous les caracteres suivants:

1. Audit régulié consultable (ex: Github)
2. Rapports transparents
3. Code source vérifiable
4. Politique de confidentialité *claire*
5. Mesures de sécurité suffisantes

Ces facteurs sont déterminants dans la confiance accordée aux outils, car bien que certains soient largement utilisés et sécurisés, la collecte de données transite par plusieurs instances, à des fins commerciales mais aussi analytiques, 


Cela se résume par:
**+ de données en transit = + large champ d'attaque.** (comprendre ici que l'attaquant est toute entitée externe)

Ainsi, la sécurité et la confidentialité des données sont deux paramètres pouvants (et devants) s'accorder. 

# Monumentum
Les solutions présentées ne sont pas miraculeuses, ni infaillibles, mais elles représentent une autre manière d'utiliser le web, prudente et réfléchie.

De plus, la méthodologie de sélection repose sur une opinion globale provenant de recherches et de questionnement auprès des communautées spécialisées.

Ce guide ne s'appuit pas entièrement sur les lois des différents pays d'ou proviennent les outils, car ce n'est pas toujours synonyme de fiabilité. Mais en choisissant des services majoritairement **sécurisés de bout en bout** (E2EE), open source, débattus au quotiden et remis en question, on réduit la possibilité d'une attaque ainsi que d'une utilisation abusive de ses données personnelles.

Finalement, tout repose sur une confiance envers un service, faites vos recherches !

# Sommaire

* [Réseau](#reseau)
* [Ordinateur](#ordinateur)
* [Systèmes d'exploitation](#systemes-dexploitation)
* [Conseils en vrac](#conseils-en-vrac)
* [Navigateurs web](#navigateurs-web)
* [Moteurs de recherche](#moteurs-de-recherche)
* [Alternatives](#alternatives)
* [Fichiers](#fichiers)
* [Communications instantannées](#communications-instantannees)
* [Smartphone](#smartphone)
* [Sécurité générale ](#securite-generale)


## Wiki


À venir...



## Références
1. privacytools.io
2. eff.org


# Réseau

## Router
Le router/modem proposé par un opérateur comporte autant de risques sécuritaires que privés:

* ❌ Updates manquantes
* ❌ Manque de configuration
* ❌ Qualité du traffic parfois limité
* ❌ [L'opérateur a un grand regard sur le traffic](https://spreadprivacy.com/protection-from-isp-spying/)


Il est préférable de choisir un router compatible avec un firewall réputé:

### [Netgate](https://www.pfsense.org/products/)

### [Protecli](https://protectli.com/)


	* ⚠️ Les appareils Ubiquiti ne sont pas présentés car une (récente) brèche (https://krebsonsecurity.com/2021/03/whistleblower-ubiquiti-breach-catastrophic/) met en question leur fiabilité. 


### Firewall

* [Pfsense](https://www.pfsense.org/)
* [Openwrt](https://openwrt.org/start)

### DNS

Tout comme une IP, et ce malgré le protocol TLS, les requêtes DNS peuvent êtres compromises et attirer les regards indiscret.


* Résolveurs DNS chiffrés : https://www.privacytools.io/providers/dns/



	* ⚠️ L'option *DNS over HTTPS* est un moyen expérimental de fournir une résolution DNS via HTTPS, et représennte plusieurs [risques](https://www.zdnet.com/article/dns-over-https-causes-more-problems-than-it-solves-experts-say/).


### VPN config:

Il est possible d'intégrer un VPN au router, mais il est recommandé d'en utiliser un sur un point d'acces, afin de libérer les ressources du router (surtout si on installe un IDS).

#### Openvpn config: 

* ✔️ Simple à configurer
* ❌ Plus lent 

#### Wireguard config:

* ✔️ Rapide
* ❌ Moins privé, enregistre 9entre autre) l'IP dans le server VPN


# Ordinateur

## Données physiques

Les composants d'un ordinateur possedent des défaults majeurs, comme le fait (pour certains) de communiquer directement avec le fabricant.

📎https://fossbytes.com/intel-processor-backdoor-management-engine/

Il existe peu d'alternatives aux composants habituels.


# Systèmes d'exploitation

## Microsoft / Macos

* ❌ Microsoft recueille, utilise et divulgue des informations personnelles. Ainsi, les données OneDrive, les recherches Cortana et l'historique du navigateur MS peuvent être vendus à des tiers.

	- 📎https://thehackernews.com/2016/02/microsoft-windows10-privacy.html
	- 📎https://arstechnica.com/information-technology/2015/08/even-when-told-not-to-windows-10-just-cant-stop-talking-to-microsoft/

* ❌ Macos n'est pas très différent, il reste un bon début de modifier certains [paramètres]( https://spreadprivacy.com/mac-privacy-tips/). 


Néanmoins, s'il est obligatoire d'utiliser Windows, voici quelques moyens pour limitter l'exfiltration des données personnelles:

* [Conseils de confidentialité](https://spreadprivacy.com/windows-10-privacy-tips/)
* [Windows Spy Blocker](https://github.com/crazy-max/WindowsSpyBlocker) 

## Linux

* ✔️ Large choix de distributions
* ✔️ Aucune entitée unique possedant l'OS
* ✔️ Customisable au goût de chacun
* ✔️ Communauté active et *réactive*

### Distributions simples


Paradoxalement à ce que l'imaginaire collectif semble penser, plusieurs distributions sont faciles d'utilisation pour des tâches quotidiennes, telles que **[PureOS](https://pureos.net/)** ou **[Ubuntu](https://ubuntu.com/)**. Il existe un grand nombre de distributions, dont les plus supportées sont:

* ✔️ [Debian](https://debian.org) 
* ✔️ [Mint](https://linuxmint.com/) 


### Distributions avancées

Les distributions présentées se spécialisent dans leurs caractèristiques: 

* [QubesOS](https://www.qubes-os.org/): Système sous virtualisation, fonctionne en templates afin de séparer les tâches.

* [Tails](https://tails.boum.org/): Système portable, possibilité de chiffrement, sous le réseau Tor.  

* [Whonix](https://www.whonix.org/): Système sous machines virtuelles.


# Navigateurs web


* ❌ Chrome: Navigateur invasif, peu modifiable, reposant sur Chromium et appartenant à Google, non recommandé d'un point de vu confidentialité.

* ✔️ [Firefox](https://www.mozilla.org/en-US/firefox/new/) : Géré par la fondation Mozilla (non profit) et disponible depuis longtemps, c'est une valeure sûre quand on modifie certains paramètres:

1. [Modification par une extension]( https://addons.mozilla.org/en-US/firefox/addon/privacy-settings) 

 
2. Modification manuelle: https://privacytools.io/browsers/#about_config



		* ⚠️ En choisissant de bloquer certains trackers, des sites peuvent devenir moins performant et parfois inaccessibles.



* ✔️ [Librewolf](https://librewolf-community.gitlab.io/): : Fork de Firefox, provient avec plusieurs options directement installées.

		* ⚠️ Le navigateur Brave n'est pas encore suffisement analysé pour être mis dans cette liste.



### Tester son navigateur


Il est possible de tester les capacités défensives de son navigateur, grâce à un service développé par l'[EFF]( https://eff.org): https://coveryourtracks.eff.org/


## Extensions

En combinant certaines extensions, on renforce la capicité du navigateur à bloquer les trackers.


### Bloqueurs 

* ✔️ [Ublock]( https://ublockorigin.com/): Bloqueur avec options avancées.

* ✔️ [ClearUrl](https://addons.mozilla.org/en-US/firefox/addon/clearurls/): Supprime le tracking dans les URL.


	* ⚠️ Plus on installe d'extensions sur un navigateur, plus son empreinte numérique augmente, donc il est bon de choisir seulement les plus utiles. 


### DNS(bis) 
* [Dnscrypt-proxy](https://github.com/DNSCrypt/dnscrypt-proxy): Nombreuses fonctionnalités de chiffrement et d'anonymisation.

# Moteurs de recherche

* ❌ Bing, Google et autres collèctent vos recherches, mots clés, historique, préférences... 


* ✔️ [Duckduckgo](https://duckduckgo.com/): Anonymise les requêtes, pas de logs, ne collecte ni ne partage de l'information identitifiable.
* ✔️ [Searx](https://searx.me/): Plusieurs instances, possibilité d'auto héberger.


# Alternatives

Il existe des moyens d'accéder aux majors (Youtube, Facebook, Twitter...), en réduisant le tracking de ces plateformes grâce à des alternatives pouvants même êtres auto-hébergées.  

* ✔️ Clones de + 100 sites populaires: https://github.com/GorvGoyl/clone-wars
* ✔️ Invidious (Youtube): https://api.invidious.io/
* ✔️ Nitter (Twitter): https://github.com/zedeus/nitter/wiki/Instances
* ✔️ Teddit (Reddit): https://codeberg.org/teddit/teddit (sans JavaScript)
* ✔️ Bibliogram (Instagram): https://git.sr.ht/~cadence/bibliogram-docs/tree/master/docs/Instances.md

* ✔️ [FreeTube](https://freetubeapp.io/) (client Youtube)


Pour les alternatives aux applications mobiles, voir la section [Applications](#applications) 


	* ⚠️ Le temps de disponibilité n'est pas parfait car certaines instances fonctionnent mieux que d'autres en raison du blocage fait par les sites d'ou proviennent le contenu.

# Fichiers

## Tranfer


* ❌ WeTransfer: Pas de chiffrement E2EE, communique avec des trackers (googletagmanager.com, facebook.net, bing.com, amazon-adsystem.com...), obligation d'utiliser un courriel et  limitation de taille des fichiers pour la version gratuite.  
 
 	* ⚠️ Si vos données sont chiffrés mais que l'hbéergeur possède la clé pour les déverrouiller, il ne s'agit pas d'E2EE.


* ❌ Le transfer de documents par courriel est limité, et peu sécurisé ([Voir section courriel](#courriel)


* ✔️ [Wormhole CLI](https://github.com/magic-wormhole/magic-wormhole) (Unix): 
	* ✔️ [Wormhole WEB](https://wormhole.app/): Max 10GB par tranfer,   

* ✔️ [Bitwarden Send](https://bitwarden.com/products/send/): Permet d'envoyer des fichiers légers (mots de passes, tokens...) avec des options comme l'éxpiration du lien.



## Hébergement 

Choisir une solution d'hébergement en ligne, c'est faire confiance à un tier gérant ses photos, vidéos, musiques etc. Auto héberger demande des efforts, mais s'avère plus sécuritaire et propice au respect de données personelles.


* ❌ Dropbox, Google Drive, OneDrive: Pas de chiffrement 'E2E', accède, stocke et analyse les fichiers et les partage avec des sociétés affiliées et des tiers, selon selon leurs conditions d'utilisation. Exige votre nom complet, votre adresse électronique et d'autres informations personnelles pour pouvoir utiliser le service.


* ✔️ [Nextcloud](https://nextcloud.com/): Service open source (évidemment), auto hébergement ou déployement sur VPS, options d'encryption  durant le transfert de données, au repos, et client à client.


 	* ⚠️ Le contenu stocké dans la plupart des serveurs des hébergeurs cloud n'est pas chiffré.


## Notes

* ✔️ [Joplin](https://joplinapp.org/) 
* ✔️ [Obsidian](https://obsidian.md) 

## Plateformes collaboratives

* ❌ Google docs, Sharepoint... enregistrent et ont un droit de regard sur les données émises.

* ✔️ [Cryptpad](https://www.cryptpad.fr)
* ✔️ [Etherpad.org](https://www.etherpad.org)
* ✔️ [Mattermost](https://mattermost.com/) 


# Communications instantannées

## Messageries

Il est **vraiment** recommendé d'abandonner le SMS et l'appel téléphonique: Votre opérateur cellulaire peut voir vos  SMS, ils peuvent être interceptés par des dispositifs pirates (légaux ou non), et un numéro de téléphone simple *en théorie/pratique* à détourner. Si quelqu'un prend le contrôle du numéro de téléphone d'une autre personne, il a accès donc à sa messagerie SMS, 



### Centralisées

Il en existe principalement 3 types:

1. Messagerie en texte clair : les métadonnées et le contenu sont divulgués à tout le monde.
2. Messagerie cryptée client-serveur : les métadonnées et le contenu sont divulgués au serveur.
3. Messagerie chiffrée de bout en bout : les métadonnées sont transmises au serveur mais le contenu est protégé.

* ❌ Facebook Messenger, Whatsapp: Pour les centaines de raisons possibles résumées par ce graphique:

![data](https://i1.wp.com/9to5mac.com/wp-content/uploads/sites/6/2021/01/App-privacy-labels-messaging-apps.png?w=2000&quality=82&strip=all&ssl=1)


Ces applications ont donc démontré leur gourmandise pour certains types de données.



* ❌ Telegram est certes une alternative, mais enregistrec(entre autre) les messages, et la politique de confidentialité n,est pas convaincante.


* ✔️ [Signal](https://signal.org): Parmis les meilleures solutions actuelles, aucune donnée n'est enregistrée dans le cloud, E2EE par défaut, une politique de confidentialité claire, et simple d'utilisation pour tous.  
* ✔️ [Briar](https://briarproject.org/): Messagerie et forum chiffrés de peer-to-peer, les messages sont stockés sur l'appareil et passe par un réseau Tor.

### Féderrées

Une solution fédérée permet à plusieurs entitées de se rejoindre malgré des protocols différents, et venant de plusieurs serveurs.


* ✔️ [Element](https://element.io): Fonctionnant sous le protocol Matrix en ajoutant le chiffrement E2EE, ne requiert aucune information personnelle (courriel, numéro de cellulaire...), permet à de nombreux petits réseaux de communiquer entre eux. 


## Courriel

### Solutions

Le courrier électronique n'a pas été conçu dans un souci de confidentialité ou de sécurité, bien qu'il se modernise depuis la généralisation du chiffrement. 

* ❌  Gmail a donné aux développeurs tiers l'accès à l'API de la plate-forme, les entreprises et peuvent apprendre des informations sur vos habitudes de messagerie, vos achats, combien vous dépensez et qui vous êtes. Les données sont sensées êtres anonymisées, mais certains leaks ont démontré que non.

Bien qu'un courriel ne soit pas une option idéale, on peut améliorer sa sécurité et confidentialité en choisissant un service E2EE pour les utilisateurs de la même plateforme:

* ✔️ [Protonmail](https://protonmail.com): Service dirigé vers la confidentialité et la sécurité en Suisse.
* ✔️ [Tutanota](https:tutanota.com): Service dirigé vers la confidentialité et la sécurité en Allemagne, plusieurs options d'alias et d'un calendrier privé.


	* ⚠️ Si le destinaire ne possède pas le même hébergeur (que les deux cités plus haut), le contenu du courriel ne sera pas E2EE, il reste possible d'ajouter un mot de passe à communiquer au destinataire pour qu'il puisse déchiffrer le message.


### Alias

Des services proposent de créer des alis à son courriel principal.

* ✔️ [Simplelogin](https://simplelogin.io)


	* ⚠️ Lors d'une brèche de sécurité depuis un service en ligne, avoir un alias au lieu de son courriel principal permet de réduire la surface d'attaque et ainsi que de protéger son identité.



## Vidéo conférence

* ❌ Teams, Zoom, Slack etc. sont des plateformes difficilement remplaçables de part leurs options, bien qu'elles ne soient pas réputées pour leur politiques de confidentialité. Zoom à également mis du temps à intégrer l'E2EE, et ces plateformes se partagent un marché qui explose, donc leur capacité à collecter et distribuer des donnéés privées ne fait qu'augmenter. Il existe heureusement d'autres plateformes, aux options suffisantes.

### Vidéo et audio


* ✔️ [Jitsi](https://jitsi.org/): Disponible sur navigateur, auto hébergé, et bien sûr open source, forte alternative à Zoom.

### Vidéo, audio, messages

* ✔️ [Jami](https://jami.net/): Peer to peer, projet récent multi plateforme.
* ✔️ [Element](https://element.io): [voir description précédente](#federrees)



# Smartphone


## Système d'exploitation

### Android / IOS

* ❌ Android appartient à Google, oblige d'avoir un compte afin d'installer des applications depuis le PlayStore.
* ❌ IOS manque de choix de personnalisation, obligeant également à utiliser seulement les ressources choisies par Apple (jailberaker n'est pas une méthode recommandée).

À noter que remplacer IOS par un autre système d'exploitation est très expérimental, il vaut mieux utliser un smartphone originellement sous Android, et modifier le ROM.

* ✔️ [CalyxOS](https://calyxos.org/): ROM personnalisé et basé sur l'Android Open Source, prend également en charge le démarrage vérifié (verified boot). 
* ✔️ [GrapheneOS](https://grapheneos.org/):  
* ✔️ [/e](https://e.foundation/):  

### Linux (*en développement*)
* ✔️ [Unbuntu Touch](https://ubuntu-touch.io/)

## Market

* ❌ Google Play store et Apple store proposent en majorité des applications propriétaires, obligation d'avoir un compte relié à Google ou Apple.

* ✔️ [FDROID](https://calyxos.org/): Catalogue d'applications open source, compatible Android et propose 

	* ⚠️ Certaines applications ont besoin du service Google pour utiliser les [Push notifications](https://developers.google.com/web/ilt/pwa/introduction-to-push-notifications)

* ✔️ [Aurora Store](https://github.com/whyorean/AuroraStore): Catalogue alternatif d'applications provenants du PlayStore.
* ✔️ [MicroG](https://microg.org/): Permet aux applications faisant appel aux API propriétaires de Google de fonctionner sur les ROMs basées sur AOSP.

## Applications

* ✔️ [NewPipe](https://newpipe.net/) (Youtube)
* ✔️ [Frost](https://f-droid.org/en/packages/com.pitchedapps.frost/) (Facebook) 
* ✔️ [Infinity](https://github.com/Docile-Alligator/Infinity-For-Reddit/) (Reddit) 


# Sécurité générale 

## Gestionnaires de mots de passe

### Local
* ✔️ [KeepassXC](https://keepassxc.org/): Fonctionne en local, plus sûr par design, mais pas de synchronisation inter appareils possible.

### En ligne
* ✔️ [Bitwarden](https://bitwarden.com/): (Rare) gestionnaire cloud open source, possibilité d'auto héberger.


	* ⚠️ Choisir d'intégrer le 2FA avec son gestionnaire de mots de passe constitue un risque de défaillance unique.
	
📝 L'une des qualités d'un gestionnaire de mots de passes est de copier/coller une entrée sans avoir a réveler le texte, réduisant une attaque type [keylogging](https://en.wikipedia.org/wiki/Keystroke_logging).


## 2FA (smartphone)

Le HOTP par SMS est mal sécurisé, le TOTP en revanche est fiable lorsqu'utilisé correctement.

* ✔️ [Aegis](https://getaegis.app/): Les mots de passe à usage unique sont stockés dans un **coffre-fort** (chiffré), l'option de sauvegardes automatiques est prise en charge. 


## VPN


// Ce sera pour une prochaine fois... 



# Conseils en vrac

À venir...
