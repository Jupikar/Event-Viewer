# Vue personnalisée pour la surveillance des événements DNS
## Description

Ce projet contient une vue personnalisée pour l'Event Viewer de Windows Server, conçue spécifiquement pour surveiller les événements liés au rôle DNS. Cette vue permet aux administrateurs système de suivre facilement les événements critiques, les erreurs, les avertissements et les informations concernant le service DNS et son état.

La vue est configurée pour inclure des événements provenant des sources DNS-Server-Service (opérations du serveur DNS) et DNS Client Events (événements côté client). Elle cible des ID d'événements spécifiques pour identifier les démarrages, arrêts, erreurs de résolution, échecs de chargement de zones et problèmes de réplication DNS.

---

### Critères de la vue personnalisée

- Niveaux surveillés :

Critique (1)

Erreur (2)

Avertissement (3)

Information (4) (uniquement pour les démarrages et arrêts)

- Sources d'événements incluses :

DNS-Server-Service

DNS Client Events

- ID d'événements surveillés :

2 : Démarrage du serveur DNS

4 : Arrêt du serveur DNS

409 : Erreur de résolution de nom

501-502 : Échec de chargement de zone

6001-6002 : Problèmes de réplication DNS

---

### Fichier inclus

Logs-DNS.xml : Fichier XML exporté de l'Event Viewer contenant la configuration de la vue personnalisée.

Instructions d'importation

Ouvrez l'Event Viewer sur votre machine Windows Server.

Faites un clic droit sur Vues personnalisées dans le panneau de gauche, puis sélectionnez Importer une vue....

Sélectionnez le fichier Logs-DNS.xml fourni dans ce dépôt.

La vue sera ajoutée sous un nom descriptif, tel que Surveillance DNS - Vue personnalisée.

---

### Utilisation

Une fois la vue importée, vous pourrez :

Visualiser les événements DNS critiques, erreurs, avertissements et informations dans un seul emplacement.

Identifier rapidement les problèmes liés au service DNS, comme les échecs de résolution de noms ou les problèmes de réplication.

Surveiller les démarrages et arrêts du service DNS pour des besoins de diagnostic ou d'audit.


Contributeurs

Créé par [Jupikar]
