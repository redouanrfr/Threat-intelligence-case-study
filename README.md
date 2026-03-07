# 🛡️ Threat Intelligence Case Study
### Corrélation APT & Belt and Road Initiative — Infrastructure Critique Française (2016–2023)

**Threat Intelligence & Analyse**
![CTI](https://img.shields.io/badge/CTI-Cyber%20Threat%20Intelligence-red)
![OSINT](https://img.shields.io/badge/OSINT%20%2F%20HUMINT-darkblue)
![Threat Hunting](https://img.shields.io/badge/Threat-Hunting-orange)
![MITRE ATT&CK](https://img.shields.io/badge/MITRE-ATT%26CK-red)
![APT Profiling](https://img.shields.io/badge/APT-Profiling-darkred)
![Malware Analysis](https://img.shields.io/badge/Malware-Analysis-black)
![Geopolitical Correlation](https://img.shields.io/badge/Géopolitique-BRI%20Correlation-purple)

**Réseau & Sécurité Périmétrique**
![Cisco ASA](https://img.shields.io/badge/Cisco-ASA%20%7C%20IPS-blue)
![Firewall](https://img.shields.io/badge/Firewall-PfSense%20%7C%20Shorewall-blue)
![Architecture](https://img.shields.io/badge/Architecture-Full%20Mesh%20Multi--DC-blue)
![HA](https://img.shields.io/badge/Haute-Disponibilité-blue)
![Segmentation](https://img.shields.io/badge/Segmentation-DMZ%20%7C%20VLAN-blue)
![Reverse Proxy](https://img.shields.io/badge/Reverse%20Proxy-SSL%20Termination-blue)
![VPN](https://img.shields.io/badge/VPN-IKE-blue)

**Hardening Système**
![Apache](https://img.shields.io/badge/Hardening-Apache%20%7C%20Nginx-green)
![SSH](https://img.shields.io/badge/Hardening-SSH%20%7C%20SFTP-green)
![Physical](https://img.shields.io/badge/Physical%20Resource-Constraining-green)
![Least Privilege](https://img.shields.io/badge/Least-Privilege-green)

**Monitoring & Détection**
![Logs](https://img.shields.io/badge/Logs-Syslogs%20%7C%20Apache%20%7C%20Auth-yellow)
![Nagios](https://img.shields.io/badge/Monitoring-Nagios%20%7C%20Zabbix%20%7C%20Cacti-yellow)
![Snort](https://img.shields.io/badge/HIDS-Snort-yellow)
![OOB](https://img.shields.io/badge/Out--of--Band-Alerting%20GPRS-yellow)

**Analyse & Renseignement**
![TRACFIN](https://img.shields.io/badge/Corrélation-TRACFIN%20%7C%20Douanes-lightgrey)
![Supply Chain](https://img.shields.io/badge/Supply%20Chain-Analysis-lightgrey)
![Risk](https://img.shields.io/badge/Risk-Management-lightgrey)
![IR](https://img.shields.io/badge/Incident-Response-lightgrey)

![License](https://img.shields.io/badge/License-CC%20BY--NC--ND%204.0-lightgrey)
![Period](https://img.shields.io/badge/Period-2012--2023-blue)

> *"L'adversaire n'a plus d'autre choix que de mobiliser ses ressources les plus coûteuses. Et il va le faire."*

---

## Vue d'ensemble

**~40 milliards d'euros protégés. 7 ans de traque. Zéro brèche.**

Ce dépôt documente une investigation CTI menée de 2016 à 2023 sur une infrastructure critique nationale de compensation (titres-restaurant) traitant **~6 Mds€ de transactions annuelles** et **100% du marché français papier**.

Ce n'est pas un CTF. Ce n'est pas un lab. C'est du **terrain réel**, face à des adversaires de niveau APT.

---

## 🎯 Contexte — L'Actif sous Attaque

| Dimension                        | Données                        |
|:---------------------------------|:-------------------------------|
| 💰 Flux annuels traités          | ~6 milliards €                 |
| 🏢 Établissements affiliés       | ~180 000                       |
| 🎫 Titres traités/an             | ~750 millions                  |
| 🇫🇷 Part de marché                 | 100% du marché français papier |
| ⏱️ Durée de la campagne adverse  | 7 ans (2016–2023) *            |

> \* Veille OSINT & géopolitique initiée dès 2011 (guerre 5G, BRI) — soit ~12 ans de surveillance continue.

---

## 🧠 Ce que ce document démontre

### 1. 🕵️ Intelligence avant la signature
Détection de signaux faibles **avant** toute signature connue, par corrélation de syslogs, Apache access/error logs, auth.log et Awstat. Identification d'un **pattern géographique systématique** révélateur d'une mission ciblée, non d'un bruit de fond automatisé.

> *Un robot s'arrête au blocage. Un soldat cherche une autre porte.*

### 2. 🗺️ Corrélation APT × Belt and Road Initiative
Toutes les sources d'attaque — Russie, Kazakhstan, Kenya, Éthiopie, Djibouti, Tanzania, Rwanda, Madagascar, Mozambique, Ouganda, Burundi — **sont partenaires ou relais de la BRI**. La chronologie des pics d'attaques coïncide précisément avec les phases d'expansion du projet lancé par la Chine en 2013.

### 3. 🏗️ Architecture Anti-Fragile comme arme défensive
Conception d'une infrastructure **Full Mesh Multi-Datacenter** qui brise la rentabilité économique de l'attaquant. Chaque couche (Firewall → IPS → Reverse Proxy → Segmentation → Endpoint), complétée par une contrainte physique et du hardening.

### 4. 📦 Preuve Cyber-Physique — Le Fil d'Ariane
La force de cette analyse : **le cyber se confirme dans le physique**.
- Identification d'une infrastructure de blanchiment via presse + rapports TRACFIN (2013–2015)
- Saisies douanières de faux titres-restaurant : de 10 512 unités en 2013 à un **record de 66 kg / 59 031 titres** en 2025 infrastructure de cash-out.
- ×6 en quantité, ×5 en valeur sur 12 ans → **production industrielle persistante**

> *De 2013 (TRACFIN) à 2026 (payloads FUD encore actifs) : 13 ans de convergence cyber-physique documentée — par le défenseur terrain lui-même, à partir de données réelles.*

### 5. 🦠 Capture de Payloads FUD
Documentation de charges utiles **Fully UnDetectable**, restées furtives de **2020 jusqu'en 2026**, compatibles avec les TTPs d'acteurs APT — confirmé via MITRE ATT&CK et vendors CTI (Mandiant, FireEye, Microsoft, Sekoia, ANSSI).

---

## 🔬 Approche Méthodologique

```
OSINT + HUMINT
     ↓
Corrélation géopolitique (BRI, guerre 5G, TRACFIN)
     ↓
Pattern analysis (logs → comportement → intention)
     ↓
Hypothèse de travail structurée (5 critères)
     ↓
Validation physique (saisies douanières, procédures judiciaires)
     ↓
Mapping MITRE ATT&CK + confirmation vendors CTI
```

**5 critères d'attribution :**
- ✅ Mobile économique sur ~6 Mds€
- ✅ Infrastructure logistique vers la France
- ✅ Connaissance approfondie du système ciblé
- ✅ Capacité opérationnelle sur 6+ ans (ressources durables)
- ✅ Réseau de blanchiment documenté

---

## ⚔️ Quelques attaques & interceptions documentées

| Période     | Vecteur                          | Cible              | Réponse                      | Résultat                  |
|:------------|:---------------------------------|:-------------------|:-----------------------------|:--------------------------|
| 2016        | DoS discret (Slowloris)          | Serveurs Web       | Hardening + limite sessions/IP | Arrêt des crashs        |
| 2016–17     | Exploitation (Struts/Traversal)  | Infrastructure Web | IPS + console de mgmt        | Détection pré-signature   |
| 2017–18     | DDoS Volumétrique + failles IKE  | Firewall           | HA + Patching critique       | Résilience continue       |
| 2020–2026   | Payloads FUD                     | Endpoints          | Analyse forensique + CTI     | Capture & documentation   |

---

## 📐 Principes Défensifs Appliqués

- **Defense in Depth** — 5 couches, zéro confiance transitive entre zones (Firewall → IPS → Reverse Proxy → Segmentation → Endpoint)
- **Rupture protocolaire** — Chaque saut impose une terminaison/réinitialisation de connexion
- **Hardening chirurgical** — Serveurs Web, SFTP/SSH, applicatifs (Linux Magazine, MISC, ANSSI, CIS Benchmarks)
- **Physical Resource Constraining** — Asphyxie physique comme vecteur défensif (2 Go de stockage = attaquant sans espace pour compiler ses kits)
- **Monitoring multi-sources** — Temps de réponse < 60 secondes (alerte → isolement → confinement)
- **Out-of-band alerting** — Modem GPRS sur console de monitoring, hors de portée de l'attaquant

> \* Veille technologique active et continue — dont **Cisco Live 2018** (Barcelone, janvier-février 2018) et **Threat Hunting Workshop** (Cisco/Firefly, Issy-les-Moulineaux, juillet 2018) — intégrée tout au long de la démarche défensive.

---

## 📊 RETEX — L'Équation Qui Change Tout

| Approche                  | Coût de réaction               | Impact               |
|:--------------------------|:-------------------------------|:---------------------|
| Détection < 60s           | Quelques centaines d'euros     | Incident mineur      |
| Détection tardive         | Centaines de milliers d'euros  | Paralysie prolongée  |
| Absence de résilience     | Millions (impact boursier)     | Risque systémique    |

> Pour une infrastructure traitant plusieurs milliards d'euros annuels, l'arrêt prolongé n'est pas une option. C'est un risque systémique national.

---

## 📁 Contenu du Dépôt

```
📄 CTI_APT_BRI_Infrastructure_Critique_2016-2023.md   ← Synthèse stratégique (version publique)
📁 [pdf/](./pdf/)                                      ← Sources : presse, TRACFIN, rapports officiels, vendors CTI
```

> 📌 **La version intégrale** (détails techniques, IoCs, analyse TTPs complète) est disponible **sur demande**.

---

## ⚠️ Avertissement légal

Ce document est une **analyse rétrospective à finalité strictement pédagogique** d'une infrastructure n'existant plus (entité dissoute le 30/06/2023).

- Aucune attribution formelle à un État ou groupe spécifique
- Toutes les informations proviennent de **sources publiques exclusivement**
- Les rapprochements APT sont fondés sur des similarités de TTPs publiées — non une attribution judiciaire
- Aucun secret d'entreprise, donnée client ou configuration interne n'est divulgué

📜 **Licence : CC BY-NC-ND 4.0**

---

## 👤 Auteur

**Redouane R** — *Field-Hardened*
Infrastructure Critique Nationale · 2012–2023 · ~40 Mds€ protégés

> *"En sécurité, le sommet n'est qu'un plateau avant la prochaine escalade."*

---

*Ce dépôt illustre une expertise individuelle acquise sur le terrain, sans outil magique ni budget illimité — juste de la rigueur, de l'anticipation, et une conviction que la sécurité se construit avant l'incident.*
