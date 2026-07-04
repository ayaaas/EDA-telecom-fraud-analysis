# Analyse Exploratoire des Données (EDA) d’un Système de Détection de Fraude Télécom

# 1. Résumé Exécutif et Cadrage du Projet

L'objectif de cette analyse est de disséquer un jeu de données composé de **10 000 enregistrements téléphoniques** afin d'en extraire la « signature » des comportements frauduleux. Contrairement aux idées reçues, la fraude identifiée dans ce jeu de données n'est pas artisanale ou subtile ; elle est **industrielle, automatisée et hautement prévisible**.

À travers une démarche d'Analyse Exploratoire des Données (**Exploratory Data Analysis – EDA**), cette étude vise à comprendre la structure des données, à identifier les caractéristiques discriminantes des comportements frauduleux et à évaluer la faisabilité d'un futur modèle de Machine Learning dédié à la détection automatique de la fraude.

L'analyse des différents indicateurs statistiques et graphiques montre qu'une combinaison intelligente de critères comportementaux, temporels et relationnels (graphes) permet d'isoler les appels frauduleux avec une efficacité quasi chirurgicale tout en protégeant les clients professionnels légitimes présentant un volume d'activité élevé.

---

# 2. Introduction

L'Analyse Exploratoire des Données (**EDA – Exploratory Data Analysis**) constitue l'une des étapes fondamentales de tout projet de Data Science. Avant d'entraîner un modèle de Machine Learning, il est indispensable de comprendre les données, leur qualité, leur structure ainsi que les relations qui existent entre les différentes variables.

Dans le contexte de la détection de fraude télécom, cette étape est encore plus critique. Un système de détection performant ne repose pas uniquement sur un algorithme puissant ; il dépend avant tout d'une compréhension approfondie des comportements des utilisateurs légitimes et des fraudeurs.

L'EDA permet ainsi :

- d'identifier les tendances ;
- de détecter les anomalies ;
- de mesurer les corrélations entre les variables ;
- de vérifier que les données contiennent suffisamment d'information pour permettre une séparation efficace entre les différentes classes.

Cette étude constitue donc le diagnostic préalable indispensable avant toute phase de nettoyage des données (**Data Cleaning**), de création de nouvelles variables (**Feature Engineering**) ou d'entraînement d'un modèle prédictif.

---

# 3. Objectifs de l'Analyse Exploratoire des Données (EDA)

## 3.1 Objectif Général de l'EDA (Approche Théorique)

L'EDA (**Exploratory Data Analysis**), ou Analyse Exploratoire des Données, est une philosophie d'analyse développée par le statisticien **John Tukey**. Son objectif fondamental est de faire parler les données avant d'appliquer un modèle statistique ou prédictif.

D'un point de vue théorique, l'EDA poursuit plusieurs objectifs essentiels.

### 3.1.1 Comprendre la Structure et la Qualité des Données

L'une des premières missions de l'EDA consiste à examiner la qualité générale du jeu de données afin d'identifier :

- les valeurs manquantes (*Missing Values*) ;
- les doublons ;
- les erreurs de saisie ;
- les incohérences ;
- les valeurs aberrantes (*Outliers*).

Cette étape permet de dresser un premier diagnostic de l'état du dataset avant toute intervention.

---

### 3.1.2 Découvrir les Structures Cachées (Patterns)

L'EDA permet d'observer comment les variables se comportent individuellement et collectivement.

L'étude des distributions, des corrélations et des relations entre variables met en évidence des structures invisibles à première vue et révèle les mécanismes qui gouvernent les comportements observés.

---

### 3.1.3 Vérifier les Hypothèses Statistiques

Avant d'entraîner un modèle d'intelligence artificielle, il est indispensable de vérifier que les données respectent certaines hypothèses statistiques.

L'EDA permet notamment d'identifier :

- les variables fortement corrélées ;
- les risques de multicolinéarité ;
- les distributions atypiques ;
- les variables peu informatives.

Cette étape garantit que les futurs modèles seront construits sur des données fiables et cohérentes.

---

### 3.1.4 Guider le Feature Engineering

L'EDA joue également un rôle essentiel dans la création de nouvelles variables.

En analysant les comportements des différentes variables, il devient possible de déterminer :

- quelles variables possèdent un fort pouvoir prédictif ;
- lesquelles doivent être transformées ;
- lesquelles peuvent être combinées ;
- lesquelles doivent être supprimées afin d'améliorer les performances du futur modèle.

Ainsi, l'EDA constitue la base de toute stratégie de **Feature Engineering**.

---

# 4. Objectifs de l'EDA Appliqués à Notre Dataset Télécom

Dans le cadre de cette étude consacrée à la détection de fraude télécom, l'EDA ne constitue pas une simple étape descriptive. Elle représente un véritable travail de décryptage des comportements observés dans les données.

Notre analyse poursuit principalement trois objectifs.

## 4.1 Décoder le « Gène » de la Fraude (Portrait-Robot du Fraudeur)

Le jeu de données utilisé dans cette étude a été conçu pour reproduire un environnement réaliste intégrant du bruit statistique ainsi que des chevauchements entre comportements légitimes et frauduleux.

Le premier objectif consiste donc à identifier les véritables signatures comportementales de la fraude.

L'EDA doit répondre à plusieurs questions essentielles :

- Comment reconnaître un fraudeur ?
- Son comportement est-il identifiable grâce aux graphes relationnels ?
- Son activité est-elle caractérisée par une vitesse élevée de numérotation ?
- L'ancienneté de sa ligne téléphonique constitue-t-elle un indicateur pertinent ?

L'ensemble des analyses statistiques et graphiques permettra de répondre à ces interrogations.

---

## 4.2 Identifier les Cas Limites (Edge Cases)

L'un des principaux défis d'un système de détection de fraude réside dans la limitation des faux positifs.

Bloquer un client légitime représente un coût économique important pour un opérateur télécom.

L'EDA cherche donc à identifier précisément :

- les entreprises présentant un volume d'appels élevé (centres d'appels, services de livraison, services clients) afin d'éviter qu'elles soient assimilées à des fraudeurs ;
- les fraudeurs opérant à faible volume mais présentant d'autres caractéristiques suspectes.

Cette cartographie des cas limites constitue une étape indispensable avant la conception d'un système de détection automatisé.

---

## 4.3 Valider la Faisabilité d'un Futur Modèle de Machine Learning

Enfin, l'EDA sert de véritable test de faisabilité.

Son objectif est de déterminer si les classes **« Appels légitimes »** et **« Appels frauduleux »** sont statistiquement séparables.

Si les différentes distributions s'étaient révélées totalement confondues, aucun algorithme de Machine Learning n'aurait été capable d'obtenir des performances satisfaisantes.

À l'inverse, la présence de séparations nettes entre les deux classes constitue une preuve scientifique de la faisabilité du projet.

Les résultats obtenus orienteront naturellement le choix des futurs algorithmes, notamment les modèles basés sur les arbres de décision tels que **XGBoost**, **LightGBM** ou **Random Forest**, particulièrement adaptés à ce type de données.

---

# 5. Présentation du Jeu de Données

Le jeu de données étudié comprend **10 000 enregistrements d'appels téléphoniques** contenant des informations comportementales, temporelles et relationnelles destinées à reproduire un environnement réaliste de détection de fraude télécom.

Les variables disponibles permettent notamment d'analyser :

- la durée des appels ;
- l'ancienneté des numéros téléphoniques ;
- le nombre de correspondants contactés ;
- le taux de blocage par les destinataires ;
- le score de réputation des appelants ;
- les comportements de numérotation séquentielle ;
- les connexions avec des fraudeurs déjà identifiés dans le réseau.

Ces différentes caractéristiques constituent les principaux indicateurs étudiés tout au long de cette analyse exploratoire.

---

# 6. Analyse Quantitative du Jeu de Données

## 6.1 Équilibre des Classes (Graphique 1)

La première étape de l'analyse consiste à examiner la répartition de la variable cible.

Notre jeu de données présente une distribution particulièrement favorable à l'entraînement d'un modèle de Machine Learning :

- **70 % d'appels légitimes**, soit **7 000 observations** ;
- **30 % d'appels frauduleux**, soit **3 000 observations**.

Cette répartition est particulièrement intéressante d'un point de vue statistique.

En effet, dans les systèmes réels de détection de fraude (télécommunications, banque ou assurance), les classes sont généralement extrêmement déséquilibrées, avec parfois **99,9 % de transactions légitimes contre seulement 0,1 % de fraude**.

Une telle situation impose souvent le recours à des techniques de rééquilibrage des données, telles que :

- le sur-échantillonnage (*SMOTE*) ;
- le sous-échantillonnage ;
- ou d'autres méthodes de rééquilibrage des classes.

Dans notre cas, la proportion de **30 % de fraude** offre une base d'apprentissage particulièrement favorable.

Le futur modèle pourra apprendre de manière équilibrée les caractéristiques des deux classes sans introduire de biais algorithmique majeur, ce qui constitue un avantage important pour la phase de modélisation.
# 7. Cartographie des Corrélations (Graphique 2)

L'étude des corrélations constitue une étape essentielle de l'Analyse Exploratoire des Données (EDA). Elle permet de mesurer l'intensité des relations linéaires entre les différentes variables du jeu de données et d'identifier celles qui possèdent le plus fort pouvoir prédictif vis-à-vis de la fraude.

Au-delà de la simple compréhension des données, cette analyse permet également de détecter les variables redondantes susceptibles de perturber les futurs modèles de Machine Learning.

L'analyse de la matrice de corrélation met ainsi en évidence deux enseignements majeurs : l'existence de variables fortement liées au phénomène de fraude et la présence de phénomènes de colinéarité entre certaines caractéristiques.

---

## 7.1 Les Principaux Prédicteurs de la Fraude

Les résultats montrent que plusieurs variables présentent une corrélation particulièrement élevée avec la variable cible.

Parmi elles, deux indicateurs se distinguent nettement :

- **receiver_block_rate (+0,92)**, représentant le taux de blocage des appels par les destinataires ;
- **sequential_dialing_score (+0,90)**, mesurant le degré de numérotation séquentielle.

Ces deux variables évoluent presque parfaitement dans le même sens que la fraude. Plus leur valeur augmente, plus la probabilité qu'un appel soit frauduleux devient importante.

À l'inverse, le **reputation_score (-0,86)** présente une forte corrélation négative avec la fraude.

Autrement dit, plus le score de réputation d'un appelant est élevé, plus la probabilité qu'il s'agisse d'un utilisateur légitime augmente. Cette variable apparaît ainsi comme l'un des meilleurs indicateurs permettant de distinguer les comportements normaux des comportements frauduleux.

---

## 7.2 Détection de la Multicolinéarité

L'analyse met également en évidence une corrélation très élevée (**0,92**) entre :

- **call_duration_sec**
- **avg_call_duration_sec**

Ces deux variables apportent pratiquement la même information.

Cette forte redondance statistique, appelée **multicolinéarité**, risque d'introduire des informations dupliquées dans les futurs modèles de Machine Learning.

Cette observation justifie pleinement l'analyse plus approfondie réalisée dans le **Graphique 7** consacré aux anomalies comportementales.

---

# 8. Portrait-Robot du Fraudeur (Graphiques 3 et 6)

Les graphiques de densité (KDE) et les Boxplots permettent d'observer la distribution des principales variables comportementales pour les appels légitimes et frauduleux.

Contrairement à une simple analyse descriptive, ces visualisations mettent en évidence les ruptures statistiques qui caractérisent les fraudeurs.

Quatre comportements distinctifs apparaissent clairement.

---

## 8.1 La Politique de la « Carte Jetable » (caller_age_days)

L'ancienneté du numéro de téléphone constitue l'un des indicateurs les plus discriminants du jeu de données.

Chez les utilisateurs légitimes, les comptes présentent un cycle de vie long et stable, avec une médiane largement supérieure à **1 000 jours**.

À l'inverse, les fraudeurs utilisent principalement des comptes très récents, dont la médiane est inférieure à **500 jours**.

Cette différence traduit une stratégie classique de fraude consistant à utiliser des cartes SIM prépayées ou des numéros éphémères, rapidement abandonnés dès qu'ils sont détectés par les opérateurs ou signalés par les victimes.

Ainsi, la jeunesse d'un compte apparaît comme un indicateur fort de risque.

---

## 8.2 La Stratégie du « Bombardement » (unique_receivers_24h)

Le nombre de destinataires uniques contactés au cours des dernières 24 heures constitue également une variable particulièrement discriminante.

Les utilisateurs légitimes contactent généralement entre **1 et 20 correspondants différents** sur une journée.

Même dans le cas de professionnels ou de petites entreprises, cette valeur reste relativement limitée.

En revanche, les fraudeurs présentent une explosion statistique du nombre de correspondants.

Les distributions montrent que certains numéros frauduleux contactent entre **80 et 200 destinataires uniques** en une seule journée.

Ce comportement correspond parfaitement aux campagnes automatisées de phishing, de spam vocal ou de démarchage frauduleux de masse.

---

## 8.3 Une Activité Fortement Automatisée (sequential_dialing_score)

L'étude du **Sequential Dialing Score** révèle un comportement radicalement différent entre les deux classes.

Les utilisateurs légitimes obtiennent des scores très proches de zéro, traduisant une numérotation naturelle.

À l'inverse, les fraudeurs présentent une concentration importante autour de **80 %**, révélant une génération automatique de numéros successifs.

Cette caractéristique constitue une signature typique des systèmes de numérotation robotisés utilisés lors des campagnes de fraude à grande échelle.

---

## 8.4 Un Taux de Blocage Exceptionnellement Élevé (receiver_block_rate)

Le taux de blocage par les destinataires constitue probablement l'indicateur le plus révélateur du comportement frauduleux.

Chez les utilisateurs légitimes, cette variable demeure très proche de zéro.

Les fraudeurs, en revanche, génèrent un taux de blocage compris entre **60 % et 70 %**, signe que leurs appels sont massivement rejetés ou signalés par les victimes.

La combinaison d'un fort **Sequential Dialing Score** et d'un **Receiver Block Rate** élevé constitue ainsi une signature comportementale particulièrement caractéristique de la fraude télécom.

---

# 9. Gestion des Cas Limites et Réduction des Faux Positifs (Graphique 4)

L'un des principaux défis des systèmes automatiques de détection de fraude consiste à limiter les faux positifs.

Bloquer un client professionnel légitime peut avoir des conséquences économiques importantes pour un opérateur.

Le Graphique 4 met précisément en évidence cette problématique.

L'observation du nuage de points révèle un groupe très distinct d'utilisateurs légitimes effectuant entre **200 et 800 appels par jour**.

À première vue, une règle métier basée uniquement sur le volume d'appels aurait conduit à considérer ces utilisateurs comme frauduleux.

Pourtant, une analyse plus approfondie montre que ces mêmes utilisateurs disposent :

- d'un **Reputation Score très élevé** ;
- d'un **Receiver Block Rate proche de zéro**.

Ces deux indicateurs démontrent qu'il s'agit en réalité de centres d'appels, services clients ou entreprises parfaitement légitimes.

Cette observation souligne qu'un système de détection performant ne peut jamais se limiter au volume d'activité.

Le futur modèle devra impérativement croiser plusieurs variables comportementales afin d'éviter de pénaliser les clients légitimes à forte activité.

---

# 10. L'Approche Réseau : L'Apport de l'Intelligence Graphe (Graphique 5)

La fraude moderne fonctionne rarement de manière isolée.

Les fraudeurs partagent fréquemment des infrastructures communes et forment des groupes fortement connectés au sein des réseaux de communication.

L'analyse relationnelle met précisément ce phénomène en évidence.

Le Graphique 5 révèle une frontière particulièrement nette.

Lorsqu'un numéro possède **plus de dix connexions** avec des numéros déjà identifiés comme frauduleux, la probabilité qu'il appartienne lui-même à un réseau malveillant devient extrêmement élevée.

Cette frontière constitue un véritable seuil de rupture comportementale.

Par ailleurs, ces numéros situés au cœur des clusters de fraude présentent également les volumes de signalements pour spam les plus importants, représentés par les plus grandes bulles du graphique.

Cette approche montre que la fraude peut être détectée non seulement grâce au comportement individuel d'un numéro, mais également grâce à sa position au sein du réseau téléphonique.

L'intégration d'informations relationnelles constitue ainsi un levier majeur pour améliorer les performances d'un système de détection.

---

# 11. Analyse Temporelle et Comportementale (Graphique 7)

Le Graphique 7 compare la durée de l'appel courant avec la durée moyenne historique de chaque utilisateur.

Cette analyse vise à détecter d'éventuelles ruptures comportementales.

Une hypothèse classique consiste à imaginer qu'un fraudeur détourne temporairement un compte légitime afin d'effectuer des appels exceptionnellement longs ou inhabituels.

Cependant, les résultats obtenus montrent une réalité très différente.

Les appels frauduleux restent majoritairement concentrés autour de durées courtes et suivent fidèlement leur comportement historique.

Aucune rupture importante n'est observée.

Cette absence d'anomalies suggère que les fraudeurs conservent un comportement stable tout au long de leur activité.

Ils ne cherchent pas à imiter progressivement les utilisateurs légitimes ; ils maintiennent au contraire une activité courte, répétitive et fortement automatisée.

Cette observation conduit à une conclusion importante.

Dans ce contexte, le futur modèle de Machine Learning devra privilégier la détection de comportements monotones et répétitifs plutôt que la recherche de variations soudaines de comportement.
# 12. Les Métriques Statistiques Calculées : Définitions, Utilités et Nécessités

L'Analyse Exploratoire des Données (EDA) ne repose pas uniquement sur l'observation des graphiques. Elle s'appuie également sur un ensemble de calculs statistiques permettant de transformer un jeu de données brut en informations exploitables.

Dans cette étude, les principales statistiques descriptives ont été obtenues à l'aide de fonctions telles que **`df.describe()`** et **`df.corr()`**, qui permettent de résumer les caractéristiques des variables et d'étudier leurs relations.

Ces calculs constituent une étape indispensable avant toute phase de modélisation, car ils fournissent une compréhension quantitative des données et permettent de guider les choix méthodologiques du projet.

---

# 12.1 La Moyenne Statistique (μ – Mean)

## Définition

La moyenne statistique correspond à la somme de toutes les valeurs d'une variable divisée par le nombre total d'observations.

Elle représente le comportement moyen ou central d'un indicateur au sein de l'ensemble du jeu de données.

Mathématiquement :

\[
\mu = \frac{\sum_{i=1}^{n}x_i}{n}
\]

où :

- \(x_i\) représente chaque observation ;
- \(n\) représente le nombre total d'observations.

---

## Utilité dans notre étude

La moyenne permet d'établir une valeur de référence (*baseline*) pour le comportement normal d'un utilisateur.

Par exemple, la variable **avg_call_duration_sec** représente la durée moyenne historique des appels d'un utilisateur.

Cette valeur sert de point de comparaison avec les nouveaux appels afin de détecter d'éventuels comportements inhabituels.

---

## Pourquoi cette métrique est-elle indispensable ?

Sans moyenne de référence, il devient impossible de mesurer l'écart entre un comportement observé et le comportement habituel d'un utilisateur.

Toute détection d'anomalie repose sur cette comparaison.

Ainsi, la moyenne constitue la première étape permettant d'identifier des comportements potentiellement frauduleux.

---

# 12.2 La Matrice de Corrélation (Coefficient de Pearson)

## Définition

La corrélation de Pearson mesure la force et le sens de la relation linéaire entre deux variables.

Le coefficient varie entre :

- **+1** : corrélation positive parfaite ;
- **−1** : corrélation négative parfaite ;
- **0** : absence de relation linéaire.

---

## Utilité dans notre étude

La matrice de corrélation permet d'identifier immédiatement quelles variables évoluent avec la fraude.

Notre analyse met notamment en évidence :

- **receiver_block_rate (+0,92)** : plus le taux de blocage augmente, plus le risque de fraude augmente ;

- **sequential_dialing_score (+0,90)** : les comportements de numérotation séquentielle sont fortement associés à la fraude ;

- **reputation_score (-0,86)** : une bonne réputation est fortement associée aux utilisateurs légitimes.

Ces résultats permettent d'identifier rapidement les variables possédant le plus fort pouvoir prédictif.

---

## Pourquoi cette métrique est-elle indispensable ?

La corrélation remplit deux fonctions essentielles.

### Sélection des Variables (Feature Selection)

Elle permet d'identifier les variables qui apportent réellement de l'information au futur modèle de Machine Learning.

Les variables fortement corrélées avec la fraude constituent naturellement les meilleurs candidats pour l'entraînement.

---

### Détection de la Multicolinéarité

La corrélation permet également de détecter les variables redondantes.

Dans notre étude, **call_duration_sec** et **avg_call_duration_sec** présentent une corrélation de **0,92**, ce qui indique qu'elles véhiculent pratiquement la même information.

Conserver simultanément ces deux variables pourrait ralentir l'entraînement du modèle, compliquer son interprétation et favoriser le surapprentissage (*Overfitting*).

La matrice de corrélation permet ainsi d'optimiser le futur jeu de données destiné au Machine Learning.

---

# 12.3 Les Quartiles et l'Analyse de la Dispersion

## Définition

Les quartiles divisent une distribution en quatre parties égales.

On distingue principalement :

- le premier quartile (**Q1 – 25 %**) ;
- la médiane (**Q2 – 50 %**) ;
- le troisième quartile (**Q3 – 75 %**).

Ces indicateurs sont notamment utilisés dans les **Boxplots** afin de représenter la dispersion des données.

---

## Utilité dans notre étude

Contrairement à la moyenne, les quartiles sont beaucoup moins sensibles aux valeurs extrêmes.

Ils permettent de localiser la majorité des observations et d'observer la dispersion réelle des comportements.

Ils rendent ainsi possible une comparaison plus robuste entre les comportements légitimes et frauduleux.

---

## Pourquoi cette métrique est-elle indispensable ?

Les quartiles constituent le fondement de nombreuses règles de décision utilisées en détection d'anomalies.

Par exemple, il devient possible de définir une règle telle que :

> Si l'ancienneté d'un compte appartient aux 25 % les plus faibles du réseau et que son volume d'appels appartient aux 25 % les plus élevés, alors une alerte de fraude peut être déclenchée.

Les quartiles permettent donc de transformer les observations statistiques en règles opérationnelles exploitables par un système intelligent.

---

# 13. Importance Cruciale des Calculs Statistiques dans l'EDA

L'intuition métier constitue souvent le point de départ d'un projet de détection de fraude.

Par exemple, il peut sembler évident qu'un fraudeur passe un grand nombre d'appels.

Cependant, cette intuition reste insuffisante pour développer un système industriel fiable.

Les calculs statistiques réalisés lors de l'EDA permettent de transformer ces intuitions en connaissances mesurables, reproductibles et scientifiquement vérifiables.

Sans cette étape, le risque de construire un modèle instable, biaisé ou peu performant devient très important.

---

## 13.1 Passer de l'Observation Visuelle à la Certitude Mathématique

Les graphiques permettent de visualiser les données.

Cependant, leur interprétation peut parfois varier selon les échelles utilisées ou la perception de l'observateur.

Les statistiques descriptives apportent une mesure objective.

Par exemple, plutôt que d'affirmer simplement que les fraudeurs utilisent des comptes récents, il devient possible de démontrer statistiquement que la majorité d'entre eux possèdent une ancienneté inférieure à un certain seuil.

Les décisions reposent ainsi sur des faits mesurables plutôt que sur une simple impression visuelle.

---

## 13.2 Évaluer le Pouvoir Séparateur des Variables

L'objectif d'un modèle de Machine Learning est de distinguer les appels légitimes des appels frauduleux.

Les calculs statistiques permettent d'évaluer dans quelle mesure chaque variable contribue à cette séparation.

Si la moyenne ou la médiane d'une variable est quasiment identique chez les fraudeurs et chez les utilisateurs légitimes, cette variable possède un faible pouvoir séparateur et contribue peu aux performances du modèle.

À l'inverse, lorsqu'une variable présente une différence importante entre les deux populations, elle devient un excellent candidat pour l'entraînement du modèle.

Par exemple, la variable **unique_receivers_24h** présente une séparation très nette entre utilisateurs légitimes et fraudeurs.

Cette différence confirme son importance stratégique dans la détection de fraude.

---

## 13.3 Diagnostiquer la Multicolinéarité pour Alléger les Modèles

Le calcul des corrélations permet également d'identifier les variables redondantes.

Lorsque deux variables évoluent presque exactement de la même manière, elles apportent une information similaire.

Cette redondance peut perturber les modèles prédictifs, augmenter leur complexité et ralentir leur exécution.

Dans notre étude, la forte corrélation entre **call_duration_sec** et **avg_call_duration_sec** justifie la suppression de l'une d'elles lors de la phase de modélisation.

Cette étape contribue à simplifier le modèle tout en conservant son pouvoir prédictif.

---

## 13.4 Comprendre la Dispersion et la Variance

La moyenne ne suffit pas toujours à décrire correctement une population.

Quelques valeurs extrêmes peuvent fortement influencer cette mesure.

L'analyse de la dispersion, à travers les quartiles et les Boxplots, permet de mieux comprendre la variabilité des comportements.

Nos calculs montrent notamment que les fraudeurs présentent un comportement relativement homogène, caractérisé par des appels courts et répétitifs.

À l'inverse, les utilisateurs légitimes présentent une plus grande diversité de comportements.

Cette différence constitue une information précieuse pour les futurs modèles de Machine Learning.

---

# 14. Synthèse des Calculs Statistiques

Les calculs statistiques réalisés lors de l'EDA constituent le socle scientifique de l'ensemble du projet.

Ils permettent :

- de résumer les principales caractéristiques du jeu de données ;
- d'identifier les variables les plus discriminantes ;
- de mesurer les relations entre les variables ;
- de détecter les phénomènes de redondance (multicolinéarité) ;
- d'analyser la dispersion des observations ;
- de transformer les observations qualitatives en résultats quantifiables.

Sans ces calculs, l'analyse reposerait uniquement sur des observations visuelles.

Grâce aux statistiques descriptives, le jeu de données est converti en une cartographie objective des risques. Ces indicateurs valident scientifiquement les hypothèses formulées au cours de l'EDA et fournissent des bases solides pour les étapes suivantes du projet, notamment le **Data Cleaning**, le **Feature Engineering** et la **modélisation par Machine Learning**.
# 15. L'EDA comme Outil de Diagnostic pour le Data Cleaning

L'Analyse Exploratoire des Données (EDA) ne constitue pas uniquement une étape descriptive destinée à comprendre les caractéristiques du jeu de données. Elle représente également le principal outil d'investigation permettant d'identifier les problèmes qui devront être corrigés lors de la phase de **Data Cleaning**.

En pratique, l'EDA joue le rôle d'un **diagnostic médical**, tandis que le Data Cleaning correspond au **traitement**. Il est impossible de nettoyer efficacement un jeu de données sans avoir, au préalable, identifié les anomalies qu'il contient.

Ainsi, même si l'EDA et le nettoyage des données sont présentés dans deux rapports distincts, ces deux étapes sont étroitement liées. Les observations réalisées durant l'EDA orientent directement les décisions qui seront prises lors de la préparation finale des données.

---

## 15.1 Détection des Valeurs Aberrantes (Outliers)

L'une des premières contributions de l'EDA consiste à mettre en évidence les valeurs aberrantes susceptibles de perturber les analyses ou les futurs modèles de Machine Learning.

Les **Boxplots (Graphique 6)** ainsi que certains **Scatter Plots (Graphiques 4 et 7)** permettent d'identifier visuellement les observations extrêmes situées en dehors du comportement normal de la population.

Par exemple, l'EDA pourrait révéler :

- un âge de compte négatif ;
- un nombre d'appels irréaliste ;
- des comportements incompatibles avec les contraintes physiques du système.

Ces observations indiquent immédiatement qu'un contrôle devra être effectué lors du nettoyage afin de déterminer si ces valeurs correspondent à des erreurs de saisie, des anomalies techniques ou des comportements réellement exceptionnels.

Ainsi, l'EDA permet de localiser les observations nécessitant une vérification approfondie avant toute phase de modélisation.

---

## 15.2 Détection des Valeurs Manquantes (Missing Values)

Les valeurs manquantes ne sont pas toujours représentées sous la forme classique de **NaN**.

Dans de nombreuses bases de données opérationnelles, une absence d'information peut être remplacée par des valeurs conventionnelles telles que :

- **0** ;
- **9999** ;
- **Unknown** ;
- ou d'autres valeurs par défaut.

L'EDA permet d'identifier ces situations en observant les distributions statistiques des variables.

Par exemple, un histogramme présentant un pic anormal autour de la valeur **0** ou **9999** peut révéler l'existence de valeurs manquantes déguisées.

Cette étape permet donc d'anticiper les traitements futurs, tels que :

- l'imputation par la moyenne ou la médiane ;
- le remplacement par une valeur plus pertinente ;
- ou la suppression des observations concernées lorsque cela est justifié.

---

## 15.3 Détection des Incohérences Logiques

L'EDA permet également de vérifier la cohérence interne du jeu de données.

Certaines anomalies n'apparaissent qu'en comparant plusieurs variables simultanément.

Le **Graphique 7**, consacré à l'analyse de la durée des appels, illustre parfaitement cette démarche.

Par exemple, une incohérence pourrait apparaître si :

- un utilisateur possède une durée d'appel très élevée alors que le nombre d'appels enregistrés pour cette journée est nul ;
- plusieurs variables décrivent des comportements incompatibles entre elles.

L'analyse exploratoire met ainsi en évidence les contradictions internes susceptibles d'altérer la qualité des données et d'influencer négativement les performances des futurs modèles.

---

## 15.4 Détection des Erreurs de Format et de Typage

L'EDA contribue également à identifier les problèmes liés au format des données.

Au cours de l'analyse descriptive, certaines variables peuvent présenter :

- des espaces inutiles ;
- des erreurs d'encodage ;
- des formats hétérogènes ;
- des variables numériques contenant du texte ;
- des catégories mal standardisées.

Par exemple, une variable censée contenir un score numérique pourrait parfois contenir des valeurs textuelles telles que **"High"** au lieu d'une valeur numérique.

Ces observations permettent de planifier les opérations de normalisation et de conversion nécessaires avant l'entraînement du modèle.

---

## 15.5 Pourquoi l'EDA est-elle Indispensable Avant le Data Cleaning ?

Les différents graphiques et statistiques produits durant cette étude montrent que l'EDA constitue le principal outil de diagnostic du Data Scientist.

En poussant les données dans leurs retranchements statistiques et graphiques, cette étape fait remonter à la surface :

- les anomalies ;
- les incohérences ;
- les erreurs de format ;
- les valeurs aberrantes ;
- les valeurs manquantes ;
- les comportements atypiques.

Sans cette analyse préalable, le nettoyage des données serait réalisé à l'aveugle, avec un risque élevé de supprimer des informations importantes ou de conserver des erreurs susceptibles de dégrader les performances du futur modèle.

---

# 16. Apport de Notre Script EDA dans la Détection des Anomalies

Au-delà des analyses descriptives classiques, le script développé dans cette étude applique une véritable logique d'investigation permettant d'identifier les signatures caractéristiques de la fraude.

Contrairement à une approche limitée à quelques statistiques descriptives, il combine plusieurs visualisations complémentaires afin d'étudier les comportements sous différents angles.

Cette approche permet non seulement de mieux comprendre le jeu de données, mais également d'anticiper les difficultés qui pourraient apparaître lors des étapes suivantes du projet.

---

## 16.1 Analyse Croisée des Variables

L'une des principales forces du script réside dans le croisement des variables.

Observer une variable de manière isolée est souvent insuffisant pour détecter un comportement suspect.

Par exemple, une durée d'appel de plusieurs centaines de secondes n'est pas nécessairement anormale.

En revanche, lorsqu'elle est comparée à la durée moyenne historique de l'utilisateur, cette information devient beaucoup plus pertinente.

Le **Graphique 7** illustre parfaitement cette logique en confrontant la durée actuelle des appels à leur comportement historique.

Même si notre analyse montre que les fraudeurs conservent ici un comportement relativement stable, cette approche demeure particulièrement efficace pour détecter d'éventuelles ruptures comportementales.

---

## 16.2 Identification des Faux Positifs

Le **Graphique 4** représente un autre point fort du script.

Il met simultanément en relation :

- le volume quotidien d'appels ;
- le score de réputation.

Cette représentation montre clairement que certains utilisateurs légitimes présentent un volume d'activité très important tout en conservant une excellente réputation.

Grâce à cette analyse, il devient possible d'éviter que les futurs modèles considèrent automatiquement les gros émetteurs d'appels comme frauduleux.

Cette étape contribue directement à la réduction des faux positifs.

---

## 16.3 Détection Visuelle des Valeurs Extrêmes

Les **Boxplots (Graphique 6)** jouent également un rôle essentiel.

Ils permettent de distinguer rapidement les observations situées en dehors du comportement habituel de la population.

Les points apparaissant en dehors des moustaches représentent des valeurs extrêmes susceptibles de nécessiter une analyse complémentaire.

Cette visualisation offre ainsi un moyen rapide et efficace d'identifier les observations atypiques parmi les **10 000 enregistrements** du jeu de données.

---

# 17. Synthèse Générale de l'EDA et Diagnostic de Faisabilité

L'Analyse Exploratoire des Données réalisée dans cette étude permet de dresser un diagnostic complet de la fraude télécom au sein du jeu de données étudié.

Les différentes analyses statistiques et graphiques montrent que les comportements frauduleux présentent des caractéristiques distinctes et reproductibles, facilitant leur identification.

Les principales signatures comportementales observées sont résumées dans le tableau suivant.

| **Métrique comportementale** | **Profil légitime** | **Profil frauduleux** |
|------------------------------|---------------------|-----------------------|
| Ancienneté du compte | Cycle de vie long et stable | Comptes très récents (cartes SIM jetables) |
| Destinataires uniques (24 h) | Faible à modérée | Très élevée (bombardement) |
| Structure des appels | Variable selon le contexte | Courte, monotone et robotique |
| Taux de blocage | Très faible | Très élevé |
| Numérotation séquentielle | Faible | Très importante |
| Position dans le réseau | Connexions normales | Clusters de fraude fortement connectés |

Cette synthèse met en évidence une séparation claire entre les deux populations.

---

## 17.1 Diagnostic Statistique de Séparabilité

L'un des principaux objectifs de cette EDA était de déterminer si les comportements des utilisateurs légitimes et des fraudeurs étaient suffisamment distincts pour permettre une classification automatique.

Les résultats obtenus montrent que les distributions observées sont largement séparées sur plusieurs variables stratégiques, notamment :

- **Receiver Block Rate** ;
- **Sequential Dialing Score** ;
- le nombre de destinataires uniques sur 24 heures ;
- l'ancienneté des comptes ;
- le score de réputation.

Cette séparation constitue une preuve statistique de la faisabilité du problème étudié.

---

## 17.2 Validation de la Faisabilité du Projet de Machine Learning

L'ensemble des analyses réalisées confirme que le problème de détection de fraude est mathématiquement résoluble.

Le jeu de données présente plusieurs caractéristiques favorables :

- une répartition équilibrée des classes (**70 % / 30 %**) ;
- des variables fortement discriminantes ;
- une bonne qualité globale des données ;
- des signatures comportementales clairement identifiables.

Ces éléments constituent des bases solides pour entraîner un futur modèle prédictif.

Les résultats obtenus suggèrent notamment que les algorithmes basés sur les arbres de décision, tels que **Random Forest**, **XGBoost** ou **LightGBM**, devraient être particulièrement adaptés à ce problème, en raison de leur capacité à exploiter efficacement les variables présentant de fortes séparations entre les classes.

---

# 18. Conclusion Générale

Cette Analyse Exploratoire des Données a permis de comprendre en profondeur la structure du jeu de données, d'identifier les principaux indicateurs de fraude et de mettre en évidence les relations existant entre les différentes variables.

Au-delà de la simple description statistique, cette étape a permis de démontrer que les comportements frauduleux possèdent des signatures clairement identifiables à travers des critères comportementaux, temporels et relationnels.

Les différentes analyses ont également confirmé l'importance des calculs statistiques dans l'interprétation des données, la sélection des variables pertinentes et la préparation des étapes suivantes du projet.

Enfin, cette EDA a joué un double rôle : elle a permis d'établir un diagnostic complet du jeu de données tout en préparant les futures phases de **Data Cleaning**, de **Feature Engineering** et de **Machine Learning**.

Ainsi, cette étude valide scientifiquement la faisabilité du projet et fournit des fondations analytiques solides pour la conception d'un système intelligent de détection automatique de fraude télécom.
