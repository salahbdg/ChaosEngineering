🧭 PLAN DÉTAILLÉ DE LA PRÉSENTATION

✅ 1. Introduction
🎯 Thème choisi : Fiabilité et résilience des systèmes dans un cadre DevOps à travers le Chaos Engineering
Dans les architectures DevOps modernes, on met l’accent sur :
la rapidité de mise en production (déploiements continus),


la scalabilité via le cloud,


l’automatisation des tests, du monitoring, etc.


Mais ces avantages viennent avec un nouveau défi : les systèmes deviennent massivement distribués (microservices), ce qui augmente le risque de panne imprévisible.
Exemples :
une instance EC2 meurt,


une configuration est mal propagée,


un pic de trafic fait planter un service non critique…


➡️ Chaos Engineering propose de tester la résilience de ces systèmes en injectant volontairement des pannes, dans des conditions contrôlées et réalistes, souvent en production.
🚨 Pourquoi c’est un challenge ?
La complexité des systèmes empêche de tout prévoir via des tests classiques.


En DevOps, les déploiements étant rapides et fréquents, les risques de régression sont élevés.


L’impact d’une panne non anticipée est souvent critique (perte de service, de clients, d’image).


Le test en production, bien qu’efficace, est encore tabou dans beaucoup d’organisations.



✅ 2. Présentation de l’article de départ
📌 Référence
Titre : Chaos Engineering


Auteurs : équipe "Traffic and Chaos" de Netflix


Organisme : Netflix, géant du streaming et pionnier du DevOps à grande échelle


Type de publication : Article scientifique – IEEE Software, vol. 33, n° 3, 2016


📄 DOI : 10.1109/MS.2016.60


🧠 Résumé des points principaux
Définition : discipline qui consiste à expérimenter sur un système distribué pour garantir qu’il résiste à des conditions réelles chaotiques (erreurs réseau, pannes, pics de charge…)


Objectif : garantir que le système reste fonctionnel et stable — le "steady state".


Méthodologie en 4 principes :


Formuler une hypothèse sur le comportement attendu.


Injecter une panne réaliste (ex. couper un service, ajouter de la latence).


Réaliser l’expérience en production (car les systèmes réels sont trop complexes à simuler).


Automatiser les expériences pour les répéter régulièrement.


Outils développés par Netflix :


Chaos Monkey : tue aléatoirement des instances.


Chaos Kong : simule la perte d’une région AWS complète.


FIT : tests d’échec entre services.


Indicateur principal : le SPS (streams per second) — une mesure simple et efficace de la santé du système.


✅ Pertinence de l’article
L’article est rédigé par ceux qui ont inventé cette approche (Netflix).


Il donne une méthodologie applicable et scientifiquement structurée.


Le contenu est directement transposable à des environnements DevOps modernes (cloud, microservices).


Il propose des outils concrets qui ont été testés en production sur une très large échelle.



✅ 3. Recherches bibliographiques complémentaires
🔎 Article 1 : Chaos Engineering chez Microsoft Azure
Titre : Inside Azure Search: Chaos Engineering


Source : Blog officiel Microsoft Azure (2015)


🔗 azure.microsoft.com/blog/inside-azure-search-chaos-engineering


Décrit la mise en place de Chaos Engineering dans les services Azure.


Confirme que les pannes simulées permettent de détecter des vulnérabilités inattendues dans un système pourtant bien testé.


🔎 Article 2 : Test extrême de résilience chez Facebook
Titre : Facebook turned off entire data center to test resiliency


Source : Data Center Knowledge (2014)


🔗 datacenterknowledge.com/facebook-test-resiliency


Facebook a coupé volontairement un datacenter entier pour tester ses mécanismes de résilience.


Montre une application radicale mais efficace de Chaos Engineering à très grande échelle.


🔄 Ce qu’ils apportent par rapport à l’article de Netflix :
Microsoft : même approche mais sur une autre infrastructure → confirmation de la méthode


Facebook : version plus extrême → approche complémentaire


Ces sources montrent que le Chaos Engineering est une discipline transversale, pas limitée à Netflix.



✅ 4. Conclusion et mise en perspective
🔁 Retour à la problématique
Le challenge DevOps est clair : comment garantir la stabilité des services dans un contexte de changements fréquents et d’architecture complexe ?
🧩 Résumé
L’article de Netflix introduit une méthode scientifique et outillée pour répondre à cette problématique.


Le test en production, les pannes contrôlées, et l’automatisation des tests sont au cœur de cette démarche.


D’autres acteurs majeurs du numérique utilisent des techniques similaires, ce qui valide la pertinence du modèle.


🔮 Mise en perspective
✅ Applicabilité : oui, pour les entreprises avec une bonne culture DevOps, des moyens d'observation et une tolérance au risque contrôlée.


⚠️ Limites :


Complexe à déployer dans des PME ou des environnements non cloud.


Demande une maturité en observabilité et automatisation.


💡 Pistes pour progresser :


Utiliser des outils comme Gremlin, LitmusChaos (open-source) ou AWS Fault Injection Simulator.


Former les équipes à la résilience, intégrer le chaos testing dans les pipelines CI/CD.


Partager les retours d’expérience pour renforcer la discipline.
