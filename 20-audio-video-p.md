---
layout: page
title: Audio, Video, Images
permalink: /html/audio-video-images/
---

Les balises image, picture, figure, audio et video

La balise Figure
===

Exemple d'utilisation:

~~~
<figure>
    <img src="monchat.jpg" alt="Un chat faisant la sieste.">
    <figcaption>Voici une photo de mon chat.</figcaption>
</figure>
~~~

Images responsives
===

`<picture>` ... élément permettant des images responsives, alternative à `<img>`.

Exemple de code:

~~~
<picture>
  <source 
    media="(min-width: 650px)"
    srcset="images/kitten-stretching.png">
  <source 
    media="(min-width: 465px)"
    srcset="images/kitten-sitting.png">
  <img 
    src="images/kitten-curled.png" 
    alt="a cute kitten">
</picture>
~~~

Et voici un autre exemple trouvé sur le site [sketchapp.com](https://www.sketchapp.com/features/). On notera qu'il utilise le format [WebP](https://fr.wikipedia.org/wiki/WebP), nouveau format compressé développé par Google.

~~~
<picture>
  <source 
   srcset="/images/features/mirror.webp 1x,
   /images/features/mirror@2x.webp 2x" 
   type="image/webp">
  <img src="/images/features/mirror-png8.png" 
   srcset="/images/features/mirror-png8@2x.png 2x">
</picture>
~~~

Enfin, une méthode trouvée sur [un site de Google](https://design.google.com/articles/introducing-pixate-and-form-1-3/) en novembre 2016: 

~~~
<div class="_image js-responsive-image loaded" data-knowndimensions="1600x1050" data-preserveaspectratio="true" data-src="form.jpg" data-target="#fig-2" style="background-image: url(&quot;form-1240@2x.jpg&quot;);"></div>
~~~

On notera qu'il n'y a pas de balise image (<img>), l'image est affichée comme image de fond en css (background-image).

## Références sur les images responsives

- [http://caniuse.com/#feat=picture](http://caniuse.com/#feat=picture)
- [https://github.com/scottjehl/picturefill - un polyfill]()
- [https://responsiveimages.org/](https://responsiveimages.org/)