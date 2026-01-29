## MVVM Compose -projekti (Week 3)

Tämä projekti on yksinkertainen tehtävienhallintasovellus, joka on toteutettu Jetpack Composella ja MVVM-arkkitehtuurilla.

### MVVM
- **Model**: sisältää datan (Task).
- **ViewModel**: hallitsee sovelluksen tilaa ja tarjoaa funktiot (addTask, updateTask, removeTask, toggleDone).
- **View**: Compose-näkymät, jotka näyttävät datan ja reagoivat tilamuutoksiin.

MVVM on hyödyllinen Composessa, koska UI päivittyy automaattisesti, kun ViewModelin tila muuttuu. Näin logiikka ja käyttöliittymä pysyvät selkeästi erillään.

### StateFlow
StateFlow on tilavirta, joka sisältää aina viimeisimmän arvon.  
ViewModel julkaisee tehtävälistan StateFlow’n kautta, ja Compose kuuntelee sitä `collectAsState()`-kutsulla.  
Kun tila muuttuu, UI päivittyy automaattisesti.

