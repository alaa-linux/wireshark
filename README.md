# 🔍 Network Sniffing avec Wireshark

## 📌 Description du projet

Ce projet a pour objectif de découvrir et d’utiliser un analyseur réseau : **Wireshark**.

Il s’agit d’une initiation pratique à :

* l’analyse du trafic réseau
* la compréhension du modèle OSI
* l’étude des principaux protocoles (ARP, TCP, UDP, DNS, DHCP, etc.)

Le projet a été réalisé dans un environnement Linux avec des machines virtuelles en réseau local.

---

## 🎯 Objectifs

* Capturer et analyser des paquets réseau
* Comprendre les couches du modèle OSI
* Identifier les protocoles réseau
* Utiliser les filtres Wireshark
* Interpréter les trames en détail
* Comprendre les mécanismes de communication réseau

---

## 🧠 Notions importantes

### 🔹 Différence entre trame et paquet

* **Trame** → couche 2 (liaison de données), contient MAC + FCS
* **Paquet** → couche 3 (réseau), contient IP + protocole

👉 Une trame encapsule un paquet lors de la transmission réseau.

---

### 🔹 Format PCAP / PCAPNG

* **PCAP** → format standard de capture réseau
* **PCAPNG** → version améliorée avec plus d’informations (interfaces, métadonnées…)

---

## 🌐 Analyse des protocoles

### 🟡 ARP

* Résolution IP → MAC
* Utilisation du broadcast

### 🔵 UDP

* Protocole rapide sans connexion
* Utilisé pour DNS, DHCP, etc.

### 🔴 TCP

* Connexion fiable (3 étapes)

#### 🔁 Handshake TCP

```
Client → SYN → Serveur
Serveur → SYN-ACK → Client
Client → ACK → Serveur
```

---

## 🧪 Environnement de test

* Réseau local (LAN)
* Machines virtuelles
* Services installés :

  * FTP
  * SSH
  * DNS
  * DHCP
  * SMB
  * HTTP / HTTPS

---

## 🎯 Filtres Wireshark utilisés

```
icmp or (udp port 67 or udp port 68) or port 53 or udp port 5353 or port 6500 or port 443 or port 21 or port 20 or tcp port 445 or tcp port 139 or tcp port 22 or http or port 10000
```

---

## 📊 Analyse des protocoles

### 🟢 ICMP (Ping)

* Vérification de connectivité
* Analyse des temps de réponse

### 🟡 DHCP

* Attribution d’adresse IP
* Communication client ↔ serveur

### 🔵 DNS

* Résolution de noms de domaine
* Exemple : échec de résolution DNS

### 🟣 mDNS

* Découverte de services locaux
* Multicast (224.0.0.251)

### 🟠 SMB

* Partage de fichiers réseau

---

## 🔐 Sécurité réseau

### ❌ FTP (non sécurisé)

* Identifiants visibles en clair
* Risque élevé

### ✅ HTTPS / TLS

* Données chiffrées
* Sécurité renforcée

---

## 🧰 Outils utilisés

* Wireshark
* Tshark
* Linux (WSL / VM)
* Réseau virtualisé

---

## 🚀 Commandes utiles

### Capture avec tshark

```
tshark -i eth0 -f "port 53"
```

---

## 📈 Compétences développées

* Analyse réseau
* Administration système
* Sécurité informatique
* Compréhension des protocoles
* Diagnostic réseau

---

## 📌 Conclusion

Ce projet m’a permis de comprendre en profondeur :

* le fonctionnement des réseaux
* les protocoles essentiels
* l’importance de la sécurité (chiffrement vs non sécurisé)

Il constitue une base solide pour la cybersécurité et le DevOps.

---

## 👨‍💻 Auteur

**Alaa Kaid Ahmed**
