# Presentations (Fork FR)

Ce dépôt contient des documents pour les divers exposés et présentations que j'ai donnés. Vous trouverez ci-dessous des liens vers des enregistrements vidéo, le cas échéant.

###### Index:
  - [pluginval - Yeah, but Why Validate Plugins](#pluginval---yeah-but-why-validate-plugins)
  - [A Backgrounder on Background Tasks](#a-backgrounder-on-background-tasks)
  - [Using JUCE value trees and modern C++ to build large scale applications](#using-juce-valuetrees-and-modern-c-to-build-large-scale-applications)
  - [Using Modern C++ with JUCE to Improve Code Clarity](#using-modern-c-with-juce-to-improve-code-clarity)
  - [Using C++11 to Improve Code Clarity- Braced Initialisers](#using-c11-to-improve-code-clarity---braced-initialisers)

### pluginval - Yeah, but Why Validate Plugins
###### ADC 2018 - [Content](https://github.com/drowaudio/presentations/tree/master/ADC%202018%20-%20pluginval,%20Yeah,%20but%20Why%20Validate%20Plugins) - [Video](https://www.youtube.com/watch?v=Q97LBXqgMus)

Plus tôt dans l'année, nous avons publié un outil open source "pluginval" pour la validation des plugins audio. L'objectif est de faciliter l'automatisation du processus de test et de validation du développement des plugins afin d'attraper plus de bugs, et plus rapidement dans le processus de développement. De plus, cela peut être utilisé par les développeurs d'hôtes, et même par les utilisateurs finaux, pour vérifier la compatibilité des plugins avec les hôtes basés sur JUCE. Pour commencer, je vais donner un aperçu du pluginval, de l'architecture, des considérations de déploiement et comment tout le monde peut s'en servir.

Dans un deuxième temps, j'aborderai certains des cas qui ont inspiré la création de pluginval en premier lieu. Développer des plugins pour une API peut sembler simple mais il y a beaucoup de " gris " dans ce domaine. Je vais creuser un peu en donnant des exemples de ce que les hôtes et les plugins peuvent faire et les tests utilisés par pluginval pour s'assurer que vous n'êtes pas pris au dépourvu.


### A Backgrounder on Background Tasks
###### London Audio Developers Meetup - April 2018 - [Content](https://github.com/drowaudio/presentations/tree/master/Audio%20Developer%20Meetup%20April%202018) - [Video](https://skillsmatter.com/skillscasts/11632-audio-developers-meet-up-april)

Les applications doivent être réactives, ce qui signifie qu'elles ne doivent pas passer beaucoup de temps sur le thread de message principal et qu'elles doivent le faire en arrière-plan. Mais quelle est la meilleure façon de procéder ? Comment communiquer en toute sécurité avec le thread de message lorsque vous avez terminé ? Comment informer les utilisateurs de l'état de ces tâches ?

Il y a beaucoup de problèmes délicats à résoudre lorsqu'il s'agit de tâches de fond. Cet exposé se penche sur eux, construisant un système d'exécution de tâches à partir de principes de base et résolvant les pièges communs un par un. Une fois cela fait, nous verrons comment construire ce système dans une application du monde réel en utilisant des motifs composables et réutilisables.

L'utilisation de types stricts et de fonctions libres vous permet d'écrire beaucoup moins de code qui contient moins de ballonnements et qui est plus expressif.


### Using JUCE ValueTrees and Modern C++ to Build Large Scale Applications
###### ADC 2017  - [Content](https://github.com/drowaudio/presentations/tree/master/ADC%202017%20-%20Using%20JUCE%20ValueTrees%20and%20Modern%20C%2B%2B%20to%20Build%20Large%20Scale%20Applications) - [Video](https://youtu.be/3IaMjH5lBEY)

JUCE ValueTrees est une structure de données arborescente capable de contenir des données de forme libre. Ils disposent d'une interface de rappel pour être avertis des modifications apportées aux éléments de données ou à l'arborescence et sont dotés d'une fonction d'annulation intégrée. Pensez XML sur les stéroïdes !
Ces caractéristiques en font un candidat idéal pour le modèle de données de nombreuses applications.
S'appuyant sur les idées présentées l'an dernier à l'ADC "Using Modern C++ with JUCE to Improve Code Clarity", cet exposé a pour but de démystifier les complexités liées à la gestion de ValueTrees et d'exposer la nature élégante qu'ils contiennent, en les utilisant pour construire rapidement des applications graphiques et audio à grande échelle.

L'exposé vise à expliquer en profondeur les meilleures pratiques de ValueTree et comment les appliquer à de nombreuses situations de codage en utilisant un langage C++ clair, concis et moderne. Tout au long de l'exposé, l'accent sera mis sur la nature comptée par référence de ces objets et sur la nature synchrone ou asynchrone des événements de rappel générés, ainsi que sur leur lien avec les performances, la sécurité des threads et le débogage. Les tâches d'application courantes telles que la sérialisation, le copier/coller et l'annulation/rétablissement sont également explorées et comment elles sont simplement implémentées avec ValueTrees. En outre, l'exposé examinera les moyens de créer vos propres classes utilitaires sur ValueTrees lorsque c'est judicieux de le faire. Les classes développées sur mesure telles que la ValueTreeObjectList sont explorées et permettent la création d'objets concrets et sûrs pour le type gérés par l'état ValueTree.

Cet exemple de présentation vise à s'assurer que les participants de tous les niveaux d'expérience repartent avec une solide compréhension de la façon de construire rapidement des applications C++ JUCE en utilisant ValueTrees d'une manière moderne, sûre et amusante.


### Using Modern C++ with JUCE to Improve Code Clarity
###### ADC 2016 - [Content](https://github.com/drowaudio/presentations/tree/master/ADC%202016%20-%20Using%20Modern%20C%2B%2B%20to%20Improve%20Code%20Clarity) - (Unfortunately this talk was not recorded)

En s'appuyant sur les idées de l'année dernière, "Using C\+++11 pour améliorer la clarté du code : Braced Initialisers" de réduire le gonflement du code pour améliorer la clarté, les performances et la robustesse, cet exposé examine plus en détail les fonctionnalités du codage C++ moderne et comment les utiliser.

L'un des aspects majeurs de la programmation événementielle et applicative est la notion de "quand quelque chose arrive, faites-le". C+++ peut souvent se mettre en travers de l'expression claire de cette intention. Cet exposé vise à utiliser des styles de codage modernes, en combinaison avec les classes JUCE, pour exprimer plus clairement et de manière plus concise cette intention.

En particulier, un certain nombre d'applications lambda et std::function sont démontrées, allant des minuteries et des rappels asynchrones aux méthodes de dessin et à la délégation générale utilisées pour réduire les dépendances à l'héritage. Un regard concis et pratique sur std::async est également inclus dans le but d'améliorer la réactivité des applications en mettant simplement et efficacement en parallèle des zones de code intensives.

Cependant, lors de la transition vers des styles de codage modernes, il peut y avoir des pièges. Cet exposé montre également certains de ces pièges et explique comment les éviter. Il fournit de bonnes pratiques pour mélanger le code JUCE et le code C+++. En particulier, il examine le comportement de la déduction automatique et de la déduction de type utilisée en conjonction avec les pointeurs intelligents JUCE et quand préférer les alternatives std.

Cet exemple de présentation vise à introduire de nouveaux paradigmes et à augmenter le nombre d'outils dans votre boîte à outils tout en gardant le code clair, robuste et maintenable. Il ne s'agit pas d'expliquer comment les fonctions C+++11 fonctionnent sous le capot, mais les possibilités qu'elles ouvrent.


### Using C++11 to Improve Code Clarity - Braced Initialisers
###### JUCE Summit 2015 - [Content](https://github.com/drowaudio/presentations/tree/master/JUCE%20Summit%202015%20-%20Using%20C%2B%2B11%20to%20Improve%20Code%20Clarity-%20Braced%20Initialisers) - [Video](https://www.youtube.com/watch?v=SmriQ5zXeAk)

Il y a beaucoup de choses auxquelles un programmeur doit penser lorsqu'il écrit du code. Il s'agit notamment de : performances, lisibilité, maintenabilité, robustesse, sécurité, portabilité, compatibilité et évolutivité. Afin de rendre l'écriture de code plus facile à raisonner, une solution est d'écrire moins de code.

C+++11/14 nous fournit plusieurs nouveaux outils pour réduire le code standard afin que nous puissions exprimer plus simplement et de manière plus concise l'intention. Certaines des principales nouveautés sont les suivantes : déduction de type, filetages et futures, lambdas, objets de fonction, gabarits variadiques, gestion de la durée de vie des objets et initialisateurs entretoisés, etc.

Le terme "initialisateurs entretoisés" est utilisé ici pour décrire un certain nombre de nouvelles applications des entretoises, notamment l'initialisation agrégée, la déclaration de membre des initialisateurs entretoisés, la déduction du constructeur d'objet.

Cet exposé passe en revue plusieurs exemples de simplification et d'amélioration du code à l'aide des fonctions liées aux accolades, basés sur JUCE et liés au monde réel. L'objectif n'est pas seulement d'améliorer l'intelligibilité, mais aussi les performances et la robustesse avec moins de temps passé à taper et à lire.
