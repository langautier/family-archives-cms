# Need a CMS to make available old family's letters and photos

Web pages are ultimately the best way:
- to provide hundred pages as a mix of scanned documents, text and photos
- to gradually build it up over years

As a result, please have a look in [Archives Langautier](http:langautier.free.fr)

## Documents as image/text and photos in a same page

Transcription of a daily page next to the page scan and a photo relating to the text

![Image doc](https://github.com/langautier/family-archives-cms/blob/master/Documents.png)

## Timeline
The timeline is a great way to tell the story of the family. The fold-out menu allows you to open and close the details of a related family.

![Image frises](https://github.com/langautier/family-archives-cms/blob/master/Frises.png)

## Photos gallery
This responsive photo gallery is built from CSS grid. It allows having photos from differents width or height.

![Image frises](https://github.com/langautier/family-archives-cms/blob/master/Gallery.png)

## Google pages with my own marks

![Image carte](https://github.com/langautier/family-archives-cms/blob/master/Carte.png)

# VBA/Word based CMS Application
Our CMS allows:
- to associate text with each document
- to build pages from a collection of documents made of images and text
- to group the pages to make up the story of the individuals within their families
- allow navigation in the pages associated with each family

## Transcribe scanned documents into text

Use Word to view the document and transcribe the text with the dual display managed by Word and also benefiting from Word's spell checker.

You will not have to manage the HTML code either, Word will do it for you by transforming your layout into HTML instructions

![Image carte](https://github.com/langautier/family-archives-cms/blob/master/Creation%20Fichier%20HTM.png)

## XML file associated with each scanned document

The trick is not to use a database, but only files in directories and to associate with each scanned document an XML file giving everything there is to know about it.

```HTML
Html\Tailleur\1915\V0f_190821-2139_086.jpg=	Nam:|
<paramdesc img="src:1383x1900+24; web:582x800+24; th:56x80+24;" key="row-class:blog; thumb; th:56x80;"/>
<float>
<p class="text-right">Le 27 février 1915</p>
<p class="text-center">Bien chers parents</p>
<p>Un petit mot bien vite. L’homme de corvée qui emporte les lettres est là à côté de moi qui attend pour emporter les baisers que je vous envoie.</p>
<p class="pl-5">Prosper</p>
</float>
```
# XML file associated with each photo
All the information to build the photo gallery are embedded within the XML file associated with the photo. Button command allows to modify it without having to compute thumb size or aspect ratio needed to properly build the wall.

![Image carte](https://github.com/langautier/family-archives-cms/blob/master/Gallery%20XML.png)

# Site description
```HTML
<menu>
  <famillemenu>Pebernad</famillemenu>
  <color>#F3E0F3 Magenta DarkMagenta Color</color>
  <prefix>P</prefix>
    <niv0>
      <libniv0>Pebernad de Langautier</libniv0>
      <famille>Pebernad de Langautier</famille>
      <niv1>
        <rep>Accueil</rep>
        <lib>Pebernad de Langautier</lib>
        <titre>Pebernad</titre>
        <miseajour><note><date>2018-10-30</date><content>Refonte de la page à l'occasion de l'introduction de la frise à tiroir</content></note><note><date>2015-02-23</date><content>Création de la page</content></note></miseajour>
        <prefix>Al2</prefix>
      </niv1>
    </niv0>
</menu>
 ```
