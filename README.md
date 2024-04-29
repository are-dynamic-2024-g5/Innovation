# Diffusion d'une innovation dans une population

## Introduction 

On a choisi d'étudier la diffusion d'une innovation dans une population. L'innovation en question peut-être une idée, un produit. 

### Objectif 

On a choisi comme hypothèse à valider ou invalider : La publicité/communication autour de l'innovation impacte plus les individus dans l'adoption de l'innovation que l'influence des pairs. Notre objectif est d'étudier l'évolution de l'adoption d'une innovation dans une population, impactée par la publicité et de déterminer si l'hypothèse est valide ou non.

## Modélisation - Code

On suppose que l'influence entre les pairs est proportionelle à l'écart d'âge entre les individus, c'est à dire qu'on suppose que plus des individus sont proches en âge, plus leur décision d'adoption de l'innovation sera influencé par les autres du même groupe d'âge. A l'inverse, plus des individus sont éloignés en âge, moins leur décision d'adoption de l'innovation influencera l'autre.

Le modèle fonctionne de la façon suivante :


- On considère un monde linéaire, supposant que tout le monde influence tout le monde  via les réseaux sociaux, on ne considère pas de voisinage pour l'influence des pairs, un monde linéaire est donc adapté à la modélisation, il n'y a pas de prise en compte spatiale. 
- Chaque personne est caractérisée par son âge, sa probabilité d'adoption, sa probabilité de déclin et si elle a ou non adopté l'innovation. 
- La probabilité d'adoption de chaque personne du monde est la même, elle est d'abord initialisé par rapport à la 'force' de la publicité/communication autour de l'innovation (avec un facteur de sensibilité). 
- La probabilité de déclin initiale est arbitraire.
- Les probabilité d'adoption et de déclin vont ensuite être impactée par l'influence des pairs. La probabilité d'adoption va augmenter si les autres individus ont adoptés l'innovation, et ce proportionnellement à leurs écarts d'âge, et de même pour la probabilité de déclin.
- La population est générée avec des âges au hasard entre 15 et 75 ans.


Les paramètres de la simulation sont :

- Le taux de 'force' de la publicité 
- La taille de la population
- Le nombre de personnes ayant initialement adopté l'innovation
- Le nombre d'itération 


## Interprétation des résultats

On lance plusieurs simulation sur une population de 2000 personnes avec 200 personnes ayant initialement adoptés l'innovation.
On remarque qu'à mesure que la force de la publicité augmente, les écarts du nombre d'adopteurs se réduisent entre les différentes tranches d'âges (écart maximal d'environ 20 personnes pour une force de pub de 0.05 parmis 198 adopteurs || écart d'environ 20 personnes pour une force de pub de 0.9 parmis près de 1700 adopteurs)

Ceci nous permet de valider l'hypothèse selon laquelle la publicité est plus décisive que l'influence des pairs.

<img width="802" alt="Capture d’écran 2024-04-29 à 17 27 16" src="https://github.com/are-dynamic-2024-g5/Innovation/assets/162325895/b5f32ad0-e8d8-414f-9785-83ba401e4f1c">

<img width="717" alt="Capture d’écran 2024-04-29 à 17 27 44" src="https://github.com/are-dynamic-2024-g5/Innovation/assets/162325895/bab1a9da-f2dc-4199-94fa-f34a747641ca">

<img width="737" alt="Capture d’écran 2024-04-29 à 17 27 59" src="https://github.com/are-dynamic-2024-g5/Innovation/assets/162325895/bddf0a1f-dca4-4b87-8026-4253e3a2edfc">

<img width="744" alt="Capture d’écran 2024-04-29 à 17 28 12" src="https://github.com/are-dynamic-2024-g5/Innovation/assets/162325895/2f11e599-2fd0-4d39-824a-b857b41df6fe">

<img width="788" alt="Capture d’écran 2024-04-29 à 17 28 28" src="https://github.com/are-dynamic-2024-g5/Innovation/assets/162325895/d6665498-11a1-4194-9de6-213d8f1c53de">



# Conclusion - Limites du modèle






## Carnet de bord 
### (05/03/2024) Introduction au projet : 
  Projet : Comment évolue la diffusion d'une innovation/idée/nouveauté au sein d'une population donnée ?
      --> différents paramètres : taille de la population, taux initial d'adoption de l'innovation, simplicité de l'innovation (compatibilité avec les normes de la population), ampleur de l'innovation sur les réseaux sociaux, stratégies de                         communications(pubs etc..), contexte social, econimique, culturel, politique, concurrance  
      Ex : adoption de la télé au sein dees foyers, des téléphones, propagation d'idées politiques, diffusion fake news, etc...
      Objectif -> réussir a modéliser l'adopation d'une innovation dans une population en fonction de différents paramètres
      
      ## Premières pistes de recherche et sources :
      
      *https://sorbonne-universite.primo.exlibrisgroup.com/permalink/33BSU_INST/1c3k0lm/alma991002877559806616
      *https://sorbonne-universite.primo.exlibrisgroup.com/permalink/33BSU_INST/nchfeo/alma991004932294606616
      *https://sorbonne-universite.primo.exlibrisgroup.com/permalink/33BSU_INST/nchfeo/alma991005264828406616
      
     >  _Présenté en 1983 par Everett Rogers, il analyse les modalités d’adoption d’une innovation, en étudiant notamment le rôle de la communication interpersonnelle et celui des leaders d’opinion. Rogers explique que l’individu qui est soumis à une innovation entre dans un processus comportant cinq étapes : la connaissance (knowledge), la persuasion (persuasion), la décision (decision), l’utilisation (implementation) et la confirmation (confirmation). Dans ces conditions, il devient possible de calculer un taux d’adoption découlant des caractéristiques de l’innovation, et de découper la population en sous-ensembles en fonction de la rapidité avec laquelle les individus qui les composent adoptent cette innovation
  ---->Le rôle des réseaux sociaux dans la diffusion de l'innovation reste une question stratégique. Dans des travaux antérieurs, nous avons introduit un apprentissage relationnel, basé sur la règle hebbienne, qui conduit à un état critique dans  lequel peu d'agents atteignent des positions structurelles de leaders d'opinion. Dans cet article, nous montrons que l'auto-organisation d'un réseau d'influence, à travers l'apprentissage social, n'est pas un processus monotonique, du point de vue de ses caractéristiques structurelles ainsi que de ses performances de diffusion. La notion d'intermédiarité, qui découle directement de la notion de réseau, apparaît nécessaire pour décrypter cette évolution. En introduisant le rôle des « liens faibles » dans les divers régimes de diffusion, il est alors possible d'apporter une nouvelle compréhension du phénomène. Le rôle des réseaux sociaux dans la diffusion de l'innovation demeure une question stratégique. Dans des travaux antérieurs, nous avons introduit un apprentissage relationnel, de type hebbien, qui conduit à un état critique, dans lequel certains agents acquièrent des positions, purement structurelles, de leaders d'opinion. Dans cet article, nous montrons que l'auto-organisation d'un réseau d'influence, par l'effet d'un apprentissage social, ne constitue pas un phénomène monotone, aussi bien du point de vue des caractéristiques structurelles du réseau que de celui de ses performances en diffusion. Ceci nécessite, pour être analysé, d'utiliser à la notion d'intermédiarité qui est inhérente au concept de réseau. Une analyse relative au rôle des "liens faibles" dans les différents régimes de diffusion devrait alors permettre d'offrir un éclairage nouveau sur cette dynamique d'évolution. Zimmermann Jean-Benoît, Deroïan Frédéric, Steyer Alexandre. Apprentissage social et diffusion de l'innovation : réseaux critiques et intermédiarité. Dans : Revue d'économie industrielle, vol. 103, 2e et 3e trimestre 2003. La morphogénèse des réseaux, sous la direction de Patrick Cohendet, Alan Kirman et Jean-Benoît Zimmermann. p. 71-89.
  
- Première Idée de code : 

On représente la population sous forme de listes de tableau, chaque tableau correspondant à une caractéristique pour chaque personne. On rajoute un tableau d'adoption de l'innovation. On réprésente l'innovation par un tableau de caractéristique. On prends chaque personne, on mêle les différentes caractéristiques de la personne et de l'innovation pour aboutir à un "taux de conviction" à partir d'un certain taux la personne adopte l'innovation. Initialement x personnes on déjà adoptées l'innovation. L'impact de chaque caractéristique sur le "taux de conviction" de la personne va être choisi par rapport aux études déjà faites sur le sujet que l'on aura trouvé. 
### 12-03-2024

Début de code ajouté au projet, on a défini le "plan" de code et de recherches en commentaire du code

### 19-03-2024 :

avancement sur le premier code, presque fini

### 26-03-2024 :

 achevement premier code mais tres brouillon, poursuite de recherches :
* https://www.persee.fr/doc/ecoap_0013-0494_1986_num_39_3_4086#ecoap_0013-0494_1986_num_39_3_T1_0619_0000
* https://www.cairn.info/sociologie-de-l-innovation--9782715408944-page-66.htm?contenu=plan
* https://theses.hal.science/tel-00440100/document
* https://archipel.uqam.ca/5885/1/M12804.pdf

### 02-04-2024 :

Nouveau code utilisation du modèle de simulation multi agent, modification du code de chatgtp, on doit l'améliorer/modifier l'implementation des parametres pour que ça soit cohérent pas de random, modifier si besoin les metriques de sorties si on a de nouvelles idées, faire plusieurs simulation et conserver les données pour
tirer des conclusions.


### 22-04-2024 : 

On décide de répondre à l'hypothèse : la communication, marketing autour d'une nouveauté est décisif/est ce qui joue le plus dans l'adoption d'une innovation pour les -40 ans mais impacte moins les +40 ans
On va donc fixer les autres paramètres et faire bouger celui ci pour voir ce qui se passe et ce que les métriques de sorties montrent


### 23-04 :

on pose que tout le monde est touché pareillement par la pub sur les reseaux
on suppose que, certes tout le monde s'influence un peu entre eux, mais les jeunes influencent plus les jeunes et les vieux influences plus les vieux 
on fait bouger la pub, on voit si ca prends le dessus sur l'influence intra age ou pas. 
On va faire un monde de personnes d'un age
il faut savoir combien ya de +40 ans et combien -40 ans 
on implémente un certain nombres d'adopteurs initiaux pour les -40 ans, un certain nombrre pour les +40 ans (a faire bouger)
on fait passer chaque personne par : l'influence de ceux de son age, l'influence de ceux de l'autre age, la force de la pub, ça donne une nouvelle probabilité d'adoption qui décide si la personne l'adopte ou pas
on itère, graphique,
