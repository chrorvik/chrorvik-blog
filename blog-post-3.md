---
layout: post-layout.njk 
title: .gitignore
date: 2021-04-22
tags: ['post']
---
<!-- Excerpt Start -->
Legger inn et par triks og tips om gitignore
<!-- Excerpt End -->
 
 ## Push mappe, men ikke innhold
For å legge inn mappe men ikke innhold, kan du opprette en .gitignore i mappen som du ønsker å bli med og skriv følgende:

```
# Ignorer alt i mappen
*
# Med unntak av denne filen
!.gitignore
```

## Fjerne innhold som allerede er pushet
1. Opprett .gitignore fil
2. Legg inn mappen eller filen som ikke skal være med (f.eks. node_modules)
3. I terminal skriv følgende:

```
git rm -r --cached .
git add .
git commit -m "fjernet gitignore filer"
git push
```
*Stor NB: om du har pushed data med sensitiv innhold, vil ikke dette angre det.*  