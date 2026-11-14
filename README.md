# Mes recettes

Petit site de recettes perso, pensé pour une tablette en plein écran (une recette = un écran).

Site : https://chkerms.github.io/Recettes/

## Fichiers

- `index.html` : le site (recherche, filtres, portions, mode cuisine).
- `recettes.js` : toutes les recettes (une entrée par recette).
- `manifest.webmanifest` + `icon.svg` : permet d'« Ajouter à l'écran d'accueil » pour ouvrir le site en plein écran.

## Format d'une recette

```json
{
  "id": "saucisse-fumee",
  "titre": "Saucisse fumée",
  "categorie": "Viande",
  "portions": 4,
  "temps": 15,
  "ingredients": [
    {"q": 250, "u": "g", "p": "de fusilli"},
    {"q": 2, "s": "gousse d'ail émincée", "p": "gousses d'ail émincées"},
    {"q": null, "p": "Parmesan râpé, pour servir"}
  ],
  "etapes": ["…", "…"],
  "photo": "IMG_20181227_191716.jpg"
}
```

- `q` quantité (null si aucune), `u` unité (g, kg, cl, ml, l), `p` texte au pluriel, `s` texte au singulier.
- `categorie` : Viande, Poisson, Veggie ou Fromage.
- `photo` : photo source déjà traitée (sert à l'automatisation pour ne pas traiter deux fois la même).
