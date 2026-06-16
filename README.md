# NetPractice

> 42 School project — Configure small TCP/IP networks (IP addresses, subnet masks and routes) so that every machine can talk to every other one.
>
> Projet de l'école 42 — Configurer de petits réseaux TCP/IP (adresses IP, masques de sous-réseau et routes) pour que chaque machine puisse communiquer avec les autres.

---

## 🇬🇧 English

### Principle

NetPractice is a **network configuration** project: there is no program to write or compile.
It is a series of online exercises in which you configure TCP/IP networks so that all the
hosts and routers in a small topology can reach each other. For each level you have to fill in
the right values for:

- **IP addresses** of interfaces,
- **subnet masks** (in dotted-decimal or CIDR form),
- **routing table entries** (destination + gateway).

A level is *valid* once every required connection in the diagram is established.

### What's in this repo

This repository archives the work for the project. At the moment it contains:

- `README.md` — this documentation.

The validated answers for each level (the exported configuration / answer files produced by
the online interface, typically one `.txt` per level — `level-1.txt`, `level-2.txt`, …, or
screenshots of the working topologies) are meant to live here as well. As they are added,
they will appear in this repository alongside this README.

> Note: the project is solved in a browser, so there are no source files, build artefacts or
> dependencies to track — only the exported configurations of the solved levels.

### How it works

NetPractice is **not a build-and-run project**. You do not clone and execute anything; instead:

1. You open the project's web interface provided by 42 and load each level.
2. You read the network diagram and figure out the addressing scheme.
3. You enter the IP addresses, masks and routes that make every link work.
4. You submit / export the configuration once the level is green.

This repository therefore acts as an **archive of the validated configurations** rather than a
runnable codebase. To verify or replay a level, you reload the corresponding configuration in
the NetPractice interface.

A subnet mask can be written either way:

```text
255.255.255.0   ==   /24
255.255.255.128 ==   /25
255.255.255.252 ==   /30
```

### What I learned

- **IPv4 addressing** — structure of an IPv4 address (network part vs host part).
- **Subnet masks & CIDR notation** — reading and computing masks in both `255.x` and `/n` forms.
- **Subnetting** — splitting an address block into smaller subnets and computing usable host ranges.
- **Gateways & routing tables** — default routes, static routes, choosing the right next hop.
- **Address classes** — classful ranges (A/B/C) and private vs public address space.
- **Network troubleshooting** — diagnosing why two hosts cannot reach each other (wrong mask,
  overlapping subnets, missing or incorrect route, gateway outside the subnet, etc.).

---

## 🇫🇷 Français

### Principe

NetPractice est un projet de **configuration réseau** : il n'y a aucun programme à écrire ni à
compiler. C'est une série d'exercices en ligne dans lesquels on configure des réseaux TCP/IP
afin que toutes les machines et tous les routeurs d'une petite topologie puissent communiquer.
Pour chaque niveau, il faut renseigner les bonnes valeurs de :

- **adresses IP** des interfaces,
- **masques de sous-réseau** (en notation décimale pointée ou CIDR),
- **entrées de table de routage** (destination + passerelle).

Un niveau est *validé* dès que toutes les connexions attendues du schéma sont établies.

### Contenu du dépôt

Ce dépôt archive le travail réalisé sur le projet. Il contient actuellement :

- `README.md` — cette documentation.

Les réponses validées de chaque niveau (les fichiers de configuration exportés depuis
l'interface en ligne, généralement un `.txt` par niveau — `level-1.txt`, `level-2.txt`, … —
ou des captures des topologies fonctionnelles) ont vocation à être archivées ici également.
Au fur et à mesure de leur ajout, elles apparaîtront dans ce dépôt aux côtés de ce README.

> Remarque : le projet se résout dans un navigateur ; il n'y a donc ni fichiers source, ni
> artefacts de compilation, ni dépendances à suivre — seulement les configurations exportées
> des niveaux résolus.

### Comment ça marche

NetPractice n'est **pas un projet à compiler et exécuter**. On ne clone rien pour le lancer ;
à la place :

1. On ouvre l'interface web du projet fournie par 42 et on charge chaque niveau.
2. On lit le schéma du réseau et on déduit le plan d'adressage.
3. On saisit les adresses IP, les masques et les routes qui font fonctionner chaque lien.
4. On soumet / exporte la configuration une fois le niveau validé (au vert).

Ce dépôt sert donc d'**archive des configurations validées** plutôt que de base de code
exécutable. Pour vérifier ou rejouer un niveau, on recharge la configuration correspondante
dans l'interface NetPractice.

Un masque de sous-réseau peut s'écrire des deux façons :

```text
255.255.255.0   ==   /24
255.255.255.128 ==   /25
255.255.255.252 ==   /30
```

### Ce que ça m'a apporté

- **Adressage IPv4** — structure d'une adresse IPv4 (partie réseau / partie hôte).
- **Masques de sous-réseau & CIDR** — lire et calculer les masques en `255.x` comme en `/n`.
- **Découpage en sous-réseaux** — diviser un bloc d'adresses et calculer les plages d'hôtes utilisables.
- **Passerelles & tables de routage** — routes par défaut, routes statiques, choix du bon saut suivant.
- **Classes d'adresses** — plages classful (A/B/C), adresses privées et publiques.
- **Dépannage réseau** — diagnostiquer pourquoi deux machines ne se joignent pas (mauvais masque,
  sous-réseaux qui se chevauchent, route manquante ou erronée, passerelle hors du sous-réseau, etc.).
