# Bus Tracker – Processeur GTFS

Ce **processeur GTFS** permet de compiler une ou plusieurs ressources GTFS pour
en extraire la liste des courses en cours de réalisation.  
Ces données sontensuite envoyées au serveur Redis pour que l'application Bus
Tracker puisse les consommer.

## Mise en route

1. Installer les dépendances : `pnpm install`.
2. Démarrer les composants externes nécessaires : `docker compose up -d`.
3. Démarrer l'application : `pnpm start -- /chemin/vers/configuration.mjs`.

Un échantillon de configurations est mis à votre disposition sur ce dépôt.

## Observation

1. Se connecter au dashboard Redis (http://localhost:8001).
2. Accéder à l'onglet Pub/Sub (panneau de gauche – dernière icône).
3. Renseigner le pattern `journeys` puis cliquer sur Subscribe.

À ce stade, les éléments envoyés par le processeur devraient apparaitre.

## Licence

Voir [LICENSE](./LICENSE).
