# Data cleaning

En prenant les données issues du `data/raw/baie_somme_2025.xlsx` :

- Nettoyage et harmonisation des noms de lieux (résidence et lieu d'entretien)
- Nettoyage et harmonisation des réponses relatives aux populations de phoque :
  - Harmonisation de l'estimation numérique de la population : données chiffrées et catégorielles (non chiffré mais estimation par niveaux ("peu", "beaucoup"))
  - Harmonisation des réponses relatives à la connaissance de la population
- One hot encoding des réponses aux questions à choix multiples sur le statut des phoques et 
- Enregistrement des données nettoyées `data/processed/data_cleaned.xlsx`

## Dictionnaire des variables

### Variables Démographiques

- `date` : Horodatage de la réponse (Format : AAAA/MM/JJ HH:MM:SS)
- `genre` : Genre du répondant (Valeurs : Homme, Femme)
- `classe_age` : Tranche d'âge (Valeurs : 20-35 ans, 35-50 ans, 50-65 ans, >65 ans)
- `lieu` : Lieu de l'enquête (Valeurs : Pointe du Hourdel, Saint-Valery-sur-Somme, Le Crotoy, Amiens)
- `residence` : Lieu de résidence du répondant (Valeurs : diverses villes et départements)
- `professions` : Catégorie socioprofessionnelle (Valeurs : Employé.e, Retraité.e, Artisans/commerçants/chefs d'entreprise, Restauration/hôtellerie, Ouvrier, Cadres et professions intellectuelles supérieures, Professions intermédiaires)

### Variables de Population de Phoques

- `pop_yes_no` : Indicateur de présence de phoques (Valeurs : VRAI, FAUX)
- `pop_max` : Estimation maximale de la population (Valeurs : Numérique, "Non", "Beaucoup")
- `phoque_noms` : Connaissance des noms de phoques (Valeurs : "Non", "Oui", "partiel : Veau-marin", "Phoque gris")

### Perception des Phoques (Binaire : 0/1)

- `phoque_paisible` : Perception des phoques comme paisibles
- `phoque_invasive` : Perception des phoques comme invasifs
- `phoque_concurrent` : Perception des phoques comme concurrents
- `phoque_menacee` : Perception des phoques comme menacés
- `phoque_prédateur` : Perception des phoques comme prédateurs

### Questions de Gestion (Binaire : 0/1)

- `q_nature_libre` : Opinion sur la liberté de la nature
- `q_surfréquentation` : Problématique de surfréquentation
- `q_conflits` : Existence de conflits
- `q_patrimoine` : Valeur patrimoniale
- `q_trop_veau` : Opinion sur le nombre de veaux marins
- `q_trop_gris` : Opinion sur le nombre de phoques gris
- `q_pas_plus_phoques` : Opposition à l'augmentation du nombre de phoques
- `q_trop_poisson` : Impact sur les ressources halieutiques
- `q_opportunité_économique` : Potentiel économique
- `q_menace_économique` : Risque économique
- `q_groupe_travail` : Soutien à un groupe de travail
- `q_panneaux` : Soutien aux panneaux d'information
- `q_barrières` : Soutien à l'installation de barrières
- `q_centre_information` : Soutien à un centre d'information
- `q_menace_tradition` : Perception comme menace pour les traditions

### Activités Pratiquées (Binaire : 0/1)

- `pêche` : Pêche
- `chasse` : Chasse
- `voile` : Voile
- `vélo` : Vélo
- `natation` : Natation
- `planceàvoile` : Planche à voile
- `paddle` : Paddle
- `kayak/canoë` : Kayak/Canoë
- `kitesurf` : Kitesurf
- `equitation` : Équitation
- `wingfoil` : Wingfoil
- `promenade` : Promenade
- `marche` : Marche
- `naturaliste` : Activités naturalistes
- `Autre` : Autres activités (Valeurs : 0, 1, 2)