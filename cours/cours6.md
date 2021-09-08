# Question au boss

Yo ma poule petite question

---

En gros je voudrais déposer plusieurs images sur un serveur distant.


## Method POST

Donc la je pense je devrais faire un champ "html input file multiple" et déposer mes 200 images

```cmd
    https://api.nakala.fr/datas/uploads

```

Avec cette clés d'API

> 00a5d07c-dfac-9351-8b0e-fe1eafcde451


## Method GET

Une fois les images téléchargés elles sont contenus dans un espace temporaire pendant 24 heures 

On peut voir les différentes images avec une requète GET

```cmd
    https://api.nakala.fr/datas/uploads

```


## POST DATA

Pour que l'image soient pérennes il faut créer une donnée référencée et lui ajouter le lien de notre image temporaire

```cmd
    https://api.nakala.fr/datas

```



Et il faut lui rentrer un object :

```json
 {
  "status": "published",
  "metas": [
    {
      "value": "string",
      "lang": "string",
      "typeUri": "string",
      "propertyUri": "string"
    }
  ],
  "files": [
    {
      "sha1": "string",
      "description": "string",
      "embargoed": "string"
    }
  ],
  "collectionsIds": [
    "string"
  ],
  "rights": [
    {
      "id": "b55e770c-849b-11ea-87ea-0242ac1b0003",
      "role": "ROLE_READER"
    }
  ]
}
```


Donc J'aimerai faire une boucle pour récupérer les données du get data/uploads et faire des post /data