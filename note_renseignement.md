# NOTE DE RENSEIGNEMENT

## Analyse de Campagne de Désinformation - Projet Éolien Offshore Loire-Atlantique

**Mention de protection** : NON PROTEGE
**Référence** : NP-2025-001-EOLIEN-LOIRE
**Date** : 2 janvier 2025
**Analyste** : L. Matthews
**Destinataire** : Direction Cybersécurité & Sûreté

---

## RÉSUMÉ EXÉCUTIF (Executive Summary)

Ce rapport fait suite à la menace posée par une compagne de désinformation (fausses informations propagées de manière volontaires) visant le projet éolien offshore Loire-Atlantique. L’impact, qui reste difficile à estimer précisément, peut être estimée à partir de l’engagement important généré par les posts, bien que ce dernier soit probablement majoritairement artificiel.

---

## SYNTHÈSE DES INDICATEURS

### Données collectées

- **Période d'observation** : 15-20 janvier 2024 (7 jours)
- **Plateformes** : Twitter, Facebook, sites web
- **Volume** : 96 tweets, 40 posts FB, 55 textes, ~30 images
- **Portée estimée** : Les comptes suspects ont étés identifiés comme étant ceux faisant partie des clusters 0 et 2 identifiés sur Gephi. Ils regroupent AlerteVerite2024, InfoPatriote_FR, Verite_Environnement, AlerteCitoyenne_Info, InfoLiberte_FR, Resistance_Nationale, Patriote_Ouest, InformationNationale, MediaCitoyen_Info, VeriteReseaux, AlerteMedias_FR, Reveil_National, CoordinationPatriote, LiberteSansCensure, ComplotVerite. Collectivement, ils possèdent $3421+2876+4123+5234+3876+4567+34214234+4876+3654+3987+4123+4567+3234+2987=34.265.759$, mais ceux-ci ne sont pas forcément distincts.

### Indicateurs de Coordinated Inauthentic Behavior (CIB)

| Indicateur | Valeur | Seuil suspect | Verdict |
|-----------|--------|---------------|---------|
| Clusters D3lta (duplication) | 5 clusters | >2 | ⚠ ALERTE |
| Comptes créés <30j | 50% | >40% | ⚠ ALERTE |
| Densité réseau cluster max | 0.833 | >0.65 | ⚠ ALERTE |
| Images IA-générées (PeREN >0.7) | 1/7 | >10% | ⚠ ALERTE |
| Textes signature LLM | 12,9% | >20% | ⚠ OK |
**Conclusion** : Le nombre important de critères inquiétants (images générées par IA, réseaux à densité anormale, comptes créés peu de temps avant la campagne, et clusters D3lta dupliquant du contenu) nous permettent d’affirmer avec une certaine confiance la présence de CIB à une échelle importante.

---

## ANALYSE DES ACTEURS

### Clusters de coordination identifiés

**CLUSTER 0** (Densité réseau : 0.75)

**CLUSTER 2** (Densité réseau : 0.833)

### Comptes à haute influence (Top 5 betweenness centrality)

Le top 5 des comptes à haute influence **qui appartiennent au cluster 0 ou 2 UNIQUEMENT** sont :

1. **AlerteVerite2024** - Degré : 15, Betweenness : 206
2. **InfoPatriote_FR** - Degré : 12, Betweenness : 176
3. **Verite_Environnement** - Degré : 16, Betweenness : 68
4. **VeriteReseaux** - Degré : 14, Betweenness : 37
5. **MediaCitoyen_Info** - Degré : 15, Betweenness : 33

---

## ANALYSE DES NARRATIFS

### Topic Modeling (BERTopic)

**Narratifs identifiés** :

| Topic ID | Label | Mots-clés principaux |
|----------|-------|----------------------|
| 0 | 0_offshore_marine_éolien offshore_publiques | offshore, marine, éolien offshore, publiques, rapport, débat, publique, pêche, enquête publique, projet |
| 1 | 1_éolien destructeur_révèle_projet éolien_preuves | révèle, projet éolien, preuves, rapport, détruire, sommes, projet, littoral, massivement |

**Narratif dominant de désinformation** : [Décrire le topic principal suspect]

### Techniques DISARM identifiées

| Technique DISARM | Description | Preuves observées |
|-----------------|-------------|-------------------|
| **T001 – Amplification coordonnée** | Diffusion massive et synchronisée d’un même message ou narratif | Clusters 0 et 2 très denses (>0.75), duplication de contenus (clusters D3lta) |
| **T002 – Exploitation de griefs légitimes** | Instrumentalisation de préoccupations réelles (écologie, pêche) | Narratifs centrés sur la biodiversité, les pêcheurs, le littoral |
| **T004 – Appel à l’émotion** | Utilisation de peur, colère ou indignation pour mobiliser | Ton alarmiste (« scandale », « destruction », « trahison ») |
| **T006 – Défiance envers les autorités** | Discrédit des institutions et des médias traditionnels | Accusations de censure, de collusion État-médias |
| **T008 – Faux experts / fausses preuves** | Références à des rapports « confidentiels » ou sources invérifiables | Mentions de documents secrets jamais publiés |
| **T012 – Illusion de consensus populaire** | Présentation artificielle d’un large soutien citoyen | Réplication massive des mêmes messages via comptes récents |

**Référence** : [DISARM Framework]
(https://github.com/DISARMFoundation/DISARMframeworks)

---

## IMPACT ET RISQUES

### Risques d'impact

- **Comptes exposés** : 34.265.759 (Ce ne sont pas forcément des comptes uniques.)
- **Viralité** : Environ 41 engagement par post
- **Impressions estimées** :   ≈ 41 × 96 tweets × facteur viralité conservateur (×10) **≈ 39.360 impressions directes**, hors rediffusion algorithmique

### Risques identifiés

- **Risque informationnel**  
  Dégradation de la qualité du débat public par diffusion de fausses informations et récits trompeurs.

- **Risque réputationnel**  
  Atteinte à l’image des acteurs institutionnels (préfecture, collectivités, experts scientifiques).

- **Risque sociétal**  
  Polarisation accrue de la population locale, radicalisation des positions et tensions sociales.

- **Risque sécuritaire indirect**  
  Mobilisations physiques déclenchées sur la base de fausses informations (manifestations, blocages).

- **Risque stratégique**  
  Fragilisation de l’acceptabilité sociale des projets de transition énergétique futurs.

## PLAN D'ACTIONS

### Court terme (0–30 jours)

- Activer une **veille renforcée** sur les clusters 0 et 2
- Signaler les contenus les plus viraux aux plateformes (CIB, manipulation)
- Publier une **communication factuelle ciblée** (FAQ, données vérifiées)
- Mobiliser des **sources crédibles (experts, scientifiques)** pour contre-discours

### Moyen terme (1–3 mois)

- Déployer un **contre-narratif structuré** basé sur les faits vérifiés
- Coopérer avec des acteurs tiers (médias, ONG, chercheurs)
- Mettre en place un **tableau de bord CIB** (réseaux, duplication, temporalité)

### Long terme (>3 mois)

- Renforcer la **résilience informationnelle** (transparence, open data)
- Former les équipes à la **détection de campagnes de désinformation**
- Capitaliser sur les signaux DISARM pour anticiper les campagnes futures

## RESSOURCES COMPLÉMENTAIRES

### Documentation officielle

- **DISARM Framework** : https://disarmfoundation.github.io/disarm-navigator/
- **D3lta (VIGINUM)** : https://github.com/VIGINUM-FR/D3lta
- **GEPHI Tutorials** : https://gephi.org/users/
- **BERTopic Docs** : https://maartengr.github.io/BERTopic/

### Rapports de référence

- VIGINUM Rapports publics : https://www.sgdsn.gouv.fr/publications?
field_type_target_id%5B182%5D=182
- DFRLab (Atlantic Council) : https://www.atlanticcouncil.org/programs/digitalforensic-research-lab/
---
**ESILV - Social listening & cognitive warfare**
*Document pédagogique - Utilisation autorisée dans cadre académique uniquement*
---
![ESILV Logo](Charte%20graphique/logo%20ESILV%20b%26r.webp)