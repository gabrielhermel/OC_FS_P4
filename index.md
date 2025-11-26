# Dashboard de veille technologique

---

## Table des matières

1. [Introduction](#1-introduction)
2. [Frameworks de test](#2-frameworks-de-test)
  2.1. [Angular](#21-angular)
    2.1.1. [Frameworks de test applicatif](#211-frameworks-de-test-applicatif)
      2.1.1.1. [Vitest](#2111-vitest)
      2.1.1.2. [Jasmine](#2112-jasmine)
      2.1.1.3. [Jest](#2113-jest)
    2.1.2. [Frameworks de test end-to-end](#212-frameworks-de-test-end-to-end)
      2.1.2.1. [Playwright](#2121-playwright)
      2.1.2.2. [Cypress](#2122-cypress)
  2.2. [Java](#22-java)
    2.2.1. [Frameworks de test applicatif](#221-frameworks-de-test-applicatif)
      2.2.1.1. [JUnit 6](#2211-junit-6)
    2.2.2. [Frameworks de test end-to-end](#222-frameworks-de-test-end-to-end)
      2.2.2.1. [Selenium](#2221-selenium)
      2.2.2.2. [Playwright pour Java](#2222-playwright-pour-java)
    2.2.3. [Frameworks de test BDD](#223-frameworks-de-test-bdd)
      2.2.3.1. [Cucumber](#2231-cucumber)
      2.2.3.2. [Gauge](#2232-gauge)
3. [Bibliothèques de composants UI](#3-bibliothèques-de-composants-ui)
  3.1. [Angular](#31-angular)
    3.1.1. [Angular Material](#311-angular-material)
    3.1.2. [NG-ZORRO](#312-ng-zorro)
    3.1.3. [PrimeNG](#313-primeng)
4. [Paradigmes de programmation](#4-paradigmes-de-programmation)
  4.0. [Aperçu des paradigmes](#40-aperçu-des-paradigmes)
  4.1. [Angular](#41-angular)
    4.1.1. [Paradigmes principaux](#411-paradigmes-principaux)
    4.1.2. [Implications architecturales](#412-implications-architecturales)
  4.2. [Java](#42-java)
    4.2.1. [Paradigmes principaux](#421-paradigmes-principaux)
    4.2.2. [Implications architecturales](#422-implications-architecturales)

---

## 1. Introduction

Ce tableau de veille a pour objectif d’identifier les technologies les plus adaptées à l’adoption d’Angular et de Java au sein de Gen-Z Web. Il présente une synthèse claire et accessible des technologies étudiées et fournit une base technique fiable pour les futurs choix d’architecture.

La veille se concentre sur les éléments suivants :
* les frameworks de test pour Angular et Java
* les bibliothèques de composants visuels pour Angular
* les paradigmes de programmation associés à chaque technologie

---

## 2. Frameworks de test

### 2.1. Angular

<img src="assets/icons/angular.svg" alt="Angular logo" width="60">

#### 2.1.1. Frameworks de test applicatif

##### 2.1.1.1. Vitest

<img src="assets/icons/vitest.svg" alt="Vitest logo" width="60">

Vitest est désormais le framework et test runner officiel introduit avec Angular 21. Il remplace progressivement la pile historique Jasmine et Karma, et s’intègre directement à l’Angular CLI grâce à Vite.

**Points importants**
- Exécution rapide
- Test runner intégré
- Bon support TypeScript
- Outil de migration fourni par Angular pour passer de Jasmine à Vitest
- Solution pérenne, au cœur de la stratégie de test d’Angular

**Sources**
- [**Documentation officielle**](https://vitest.dev/)
- [**Guide officiel Angular** Migrating from Karma to Vitest](https://angular.dev/guide/testing/migrating-to-vitest)
- [**ng-news** Vitest — Angular’s New Testing Framework](https://medium.com/ng-news/ng-news-25-43-vitest-angulars-new-testing-framework-c4af76fef09f)
- [**Ninja Squad** What’s new in Angular 21](https://blog.ninja-squad.com/2025/11/20/what-is-new-angular-21.0)

##### 2.1.1.2. Jasmine

<img src="assets/icons/jasmine.svg" alt="Jasmine logo" width="60">

Jasmine a longtemps été le standard pour les tests Angular, exécutés principalement via le test runner Karma. Karma est désormais déprécié. Une piste avait été explorée autour de Web Test Runner comme remplacement moderne, mais Angular a finalement choisi Vitest, entraînant l’abandon progressif de Jasmine et Karma.

**Points importants**
- Non recommandé pour les nouveaux projets Angular
- À utiliser uniquement pour la maintenance d’applications existantes

**Sources**
- [**Documentation officielle**](https://jasmine.github.io)
- [**npm** Karma is deprecated](https://www.npmjs.com/package/karma)

##### 2.1.1.3. Jest

<img src="assets/icons/jest.svg" alt="Jest logo" width="60">

Jest est largement utilisé dans l’écosystème JavaScript grâce à sa rapidité et à son API moderne. Cependant, les builders dédiés à Angular ont été dépréciés et seront retirés à partir d’Angular 22, ce qui rend Jest inadapté pour les futurs projets Angular.

**Points importants**
- Non recommandé pour les nouveaux projets Angular
- Peut être utilisé pour :
  - des outils Node.js non liés à Angular
  - des bibliothèques utilitaires
  - des scripts ou projets hors framework

**Sources**
- [**Documentation officielle**](https://jestjs.io)
- [**ng-news** Future Testing Framework: Vitest or Jest?](https://medium.com/ng-news/ng-news-25-41-future-testing-framework-vitest-or-jest-ea65a318065c)

#### 2.1.2. Frameworks de test end-to-end

##### 2.1.2.1. Playwright

<img src="assets/icons/playwright.svg" alt="Playwright logo" width="60">

Playwright est un outil de test end-to-end moderne capable d’exécuter des tests sur Chrome, Firefox et WebKit. Il offre une API cohérente, des performances stables et une bonne évolutivité, ce qui en fait une solution adaptée aux applications Angular nécessitant des tests robustes et réalistes.

**Points importants**
- Compatible avec plusieurs navigateurs
- API uniforme et expressive
- Exécution stable et rapide
- Solution adaptée aux projets modernes, recommandée pour les nouveaux développements

**Sources**
- [**Documentation officielle**](https://playwright.dev)
- [**Angular.love** Modern E2E Testing for Angular Apps with Playwright](https://angular.love/modern-e2e-testing-for-angular-apps-with-playwright)
- [**Test Automation** Advantages and Disadvantages of Playwright](https://test-automation.blog/playwright/advantages-and-disadvantages-of-playwright/)

##### 2.1.2.2. Cypress

<img src="assets/icons/cypress.svg" alt="Cypress logo" width="60">

Cypress est apprécié pour son interface interactive et sa facilité de prise en main. Il exécute les tests directement dans un navigateur contrôlé, ce qui facilite le débogage. Ses limites concernent principalement l’absence de support WebKit et une évolutivité moindre sur de grandes suites de tests.

**Points importants**
- Expérience développeur agréable
- Interface de débogage intuitive
- Pas de support WebKit
- Adapté à des projets de taille réduite ou intermédiaire

**Sources**
- [**Documentation officielle**](https://www.cypress.io)
- [**BigBinary** Why we switched from Cypress to Playwright](https://www.bigbinary.com/blog/why-we-switched-from-cypress-to-playwright)

### 2.2 Java

<img src="assets/icons/java.svg" alt="Java logo" width="60">

#### 2.2.1. Frameworks de test applicatif

##### 2.2.1.1. JUnit 6

<img src="assets/icons/junit6.webp" alt="JUnit 6 logo" width="60">

JUnit 6 constitue aujourd’hui le standard moderne pour les tests applicatifs en Java. Il repose sur une architecture modulaire et offre un modèle d’extensions flexible, des tests paramétrés, des tests imbriqués et une intégration fluide avec Maven, Gradle et les IDE. La majorité des nouveaux projets Java adoptent JUnit 6 en raison de sa maturité, de son écosystème et de son évolution active.

**Points importants**
- Standard moderne pour les tests unitaires et d’intégration légère
- Architecture modulaire et extensible
- Large adoption et documentation abondante
- Intégration native avec les outils de développement et d’intégration continue

**Sources**
- [**Documentation officielle**](https://docs.junit.org/current/user-guide/)
- [**A Java geek** Are you really wasting your time in Java without these 10 libraries?](https://blog.frankel.ch/wasting-time-without-10-libraries/)
- [**Bestarion** 8 Test Frameworks for Java/Fullstack Developers](https://bestarion.com/test-frameworks-to-follow-for-javafullst/)
- [**Javarevisited** JUnit 5 is dead, long live JUnit 6!](https://medium.com/javarevisited/junit-5-is-dead-long-live-junit-6-e142806c11a6)

#### 2.2.2. Frameworks de test end-to-end

##### 2.2.2.1. Selenium

<img src="assets/icons/selenium.svg" alt="Selenium logo" width="60">

Selenium est la solution historique pour les tests d’interface web en Java. Sa version 4 introduit de nombreuses améliorations, notamment le protocole WebDriver BiDi, une meilleure compatibilité avec les navigateurs modernes et un support plus cohérent. Sa vaste communauté, son écosystème mature et sa stabilité en font l’option privilégiée dans les environnements Java d’entreprise.

**Points importants**
- Standard reconnu pour l’automatisation des tests web
- Large compatibilité entre navigateurs
- Écosystème riche et documentation étendue

**Sources**
- [**Documentation officielle**](https://www.selenium.dev/documentation/)
- [**GeeksforGeeks** Pros and Cons of Selenium as an Automation Testing tool](https://www.geeksforgeeks.org/software-testing/pros-and-cons-of-selenium-as-an-automation-testing-tool/)
- [**BrowserStack** Why should Selenium be selected as a tool?](https://www.browserstack.com/guide/why-should-selenium-be-selected-as-a-tool)
- [**TestDevLab** Automated Testing With Java and Selenium: Advantages, Specifics, and Challenges](https://www.testdevlab.com/blog/test-automation-with-java-and-selenium)

##### 2.2.2.2. Playwright pour Java

<img src="assets/icons/playwright.svg" alt="Playwright logo" width="60">

Playwright est une alternative moderne pour les tests end-to-end, offrant une exécution rapide, fiable et dotée d’un système d’attente automatique. Il inclut des outils intégrés tels que le trace viewer, le codegen et l’inspecteur, facilitant le débogage. Bien que sa communauté Java soit plus restreinte que celle de Selenium, Playwright propose une approche moderne particulièrement adaptée aux applications web dynamiques. Son adoption pourrait également harmoniser les pratiques de test avec Angular, où Playwright est souvent recommandé.

**Points importants**
- Exécution rapide et stable grâce à l’attente automatique
- Outils intégrés pour l’analyse et le débogage
- Solution moderne pour les applications web complexes

**Sources**
- [**Documentation officielle**](https://playwright.dev/java/)
- [**BrowserStack** Playwright vs Selenium: Which to choose in 2025](https://www.browserstack.com/guide/playwright-vs-selenium)
- [**applitools** Playwright vs Selenium: What are the Main Differences and Which is Better?](https://applitools.com/blog/playwright-vs-selenium/)

#### 2.2.3. Frameworks de test BDD

##### 2.2.3.1. Cucumber

<img src="assets/icons/cucumber.svg" alt="Cucumber logo" width="60">

Cucumber est la solution BDD la plus largement adoptée dans l’écosystème Java. Il utilise la syntaxe Gherkin pour décrire les comportements attendus sous forme de scénarios lisibles, améliorant la communication entre équipes techniques et fonctionnelles. Il s’intègre facilement avec JUnit ainsi qu’avec Selenium ou Playwright pour l’automatisation des étapes.

**Points importants**
- Standard BDD largement adopté
- Syntaxe Gherkin lisible
- Intégration fluide avec JUnit et les outils d’automatisation
- Peut introduire une surcharge de maintenance (multiplication des étapes, etc.)

**Sources**
- [**Documentation officielle**](https://cucumber.io/docs)
- [**BrowserStack** What is Cucumber Framework? (Benefits of Cucumber Testing)](https://www.browserstack.com/guide/learn-about-cucumber-testing-tool)
- [**PixelQA** Cucumber BDD Framework: Features, Setup & Benefits](https://www.pixelqa.com/blog/post/cucumber-bdd-testing-framework-guide)
- [**TestGrid** Cucumber Testing Framework: The Ultimate Guide with Practical Examples](https://testgrid.io/blog/cucumber-testing/)

##### 2.2.3.2. Gauge

<img src="assets/icons/gauge.svg" alt="Guage logo" width="60">

Gauge est une alternative moderne à Cucumber, proposée par ThoughtWorks. Conçu pour réduire la complexité et les problèmes de maintenance associés aux définitions d’étapes Gherkin, il utilise des spécifications en Markdown plus simples à écrire et à refactorer. Gauge s’intègre avec Java, Selenium et Playwright, et bénéficie d’une adoption croissante dans certains environnements d’entreprise.

**Points importants**
- Spécifications en Markdown plus faciles à maintenir que Gherkin
- Intégration simple avec Java et les outils d’automatisation
- Conçu pour corriger certaines limites de Cucumber (duplication, surcharge de maintenance)
- Alternative moderne et minimaliste pour les tests orientés comportement

**Sources**
- [**Documentation officielle**](https://docs.gauge.org/)
- [**Test Automation Tools** Top 5 BDD Testing Tools – 2025 Review](https://testautomationtools.dev/bdd-testing-tools/#Gauge)
- [**Knapsack Pro** Gauge vs Cucumber](https://knapsackpro.com/testing_frameworks/difference_between/gauge/vs/cucumber)

---

## 3. Bibliothèques de composants UI

### 3.1. Angular

<img src="assets/icons/angular_new.svg" alt="Angular logo" width="60">

#### 3.1.1. Angular Material

<img src="assets/icons/material.svg" alt="Material logo" width="60">

Angular Material est la bibliothèque officielle développée et maintenue par l’équipe Angular. Elle fournit un ensemble cohérent de composants conformes aux standards Material Design, avec une forte attention portée à l’accessibilité, aux performances et à la réactivité. Grâce à son intégration native avec l’Angular CDK, aux bonnes pratiques qu’elle impose et à son support à long terme, elle constitue un choix sûr et durable pour les projets Angular.

**Points importants**
- Intégration native avec Angular et le CDK
- Accessibilité et cohérence assurées par les standards Material Design
- Maintenance solide et longévité garanties par l’équipe Angular
- Style plus rigide et gamme de composants plus limitée que certaines alternatives

**Sources**
- [**Documentation officielle**](https://material.angular.dev/)
- [**Syncfusion** 10 Essential Angular Component Libraries Every Developer Needs in 2025](https://www.syncfusion.com/blogs/post/angular-component-libraries-in-2025)
- [**iFlair** Choosing the Right Angular UI Library](https://www.iflair.com/choosing-the-right-angular-ui-library-angular-material-primeng-and-ng-zorro-compared/)
- [**BairesDev** Angular Material vs Bootstrap: Which One Is Best?](https://www.bairesdev.com/blog/angular-material-vs-bootstrap/)

#### 3.1.2. NG-ZORRO

<img src="assets/icons/ng-zorro.svg" alt="NG-ZORRO logo" width="60">

NG-ZORRO est la déclinaison Angular du design system Ant Design. Il propose un ensemble étendu de composants modernes, cohérents et bien adaptés aux applications d’administration ou aux outils internes nécessitant une interface structurée et uniforme. Sa richesse fonctionnelle en fait une alternative crédible à Angular Material, mais son écosystème plus restreint et sa popularité moindre limitent parfois la disponibilité de ressources et de retours d’expérience.

**Points importants**
- Large éventail de composants cohérents basés sur Ant Design
- Design moderne et adapté aux interfaces professionnelles structurées
- Écosystème et communauté plus réduits que les solutions les plus répandues

**Sources**
- [**Documentation officielle**](https://ng.ant.design/docs/introduce/en)
- [**UI Bakery** 5 Top Angular Component Libraries You Should Know in 2025](https://uibakery.io/blog/top-angular-libraries)
- [**LogixBuilt** Best Angular Component Library in 2025](https://logixbuilt.com/blogs/best-angular-component-library-in-2025)

#### 3.1.3. PrimeNG

<img src="assets/icons/primeng.svg" alt="PrimeNG logo" width="60">

PrimeNG est une bibliothèque riche en composants, souvent choisie pour sa couverture fonctionnelle étendue et son intégration rapide avec les évolutions d’Angular (Signals, composants standalone, SSR). Elle convient bien aux applications métier nécessitant de nombreux widgets prêts à l’emploi. Cependant, elle peut introduire une dette technique sur des projets complexes et certaines fonctionnalités avancées sont réservées à des offres commerciales.

**Points importants**
- Large gamme de composants avancés adaptés aux applications métier
- Bonne intégration avec les nouveautés Angular (Signals, SSR, standalone)
- Limites possibles sur des projets complexes (performances, theming, maintenance) et fonctionnalités premium sous abonnement

**Sources**
- [**Documentation officielle**](https://primeng.org/)
- [**Infragistics** PrimeNG Alternatives: What Library Fits Your Project](https://www.infragistics.com/blogs/primeng-alternatives/)
- [**Diggibyte** Why PrimeNG Remains My Go-To UI Library for Angular 19 in 2025](https://diggibyte.com/why-primeng-remains-my-go-to-ui-library-for-angular-19-in-2025/)

---

## 4. Paradigmes de programmation

Les langages et frameworks modernes combinent plusieurs manières d’organiser la logique d’un logiciel. Comprendre ces paradigmes permet de mieux structurer les applications, d’adapter l’architecture aux besoins métier et de choisir les approches les plus adaptées à Angular ou à Java.

### 4.0. Aperçu des paradigmes

**Impérative**
Style dans lequel le programme décrit explicitement, étape par étape, les opérations à effectuer et les changements d’état nécessaires pour atteindre un résultat.

**Orientée-objet**
Approche impérative structurée autour d’objets regroupant données et comportements. Elle favorise l’encapsulation (modifier l’implémentation interne sans impacter le reste du code) et facilite la réutilisation via l’héritage et le polymorphisme.

**Déclarative**
Approche où l’on décrit le résultat attendu plutôt que les étapes pour y parvenir. Le système sous-jacent détermine la manière d’obtenir ce résultat.

**Fonctionnelle**
Forme de programmation déclarative privilégiant les fonctions pures et l'immuabilité, afin de réduire les effets de bord et d’améliorer la prévisibilité du code. Elle permet des transformations de données plus simples, testables et sûres.

**Réactive**
Approche centrée sur des flux d’événements asynchrones où les mises à jour se propagent automatiquement. Elle est bien adaptée aux interfaces dynamiques et aux architectures non bloquantes.

### 4.1. Angular

<img src="assets/icons/angular.svg" alt="Angular logo" width="60">

#### 4.1.1. Paradigmes principaux

Angular adopte une approche **déclarative**, où les templates décrivent l’état attendu de l’interface, et une architecture orientée composants qui structure l’application en blocs cohérents et réutilisables. La programmation **réactive** est centrale, historiquement via RxJS (Observables, flux asynchrones) et aujourd’hui renforcée par Signals, qui assurent une propagation automatique et fine des changements d’état. Des éléments **fonctionnels** s’intègrent également : immutabilité encouragée dans le change detection, pipes purs, fonctions de transformation.

#### 4.1.2. Implications architecturales

- Interfaces hautement dynamiques (dashboards, applications collaboratives, e-commerce) :
  - Signals pour l’état local et la **réactivité** fine
  - RxJS pour les flux complexes (API multiples, WebSockets)
  - Services **réactifs** pour la coordination entre composants
- Applications transactionnelles (panier d'achat, réservations) :
  - État **réactif** pour les données utilisateur
  - Logique métier **fonctionnelle** pour les calculs purs et transformations immuables
- Formulaires avancés (portails administratifs, configuration produits, onboarding) :
  - Reactive Forms pour une approche **déclarative** et composable
  - Adaptée aux processus multi-étapes
- Applications modulaires et scalables (plateformes multi-tenant, portails avec nombreux modules métiers) :
  - Composants standalone
  - Lazy loading
  - Organisation par features pour maintenir lisibilité et évolutivité
- Applications Web progressives / Offline-first :
  - Synchronisation **réactive**
  - Stratégies de cache **déclaratives**
  - Séparation claire entre logique pure et effets

**Recommandations générales**
  - Utiliser les Signals comme primitive de **réactivité** par défaut
  - Réserver RxJS aux flux asynchrones complexes
  - Maintenir l’immutabilité dans les données
  - Privilégier la composition **fonctionnelle** pour une logique testable

### **4.2. Java**

<img src="assets/icons/java.svg" alt="Java logo" width="60">

#### 4.2.1. Paradigmes principaux

Java repose sur une base **orientée objet** et **impérative** : classes, encapsulation, héritage et polymorphisme structurent la modélisation métier. Depuis Java 8, le langage intègre des outils **fonctionnels** (lambdas, Streams API, Optional) permettant des transformations **déclaratives** et composables. La programmation **réactive** est accessible via des bibliothèques (Project Reactor, RxJava, Mutiny) pour des architectures non-bloquantes. De nombreux frameworks (Spring notamment) encouragent un style **déclaratif** via annotations et configuration, réduisant le code répétitif.

#### 4.2.2. Implications architecturales

- Architectures **réactives** et haute concurrence (APIs à fort trafic, microservices non-bloquants) :
  - Spring WebFlux + Reactor pour I/O non-bloquant
  - Backpressure natif pour la résilience
  - Immutabilité pour la prévisibilité
- Applications métier transactionnelles (e-commerce, réservations, systèmes financiers) :
  - Modélisation **orientée objet** du domaine (entités, agrégats)
  - Logique **fonctionnelle** pour calculs et règles métier composables
  - **Réactivité** pour notifications et mises à jour temps réel
- Systèmes orientés événements (architectures distribuées, messaging) :
  - Streams réactifs pour traitement d'événements (Kafka, RabbitMQ)
  - Handlers **fonctionnels** purs
  - Event sourcing avec logs immuables
- Applications traditionnelles CRUD (portails administratifs, backoffices) :
  - Spring MVC + Hibernate pour modèle **orienté objet** classique
  - Annotations **déclaratives** pour réduire le boilerplate
- Traitement de données et pipelines (batch, ETL, analytics) :
  - Streams API pour transformations **fonctionnelles** parallélisables
  - Collectors pour agrégations **déclaratives**
  - Vavr pour structures immuables persistantes
- Modernisation de systèmes legacy :
  - Introduction progressive de patterns **fonctionnels**
  - Facades **réactives** sur APIs synchrones
  - Découplage par événements

**Recommandations générales**
  - S'appuyer sur un socle **orienté objet** pour la modélisation du domaine
  - Enrichir avec des patterns **fonctionnels** pour la logique testable (immutabilité, composition)
  - N'introduire la **réactivité** complète que si justifié architecturalement (I/O intensif, haute concurrence)
  - Maintenir une cohérence de style par projet plutôt que mélanger les paradigmes sans raison claire