## Générer le site localement avec Jekyll

### Prérequis

[Installer ruby et Jekyll](https://jekyllrb.com/docs/installation/)

### Installer les dépendances du projet

Se déplacer à la racine du projet puis

```sh
bundle install
```

### Démarrer le serveur de développement

```sh
bundle exec jekyll serve --safe
```

> `bundle exec` vous assure que la version de jekyll utilisée est celle spécifiée dans le fichier `Gemfile.lock`.

> L'option `--safe` permet d'avoir le même comportement que sur les serveurs de build de Github Pages. Ainsi pas de surprise lors du déploiement.

```
Generating... 
                   done in 0.124 seconds.
Auto-regeneration: enabled for '/home/emak/code/societenumerique.github.io'
Server address:    http://127.0.0.1:4000
Server running...  press ctrl-c to stop.
```

Visiter l'url : <http://localhost:4000>

> Le site est généré dans le dossier `_site` qui est ignoré par git.

> Le site est automatiquement regénéré lorsqu'un fichier source est édité (`_layouts`, `_includes`, `_topics`, etc). Il suffit de rafraichir la page pour voir les changements.

### Mettre à jour les dépendances

Comme la gem `github-pages` est mise à jour régulièrement, il est conseillé de mettre à jour les dépendances (gems) de temps en temps:

```sh
bundle update
```

## Documentation utile

* [Jekyll](https://jekyllrb.com/docs/home/), générateur de site statique
* [Liquid](https://shopify.github.io/liquid/), language de templating utilisé par Jekyll
* [Github Pages Basics](https://help.github.com/categories/github-pages-basics/)
* [Customizing Github Pages](https://help.github.com/categories/customizing-github-pages/)
