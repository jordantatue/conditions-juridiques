# Conditions juridiques — Jordan Tatue

Site statique hébergeant les documents juridiques de mes applications :
politique de confidentialité, conditions d'utilisation et politique de
suppression des données. Il sert de source aux URL exigées par les plateformes
développeur **Meta** et **TikTok**.

🔗 **https://jordantatue.github.io/conditions-juridiques/**

## URLs à renseigner sur les plateformes

| Champ | URL |
| --- | --- |
| Privacy Policy URL | `https://jordantatue.github.io/conditions-juridiques/privacy.html` |
| Terms of Service URL | `https://jordantatue.github.io/conditions-juridiques/terms.html` |
| Data Deletion Instructions URL (Meta) | `https://jordantatue.github.io/conditions-juridiques/data-deletion.html` |

Les versions françaises vivent sous `/fr/` et sont reliées aux pages anglaises
par un sélecteur de langue.

> ⚠️ **Ne mets pas ce site dans le champ « Website URL » de TikTok.** TikTok
> exige que cette URL soit le site de ton application, « entièrement
> développé », et refuse explicitement une page d'accueil vide. Ce dépôt ne
> fournit que les documents juridiques. Le site de ton application devra
> afficher des liens vers `privacy.html` et `terms.html` **visibles sans
> ouvrir de menu**, condition posée noir sur blanc par la revue TikTok.

## Vérification d'URL TikTok

TikTok demande de prouver que tu contrôles le domaine avant la soumission. Il
fournit un fichier de vérification à déposer à la racine du site : commite-le
à la racine du dépôt, pousse, et il sera servi à
`https://jordantatue.github.io/conditions-juridiques/<nom-du-fichier>.txt`.

> GitHub Pages sert le site sous le chemin `/conditions-juridiques/`, pas à la racine du
> domaine `jordantatue.github.io`. Si TikTok exige une vérification à la racine
> du domaine, il faudra passer par un dépôt `jordantatue.github.io` ou un nom
> de domaine personnalisé.

## Structure

```
.
├── index.html              Accueil — liens légaux visibles sans menu (exigence TikTok)
├── privacy.html            Politique de confidentialité
├── terms.html              Conditions d'utilisation
├── data-deletion.html      Procédure de suppression des données
├── fr/                     Mêmes pages en français
├── assets/style.css        Feuille de style unique
└── .nojekyll               Désactive le traitement Jekyll de GitHub Pages
```

Aucune dépendance, aucune étape de build : les fichiers sont servis tels quels.

## Modifier le contenu

Chaque document existe en deux exemplaires, anglais et français. **Modifie
toujours les deux**, sinon les versions divergent.

| Document | Anglais | Français |
| --- | --- | --- |
| Confidentialité | `privacy.html` | `fr/privacy.html` |
| Conditions | `terms.html` | `fr/terms.html` |
| Suppression | `data-deletion.html` | `fr/data-deletion.html` |

Pense à mettre à jour la date dans le bloc `pagehead-meta` des deux versions.

## À adapter avant soumission

Ces documents décrivent des pratiques. Ils ne te protègent que si elles
correspondent à la réalité de tes applications. Vérifie en particulier :

- les **durées de conservation** (section 8 de la politique de confidentialité) ;
- la **localisation de l'hébergement** (section 7) — à corriger si ton
  hébergeur est hors Union européenne ;
- les **étapes de suppression dans l'application** (`data-deletion.html`,
  option 1) — elles doivent exister réellement dans ton interface ;
- le **plafond de responsabilité** des conditions d'utilisation (section 10).

## Licence

Contenu adapté des [politiques open-source de Basecamp](https://github.com/basecamp/policies),
publiées sous [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
L'attribution figure en pied de chaque page, comme la licence l'exige.
