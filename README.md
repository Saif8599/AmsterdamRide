# AmsterdamRide

## Inhoudsopgave

  * [Beschrijving](#beschrijving)
  * [Kenmerken](#kenmerken)
  * [Functionaliteit](#functionaliteit)
  * [Installatie](#installatie)

## Beschrijving


## Kenmerken
In dit project heb ik gebruik gemaakt van Node.js en Express om een webserver te maken. Voor het genereren van dynamische HTML-pagina's is er gebruik gemaakt van Liquid, dit maakt de webpagina's flexibel en makkelijk te onderhouden maakt.

### Ontwerpkeuzes

**Routes & data**
- Homepagina "/" :
- Chaffeurs "/drivers" :
- About "/about" :
- Contact "/contact" :
- Register "/register" :

**UI States & Interacties**
Actieve Chaffeurs pagina :

- Loading state 
- Succes state

**Progressive Enhancement**
- 

## Javascript 
### Client-side fetch
Op de pagina van Chauffeurs kun je een chauffeur boeken doormiddel van een post form. Dit doe je door de book button te klikken. Zodra je hier op klikt krijg je en modal te zien. In de modal zit een form met invoer velden die nodig zijn voor het versturen. Met preventDefault() stopt de pagina refresh en speelt de loading state en de succes state. De "bevestig boeking" knop text word veranderd en er komt een checkmark animatie te zien op de driverCard.

https://github.com/user-attachments/assets/a731ea7d-9768-4474-980e-600eaedee96d

Er is gebruik gemaakt van feature detectie. Als fetch word ondersteunt door de browser voerd het deze code uit. Voor elke submit word de form getarget. Dit geldt alleen voor formulieren die enhanced zijn. Als ze niet geenhanced zijn dan krijg je een return. 

https://github.com/Saif8599/AmsterdamRide/blob/05245120eaab8f766d7a1df7d682dae1fb627bc9/views/partials/active-drivers.liquid#L430-L440

Daarna word de inner text van de button veranderd naar "Verwerken..". Dit om de gebruiker een feedback te geven wat er gebeurd met het form.

https://github.com/Saif8599/AmsterdamRide/blob/05245120eaab8f766d7a1df7d682dae1fb627bc9/views/partials/active-drivers.liquid#L441-L445

Hier word alle informatie van de formulier verzameld en verstuurt naar de server vie een fetch-request. Daarna word de oude formulier vervangen met een nieuwe versie.

https://github.com/Saif8599/AmsterdamRide/blob/05245120eaab8f766d7a1df7d682dae1fb627bc9/views/partials/active-drivers.liquid#L448-L465

Dit gedeelte zorgt voor de checkmark slide animatie als je een chauffeur hebt geboekt.

https://github.com/Saif8599/AmsterdamRide/blob/05245120eaab8f766d7a1df7d682dae1fb627bc9/views/partials/active-drivers.liquid#L471-L501

## Functionaliteit


## Installatie

1. **Clone de repository:**
   ```bash
   git clone https://github.com/Saif8599/AmsterdamRide.git
   ```
2. **Installeer de dependencies:**
   ```bash
   npm install
   ```
3. **Start de server:**
   ```bash
   npm start
   ```
4. **Toegang tot de applicatie:**
   - Open een browser en ga naar: `http://localhost:8000`
