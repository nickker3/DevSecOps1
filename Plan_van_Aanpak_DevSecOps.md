# 📋 Plan van Aanpak - DevSecOps Bouwstraat

**Datum:** 02-04-2025

## 🎯 Doel
Een volledig functionele DevSecOps-bouwstraat opzetten met een CI/CD-pipeline, versiebeheer, automatische deployment en optionele security- en monitoringcomponenten.

---

## 🧩 Projectonderdelen

### ✅ Verplichte onderdelen
1. **Self-hosted Gitea installatie**
2. **CI/CD pipeline met build- en deployfase (Drone CI of Gitea Actions)**
3. **Webapplicatie automatisch deployen na commit naar `main`**
4. **Opname van werkende pipeline**
5. **Configuratiebestanden (YAML, config)**
6. **Markdown-documentatie met bewijsstukken (screenshots, logs, configs)**

### ✳️ Optionele uitbreidingen (voor cijfer >6)
- SBOM (Software Bill of Materials)
- Monitoring (infra + app)
- Alerting
- Security tests (SAST, DAST, etc.)
- Load testing
- Roll-back opties
- Containerisatie
- ChatOps
- Fuzzing

---

## 🛠️ Stappenplan

### 1. **Voorbereiding**
- ✅ Repo aanmaken (bijv. GitHub/Gitea)          "https://www.github.com/nickker3/DevSecOps1 .git"
- ✅Webapplicatie kiezen (bijv. Node.js app)        "https://uptime.kuma.pet/"
- ✅Keuze maken voor CI/CD-tool                    "https://www.drone.io/"
- ISO/VM-voorbereiding

### 2. **VM(s) aanmaken**
- Script gebruiken (`Create_VM_HA.sh`)
- IP's, namen en SSH toegang configureren
- Testen of VMs correct starten

### 3. **Gitea installeren**
- Handmatig of via cloud-init
- Webinterface instellen (admin, database)
- Repositories beheren

### 4. **CI/CD inrichten**
- Build- en deploy-fase opzetten (Drone CI of Gitea Actions)
- Build = app bouwen
- Deploy = automatisch naar productie-VM

### 5. **Webapp hosten**
- Webapp kiezen en deployen op VM
- Zorg voor werkende webserver (bijv. nginx of direct via app)
- Pipeline moet push → build → deploy → live resultaat tonen

### 6. **Opname maken**
- Demonstratie opnemen van commit tot live app
- Backup voor als demo niet werkt

### 7. **Documentatie schrijven**
- Markdown-bestand aanmaken in repo
- Beschrijven van keuzes + implementatie per onderdeel
- Screenshots, configuratie en logs als bewijs
- ZIP van hele repo toevoegen aan BB

### 8. **Extra features (optioneel)**
- Monitoring met Prometheus + Grafana
- Alerting via webhook of mail
- Security scans (Trivy, Snyk, etc.)
- SBOM genereren met Syft

---

## 🗓️ Planning & Deadline
- Check oplevermoment op Blackboard
- Zorg dat alles (video, documentatie, configs) op tijd ingeleverd is

---

## 📦 Bestanden die ingeleverd worden
- Video opname van werkende pipeline
- Zip-bestand van de hele repository
- Markdown-documentatie met bewijsstukken

---

## 🔚 Eindresultaat
Een geautomatiseerde bouwstraat waar een commit leidt tot:
- Build
- Test
- Deploy
- Gehoste applicatie in productie
