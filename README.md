![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# LAB | Vue.js IronContacts (Composition API)

## Einführung

Nach Ironhack hast Du beschlossen, in der Filmindustrie zu arbeiten, und Du hast einen Job gefunden, bei dem Du die Kontakte eines berühmten Produzenten verwalten musst.

Deine Aufgabe besteht darin, eine Kontaktverwaltungs-App für den Produzenten mit Vue.js zu erstellen.

## Anforderungen

- Fork dieses Repo
- Clone dieses Repo
- Öffne das LAB und starte:

  ```bash
  $ cd lab-vue-c-ironcontacts
  $ npm install
  $ npm run dev
  ```

## Abgabe

- Wenn Du fertig bist, führe folgende Befehle aus:

  ```bash
  git add .
  git commit -m "done"
  git push origin main
  ```

- Erstelle einen Pull Request, damit Deine TAs Deine Arbeit überprüfen können.

## Loslegen

Reinige die `App.js` Komponente, damit sie die folgende Struktur hat:

```js
// src/App.vue
<template>
</template>

<script setup>
</script>

<style>
</style>
```

## Anleitung


### Iteration 1 | 5 Kontakte anzeigen

Schauen wir uns den Startercode an.

In der `src`-Ordner haben wir eine `contacts.json`-Datei, die die Kontakte des Produzenten enthält. Importiere die `contacts.json`-Datei in `App.vue`. Erstelle dann eine Ref-Variable namens `contacts` und speichere ein **Array mit den ersten 5 Kontakten** darin.

Zeige dieses Array von 5 Kontakten als Liste in einer `<table>` an und zeige das `Bild`, `Name` und `Beliebtheit` jedes Kontakts an.

Lass uns die Inhalte vorerst in `App.vue` rendern. Gehe deshalb nicht dazu über, eine dedizierte Komponente für die Kontaktliste zu erstellen. Lassen Sie uns vorerst alles einfach in einer Komponente rendern.

<!-- Der Grund wird etwas klarer, wenn wir den Löschbutton neben jedem Kontakt hinzufügen. Du bist wahrscheinlich noch nicht vertraut mit dem Konzept des "Liftens von State" und dem Übergeben von Callbacks als Props. Aus diesem Grund ist es besser, vorerst alles in einer Komponente zu rendern. -->

Lass uns weitermachen.

Um `contacts.json` in `App.vue` zu importieren, kannst Du folgendes verwenden:

```js 
import contacts from "./contacts.json"; 
```   
Am Ende dieser Iteration sollte deine Anwendung wie folgt aussehen:

<details>    
 <summary> Bild in der Iteration 1 überprüfen</summary>   

![Screenshot - Iteration 1](https://education-team-2020.s3.eu-west-1.amazonaws.com/web-dev/labs/lab-react-ironcontacts-1.png)

</details>   

### Iteration 2 | Bedingte Anzeige von Awards-Informationen

Der Produzent möchte die Informationen über die Auszeichnungen sehen, die ein Kontakt gewonnen hat.

Aktualisiere die Liste und füge am Ende der Tabelle zwei weitere Spalten "Won an Oscar" und "Won an Emmy" hinzu. Rendere dann bedingt ein Trophäen-Symbol :trophy: oder keinen Inhalt, abhängig von den Werten `wonOscar` und `wonEmmy` jedes Kontakts.

Nach Abschluss sollte deine Anwendung wie folgt aussehen:

<details> <summary> Bild in der Iteration 2 überprüfen </summary>   

![Screenshot - Iteration 2](https://education-team-2020.s3.eu-west-1.amazonaws.com/web-dev/labs/lab-react-ironcontacts-2.png)

</details>   

### Iteration 3 | Hinzufügen neuer zufälliger Kontakte

Erstelle in deiner Anwendung eine Schaltfläche "Add Random Contact". Jedes Mal, wenn du auf diese Schaltfläche klickst, sollte ein neuer zufälliger Kontakt zu den `contacts` hinzugefügt werden. Du solltest zufällige Kontakte aus den verbleibenden Kontakten erhalten, die noch nicht angezeigt werden.

Wähle zunächst zufällig einen Kontakt aus dem Array der verbleibenden Kontakte aus. Füge dann diesen Kontakt dem Array hinzu, der in deinem Daten-Ref (das ist das zuvor erstellte Array mit 5 Kontakten) lebt.

Am Ende dieser Iteration wird deine Website wahrscheinlich so aussehen:

<details>    
 <summary> Bild in der Iteration 3 überprüfen </summary>   

![Screenshot - Iteration 3](https://education-team-2020.s3.eu-west-1.amazonaws.com/web-dev/labs/lab-react-ironcontacts-3.png)

</details>   

### Iteration 4 | Kontakte nach Name und Popularität sortieren

Der Produzent hat dich gebeten, zwei neue Schaltflächen hinzuzufügen, um ihm beim Sortieren der Kontakte zu helfen. Wenn du auf eine der Schaltflächen klickst, sollte die Tabelle **nach `name`** (alphabetisch) bzw. nach `popularity` (höchste zuerst) sortiert werden.

Sobald du das Array sortiert hast, denke daran, die Referenzvariable zu aktualisieren, die die Kontakte enthält.

So sollte deine Anwendung am Ende dieser Iteration aussehen:

<details>    
 <summary> Bild in der Iteration 4 überprüfen </summary>   

![Screenshot - Iteration 4](https://education-team-2020.s3.eu-west-1.amazonaws.com/web-dev/labs/lab-react-ironcontacts-4.png)

</details>   

### Iteration 5 | Entfernen von Kontakten

Der Produzent möchte auch einige Kontakte entfernen. Implementiere einen _Löschen_ -Button in jeder Zeile deiner `<table>`, mit dem der Benutzer den angeklickten Kontakt entfernen kann.

Wenn der Benutzer auf den Button klickt, solltest Du die `id` des Schauspielers erhalten und verwenden, um den Kontakt aus dem Array zu entfernen. Vergiss nicht, die Referenzvariable zu aktualisieren, die die Kontakte hält, nachdem Du den Kontakt entfernt hast!

Wenn Du fertig bist, sollte Deine App so aussehen (nachdem Du ein wenig mit dem _Löschen_ -Button gespielt hast):

<details>    
 <summary> Bild in Iteration 5 überprüfen </summary>   

![Screenshot - Iteration 5](https://education-team-2020.s3.eu-west-1.amazonaws.com/web-dev/labs/lab-react-ironcontacts-5.png)

</details>   

Leider ist diese Kontaktliste nicht bereit für die Produktion. Wir sind im Filmgeschäft! Es muss funkeln! Füge etwas schönes CSS hinzu, um die App auffälliger zu machen.

<br>  

**Viel Spaß beim Coden!** :heart: