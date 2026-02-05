# Dashboard Criminalité - Centre-Val de Loire

Dashboard interactif d'analyse des données de criminalité en région Centre-Val de Loire, confrontées au sentiment d'insécurité national.

## Objectif

Ce dashboard permet de visualiser l'évolution réelle de la criminalité enregistrée par les forces de l'ordre, et de la comparer au sentiment d'insécurité ressenti par la population française. L'objectif est de fournir une analyse factuelle basée sur les données officielles, pour permettre à chacun de se faire sa propre opinion au-delà des discours politiques.

## Données utilisées

### Criminalité enregistrée

**Source**: [SSMSI - Service Statistique Ministériel de la Sécurité Intérieure](https://www.interieur.gouv.fr/Interstats)

**Dataset**: Base des séries chronologiques - disponible sur [data.gouv.fr](https://www.data.gouv.fr/datasets/service-statistique-ministeriel-de-la-securite-interieure-base-des-series-chronologiques)

**Période**: 2016-2024

**Périmètre géographique**: Région Centre-Val de Loire (6 départements)

| Code | Département | Population (INSEE 2024) |
|------|-------------|------------------------|
| 18 | Cher | 302 306 |
| 28 | Eure-et-Loir | 439 042 |
| 36 | Indre | 218 263 |
| 37 | Indre-et-Loire | 612 061 |
| 41 | Loir-et-Cher | 329 470 |
| 45 | Loiret | 684 395 |
| **Total** | | **2 585 537** |

### Indicateurs de criminalité

| Indicateur | Catégorie | Description |
|------------|-----------|-------------|
| Homicides | Atteintes aux personnes | Homicides volontaires enregistrés |
| Tentatives d'homicide | Atteintes aux personnes | Tentatives d'homicide enregistrées |
| Violences | Atteintes aux personnes | Violences physiques (intra/extra familiales) |
| Vols avec armes | Vols violents | Vols commis avec une arme |
| Vols violents sans arme | Vols violents | Vols avec violence mais sans arme |
| Cambriolages | Atteintes aux biens | Cambriolages de résidences principales et secondaires |
| Vols de véhicules | Atteintes aux biens | Vols de véhicules motorisés |
| Vols dans véhicules | Atteintes aux biens | Vols à l'intérieur des véhicules |
| Vols d'accessoires | Atteintes aux biens | Vols d'accessoires sur véhicules |
| Usage de stupéfiants | Stupéfiants | Infractions pour usage de stupéfiants |
| Trafic de stupéfiants | Stupéfiants | Infractions pour trafic de stupéfiants |

### Sentiment d'insécurité

**Sources**:
- Enquête CVS (Cadre de Vie et Sécurité) 2007-2021 - [data.gouv.fr](https://www.data.gouv.fr/datasets/indicateurs-annuels-de-la-victimation-et-du-sentiment-dinsecurite-issus-des-enquetes-cadre-de-vie-et-securite)
- Enquête VRS (Vécu et Ressenti en matière de Sécurité) 2022-2024 - [Rapport SSMSI](https://www.interieur.gouv.fr/Interstats/Actualites/Vecu-et-ressenti-en-matiere-de-securite-Victimation-delinquance-et-sentiment-d-insecurite-Rapport-d-enquete-edition-2024)

**Indicateurs**:
- Sentiment d'insécurité dans le quartier/village (% population 14+)
- Sentiment d'insécurité au domicile (% population 14+)

**Note**: Les données 2022-2024 sont des estimations basées sur les taux de croissance publiés par le SSMSI (+15%/an). L'enquête 2020 n'a pas eu lieu (COVID-19).

**Périmètre**: France métropolitaine (données nationales uniquement)

## Fonctionnalités du dashboard

### Visualisations

- **Evolution temporelle**: Graphique interactif avec deux modes:
  - *Valeurs*: Nombres bruts de faits enregistrés
  - *Variation (%)*: Pourcentage d'évolution depuis 2016

- **Cartes par indicateur**: Mini-graphiques avec moyenne annuelle et tendance

- **Analyse statistique**: Pour chaque indicateur sélectionné:
  - Moyenne, écart-type
  - Coefficient de variation
  - Skewness, Kurtosis
  - R² de la tendance linéaire
  - Test de significativité (p-value)

- **Tendances**: Graphique en barres des évolutions moyennes par an

- **Comparaison Perception/Réalité**:
  - Evolution du sentiment d'insécurité national
  - Confrontation avec les infractions enregistrées
  - Bilan comparatif 2016-2024

- **Tableau détaillé**: Données complètes avec population et taux pour 1000 habitants

### Interactivité

- Sélection multiple de départements
- Sélection multiple d'indicateurs
- Filtrage par catégorie (Personnes, Biens, Stupéfiants)
- Export possible des visualisations (clic droit sur les graphiques)

## Limites et précautions

1. **Chiffre noir**: Les statistiques ne représentent que les infractions *enregistrées* par les forces de l'ordre. De nombreux faits ne sont jamais déclarés (notamment violences intra-familiales, agressions sexuelles).

2. **Petits effectifs**: Pour certains indicateurs (homicides), les variations peuvent être dues à quelques cas seulement.

3. **Données de sentiment nationales**: Les enquêtes CVS/VRS ne fournissent pas de déclinaison régionale du sentiment d'insécurité. La comparaison avec les données régionales de criminalité est donc indicative.

4. **Estimations VRS**: Les données de sentiment 2022-2024 sont des estimations basées sur les taux de croissance publiés, pas des chiffres officiels.

5. **Analyse descriptive**: Ce dashboard présente des statistiques descriptives. Aucune relation de causalité ne peut être établie.

## Technologies

- HTML/CSS/JavaScript vanilla
- [Plotly.js](https://plotly.com/javascript/) pour les visualisations
- Données pré-calculées en JSON (généré via Python/Pandas)

## Licence

Les données sources sont sous [Licence Ouverte 2.0](https://www.etalab.gouv.fr/licence-ouverte-open-licence/) (Etalab).

Le code de ce dashboard est libre de droits.

## Auteur

Dashboard créé pour l'analyse factuelle des données publiques de sécurité.
