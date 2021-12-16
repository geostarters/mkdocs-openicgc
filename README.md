# Projecte MkDocs

Projecte de test usant [Mkdocs](https://www.mkdocs.org/) com a eina de documentació i [GitHub Pages](https://pages.github.com/) com a eina de publicació:  

https://geostarters.github.io/mkdocs-openicgc/    


## 1. Instal·lació Mkdocs en local

Instal·lem Mkdocs:
```
pip install mkdocs
```    

## 2. Creació inicial del projecte

Creem una carpeta en qualsevol directori del nostre ordinador on emmagtzemarem tots els fitxers del projecte:

```
mkdocs new NOM_DEL_PROJECTE
cd NOM_DEL_PROJECTE
```    

## 3. Inicialització del servidor virtual

Iniciem el servidor Mkdocs:

```
mkdocs serve
```

Accedim a http://127.0.0.1:8000 per veure el nostre projecte local des del navegador.      


## 4. Configuració

Els fitxers font de la documentació s'escriuen a Markdown i es configuren amb un únic fitxer de configuració YAML:

* Creem les pàgines .md de contingut.
* Escollim un [theme](https://www.mkdocs.org/user-guide/choosing-your-theme/).
* Afegim els [pluguins](https://www.mkdocs.org/dev-guide/plugins/) que desitgem.    


## 5. Publicació amb GitHub pages

Creem un nou repositori al GitHub on pujarem el nostre projecte fent servir Git.  

Mitjançant el terminal, ens situem dins de la carpeta local que conté els arxius i executem:

```
python -m mkdocs build
```

Inicialitzem el repositori local i fem el nostre primer commit usant les ordres habituals:

```
git init
site/ > .gitignore
git add .
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/geostarters/mkdocs-openicgc.git
git push -u origin main
mkdocs gh-deploy
```  

Si tot ha anat bé, la web s'haurà creat i la consola mostrarà el següent missatge final:  
_Your documentation should shortly be available at:_ https://geostarters.github.io/mkdocs-openicgc/    


## 6. Actualització

Per actualitzacions, canvis, modificacions, afegir contingut, etc:

* Creem una nova branch i la clonem des del nostre ordinador (usem SourceTree)
* Fem els canvis que vulguem des de l'editor (usem Visual Studio Code)
* Pujem els canvis a partir de les següents ordres:   

```
git commit -m "NOM_DEL_COMMIT"
git push -u origin NOM_DE_LA_BRANCH
mkdocs gh-deploy
```  

Si tot ha anat bé, la consola mostrarà el següent missatge final:  
_Your documentation should shortly be available at:_ https://geostarters.github.io/mkdocs-openicgc/  
