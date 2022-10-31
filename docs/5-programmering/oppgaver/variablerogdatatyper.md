---
title: "Oppgaver: Variabler og datatyper"
sidebar_position: 1
sidebar_label: Variabler og datatyper
description: "Oppgaver: Varabler og datatyper"
---

# Variabler og Datatyper

## Oppgave 1.1

Print ut noen selvvalgte beskjeder. Prøv å se hva som skjer dersom du glemmer anførselstegnene.

## Oppgave 1.2 

a) Hva tror du skjer dersom vi kjører følgende kode? 

```python
a = 2
print(a + 2)
``` 

b) Hvorfor er det ingen anførselstegn i print-instruksjonen denne gangen?

<details>
    <summary>Klikk for løsning</summary>

Koden printer ut 4. Vi kan ikke bruke anførselstegn fordi det ikke er en streng vi skal printe ut.

</details>

## Oppgave 1.3

Se på følgende kode:

```python
lengde = 5
bredde = 7

areal = lengde*bredde

print("Arealet av rektangelet er", areal)
```
Hvorfor bruker vi variable for lengde og bredde? Kunne vi ikke bare ha skrevet arealet rett inn i print-funksjonen?

<details>
<summary>Klikk for løsning</summary>

Variabler gir bedre oversikt når man leser koden. Dersom man ønsker å regne areal for et annet rektangel er det mye lettere å endre på verdien på variablene enn å gå inn i resten av koden for å endre på tallene. Dette blir spesielt viktig jo større koden er.

</details>

## Oppgave 1.4

Spør den du sitter nærmest om alder. Lagre både navn og alder i to forskjellige variabler. Print en tekst som skriver ut følgende tekst rikig: Hei *navn*, du er *alder* år.

<details>
<summary>Klikk for hint</summary>

Lag et input-felt for navn og alder. Husk komma i mellom strenger og variable når du printer ut.

</details>

<details>
<summary>Klikk for løsning</summary>

```python
navn = input("Hva heter du? ")
alder = input("Hvor gammel er du? ")

print("Hei", navn, "du er", alder, "år")
```

</details>

## Oppgave 1.5

Lag et program som ber om to tall. Programmet skal deretter regne ut differansen mellom de to tallene og skrive ut svaret. Her er et eksempel på hvordan en kjøring av programmet kan se ut:

```
Oppgi verdien til x: 25
Oppgi verdien til y: 19
Differansen mellom x og y er 6.
```

<details>
<summary>Klikk for hint</summary>

Husk at det som bruker skriver inn alltid blir tekst, du må konvertere til flyttall (float) eller heltall (int). Eks: `float(input("Oppgi verdien til x: "))`

</details>

<details>
<summary>Klikk for løsning</summary>

```python
x = float(input("Oppgi verdien til x: "))
y = float(input("Oppgi verdien til y: "))
diff = x - y
print("Differansen mellom x og y er ", diff)
```

</details>

## Oppgave 1.6

![oppgave 5](../bilder/oppgave_5.png)

a) Forklar hva som er galt med denne koden. Hvorfor blir det feil? Rett opp koden slik at den kjører.

b) Skriv adressen ut på følgende to måter ved å bruke variabler: "Adressen er Kongens gate 432b" og "Gaten er Kongens Gate, husnummeret er 432, oppgang b" 

<details>
<summary>Klikk for løsning</summary>

a) I linje 3 er b skrevet uten anførselstegn. Da leter programmet etter en variabel som heter `b`, som ikke finnes.

b)

```python
gate = "Kongens gate"
husnr = "432"
oppgang = "b"

print("Adressen er", gate + husnummer + oppgang)
print("Gaten er", gate, ", husnummeret er", husnr, "oppgang", oppgang)
```

</details>

## Oppgave 1.7

Du er på restaurant med venner, og på regningen er følgende informasjon:

Total pris for mat og drikke: 850 kr<br />
Ungdomsrabatt: 25 %<br />
Tips: 10 %

a) Legg informasjonen inn i variabler som tall (ikke bruk %, det gir ikke mening når vi programmerer)

b) Bruk variablene for total pris og ungdomsrabatt til å regne ut rabatten.

c) Trekk fra rabatt og bruk så variabelen for tips til å regne ut tips. 

d) Legg på tips, og skriv ut summen for måltidet etter både rabatt og tips 

e) Lag en variabel for antall personer, og skriv ut pris per person samt antall personer.

<details>
<summary>Klikk for hint</summary>
<p>

- Lag de tre variablene
- Husk prosentformlene: pris*rabatt/100 gir selve rabatten
- Lag egne variabler for alle mellomregningen.
- Bruk mellomregningene til å regne ut det som skal betales
- Print ut alle variabler du er usikre på underveis så er det lettere å finne ut om matematikken stemmer

</p>
</details>


<details><summary>Klikk for løsning</summary>

```python
# Her regner vi tips før rabatt, man kan argumentere for at det kan gjøres motsatt

pris = 850
rabatt_prosent = 25
tips = 10
ant_pers = 3

rabatt_kr = pris*rabatt_prosent/100
tips_kr = pris*tips_kr

totalt = pris - rabatt_kr + tips_kr/100
per_pers = totalt/ant_pers

print("Pris etter rabatt og tips er", totalt, "det blir", per_pers, "kr per person")
```

</details>

## Oppgave 1.8

Formelen for å regne Fahrenheit om til Celsius er `C = (F-32)*5/9`. Lag et program som spør brukeren om temperaturen i fahrenheit. Regn om til Celsius og skriv en beskjed som sier hvor mange grader Celsius det tilsvarer. 

<details>
<summary>Klikk for hint</summary>

- Lag en input som tar inn temperatur, husk å gjøre om til desimaltall
- Regn ut Celsius med formelen, lagre i en ny variabel
- Skriv ut variabelen sammen med input variabelen i en passende tekst

</details>


<details>
<summary>Klikk for løsning</summary>

```python
f_heit = float(input("Hvor mange Fahrenheit? "))
celsius = (f_heit-32)*5/9

print(f_heit, "Fahrenheit tilsvarer, celsius, "grader Celsius")
```

</details>

## Oppgave 1.9

Endre på koden i oppgave 1.7 slik at alle variablene skrives inn som input, det vil si at vi selv kan velge totalpris, rabatt, tips og antall personer 

<details>
<summary>Klikk for løsning</summary>

```python
pris = float(input("Hva kostet måltidet? "))
rabatt_prosent = float(input("Har du eventuell rabatt? "))
tips = float(input("Vil du gi tips (oppgi i prosent) "))
ant_pers = float(input("Hvor mange er dere? "))

rabatt_kr = pris*rabatt_prosent/100
tips_kr = pris*tips_kr

totalt = pris - rabatt_kr + tips_kr/100
per_pers = totalt/ant_pers

print("Pris etter rabatt og tips er", totalt, "det blir", per_pers, "kr per person")
```

</details>

## Oppgave 1.10

**HANDLETUR**

Lag et program som regner ut totalpris for en bruker etter å ha vært på handletur. De varene det er mulig å kjøpe er brød, melk, ost og yoghurt.

Prisene er som følger:

Brød: 20 kr.<br />
Melk: 15 kr.<br />
Ost: 40 kr.<br />
Yoghurt: 12 kr.

Eksempel på bruk av programmet:
```
Hei! Velkommen til IT-butikken.
Hvor mange brød vil du ha?
> 2
Hvor mange melk vil du ha?
> 1
Hvor mange ost vil du ha?
> 1
Hvor mange yoghurt vil du ha?
> 3
Du skal betale: 131 kr.
```

<details>
<summary>Klikk for løsning</summary>

```python
#priser
brød = 20
melk = 15
ost = 40
youghurt = 12

# handling
print("-- Velkommen til IT-butikken --")
print("Hvor mange brød vil du ha?")
ant_brød = int(input("> "))
print("Hvor mange melk vil du ha?")
ant_melk = int(input("> "))
print("Hvor mange oster vil du ha?")
ant_ost = int(input("> "))
print("Hvor mange yoghurt vil du ha?")
ant_yoghurt = int(input("> "))

# utregning av pris
pris = brød * ant_brød + melk * ant_melk + ost * ant_ost + youghurt * ant_yoghurt
print("Du skal betale ", pris, " kr.")
print("-- Takk for handelen --")
```

</details>