---
title: Python spiekbrief
---

# 1 Invoer en uitvoer
Het doel van **invoer** en **uitvoer** is om interactie met de gebruiker mogelijk te maken en gegevens te verwerken binnen een programma.

| **Functie**          | **Beschrijving**                                             | **Voorbeeld**                      |
| -------------------- | ------------------------------------------------------------ | ---------------------------------- |
| `print()`            | Geeft uitvoer weer naar de console                           | `print("Hallo!")`                  |
| `input()`            | Verkrijgt invoer van de gebruiker (altijd als string)        | `naam = input("Wat is je naam? ")` |
| `int()`              | Zet een string om naar een geheel getal                      | `leeftijd = int(input())`          |
| `float()`            | Zet een string om naar een kommagetal                        | `prijs = float(input())`           |
| `str()`              | Zet een getal of object om naar een string                   | `str(leeftijd)`                    |
| f-strings (`f"..."`) | Formatteerbare string voor makkelijk invoegen van variabelen | `print(f"Hallo, {naam}!")`         |

## 1.1 Samengestelde tekst (concatenatie)
```python
naam = input("Wat is je naam?")
leeftijd = input("wat is je leeftijd?") 
print("Hallo, mijn naam is " + naam + " en ik ben " + str(leeftijd) + " jaar oud.")
```

# 2 Variabelen
Het doel van een **variabele** is om gegevens op te slaan die tijdens de uitvoering van een programma kunnen worden gebruikt, gewijzigd of opgehaald. Variabelen dienen als container voor verschillende soorten gegevens, zoals getallen, tekst of objecten, en geven deze gegevens een naam die kan worden aangeroepen wanneer dat nodig is. Ze maken het mogelijk om dynamisch met gegevens te werken en je programma flexibel en efficiënt te maken.

Een `integer` is een geheel getal zonder decimalen.
Een `float` is een getal met een decimale punt.
Een `string` is een reeks tekens, zoals letters, cijfers, symbolen of woorden, die als tekst wordt behandeld in een programmeertaal.
Een `boolean` is een gegevenstype dat slechts twee mogelijke waarden heeft: **true** (waar) of **false** (onwaar).

```python
x = 5           # Integer
y = 3.14        # Float
name = "Anna"   # String
is_student = True  # Boolean
```

# 3 Datatypes
Het doel van **datatypes** is om de aard en het soort gegevens die een variabele kan bevatten te definiëren. Ze bepalen hoe de gegevens worden opgeslagen, verwerkt en welke bewerkingen erop kunnen worden uitgevoerd. Door het juiste datatype te kiezen, kan Python efficiënt omgaan met verschillende soorten informatie, zoals tekst, getallen, lijsten, booleaanse waarden, enzovoort.

- **Numbers:** `int`, `float`, `complex`
- **Text:** `str`
- **Booleans:** `True`, `False`
- **Lists:** `my_list = [1, 2, 3]`
- **Tuples:** `my_tuple = (1, 2, 3)`
- **Dictionaries:** `my_dict = {"key": "value"}`
- **Sets:** `my_set = {1, 2, 3}`

# 4 Wiskundige Operatoren
Het doel van **wiskundige operatoren** is om numerieke berekeningen uit te voeren, zoals optellen, aftrekken, vermenigvuldigen, delen, en meer. Ze worden gebruikt om wiskundige bewerkingen op getallen uit te voeren en kunnen helpen bij het verwerken van cijfers in programma's.

| Operator | Beschrijving              | Voorbeeld | Resultaat |
| -------- | ------------------------- | --------- | --------- |
| `+`      | Optelling                 | `3 + 5`   | `8`       |
| `-`      | Aftrekking                | `10 - 4`  | `6`       |
| `*`      | Vermenigvuldiging         | `2 * 3`   | `6`       |
| `/`      | Deling                    | `8 / 2`   | `4.0`     |
| `//`     | Gehele deling (floor)     | `7 // 2`  | `3`       |
| `%`      | Modulus (rest bij deling) | `7 % 3`   | `1`       |
| `**`     | Machtsverheffing          | `2 ** 3`  | `8`       |

## 4.1 Prioriteit van Operatoren (Volgorde)
Python volgt **PEMDAS**:
1. **P**arentheses (haakjes): `(3 + 2) * 5`
2. **E**xponents (machtsverheffing): `2 ** 3`
3. **MD** Multiplication/Division (van links naar rechts): `10 / 2 * 5`
4. **AS** Addition/Subtraction (van links naar rechts): `5 + 3 - 2`

**Voorbeeld:**
```python
result = 3 + 2 * 2 ** 3 / 4 - 1
# Uitwerking:
# 1. Macht: 2 ** 3 = 8
# 2. Vermenigvuldiging: 2 * 8 = 16
# 3. Deling: 16 / 4 = 4
# 4. Optelling: 3 + 4 = 7
# 5. Aftrekking: 7 - 1 = 6
print(result)  # Output: 6.0
```

# 5 Relationele Operatoren
Het doel van **relationele operatoren** is om twee waarden met elkaar te vergelijken en een booleaanse waarde (`True` of `False`) te retourneren, afhankelijk van de uitkomst van de vergelijking. Deze operatoren helpen bij het maken van voorwaarden en beslissingen in je code.

| Operator | Beschrijving              | Voorbeeld | Resultaat |
| -------- | ------------------------- | --------- | --------- |
| `==`     | Gelijk aan                | `5 == 5`  | `True`    |
| `!=`     | Niet gelijk aan           | `5 != 5`  | `False`   |
| `>`      | Groter dan                | `8 > 2`   | `True`    |
| `<`      | Kleiner dan               | `8 < 2`   | `False`   |
| `>=`     | Groter dan of gelijk aan  | `6 >= 6`  | `True`    |
| `<=`     | Kleiner dan of gelijk aan | `1 <= 6`  | `True`    |

## 5.1 Belangrijk verschil!
Met `=` pas je een waarde aan, terwijl je met `==` alleen controleert of iets gelijk is.
### 5.1.1 `=` (toekenningsoperator)
De **enkele gelijkheidsteken** wordt gebruikt om een **waarde toe te wijzen** aan een variabele.  
Bijvoorbeeld: Hier wordt `5` opgeslagen in de variabele `x`.

```python
x = 5  # Wijs de waarde 5 toe aan de variabele x
print(x) # 5
```
### 5.1.2 `==` (vergelijkingsoperator)
De **dubbele gelijkheidsteken** wordt gebruikt om **twee waarden te vergelijken**. Het controleert of de waarden aan beide kanten van de operator **gelijk zijn** en retourneert een boolean (`True` of `False`).  Bijvoorbeeld:

```python
x = 5
y = 10
print(x == y)  # Controleer of x gelijk is aan y (uitvoer: False)
```

# 6 Ingebouwde functies
Deze ingebouwde functies maken het mogelijk om veelvoorkomende berekeningen snel en efficiënt uit te voeren zonder dat je extra code hoeft te schrijven.

| Functie        | Omschrijving                               | Voorbeeld                         |
| -------------- | ------------------------------------------ | --------------------------------- |
| `abs()`        | Geeft de absolute waarde van een getal     | `abs(-3)` → `3`                   |
| `round()`      | Rondt een getal af                         | `round(5.678, 1)` → `5.7`         |
| `max()`        | Geeft het grootste getal uit een collectie | `max([1, 2, 3])` → `3`            |
| `min()`        | Geeft het kleinste getal uit een collectie | `min([1, 2, 3])` → `1`            |
| `sum()`        | Berekent de som van een lijst van getallen | `sum([1, 2, 3])` → `6`            |
| `len()`        | Geeft het aantal items in een object       | `len("Hallo")` → `5`              |
| `pow()`        | Berekent de macht van een getal            | `pow(2, 3)` → `8`                 |
| `divmod()`     | Geeft quotiënt en rest van een deling      | `divmod(9, 4)` → `(2, 1)`         |
| `isinstance()` | Controleert het type van een object        | `isinstance(10, int)` → `True`    |
| `sorted()`     | Sorteert een lijst                         | `sorted([3, 1, 4])` → `[1, 3, 4]` |

# 7 Importeren van een library
Het doel van het importeren van een **library** is om toegang te krijgen tot vooraf geschreven code die specifieke functionaliteiten biedt, zoals wiskundige berekeningen, bestandsbeheer, netwerkcommunicatie, of data-analyse. Dit bespaart tijd en moeite doordat je niet zelf alles hoeft te programmeren, en je kunt eenvoudig gebruikmaken van de geoptimaliseerde en goed geteste functies die de bibliotheken bieden.
## 7.1 De `math`-bibliotheek in Python
In Python gebruik je de **`math`-bibliotheek** als je wiskundige functies nodig hebt, zoals kwadraten, vierkantswortels of goniometrie.

Om de bibliotheek te gebruiken, schrijf je eerst bovenaan je programma:

```python
import math
```

Daarna kan je allerlei handige functies gebruiken met `math.` ervoor.
### 7.1.1 Veelgebruikte functies in `math`

|Functie|Wat doet het?|Voorbeeld|
|---|---|---|
|`math.sqrt(x)`|De **vierkantswortel** van `x`|`math.sqrt(9)` ➝ `3.0`|
|`math.pow(x, y)`|`x` tot de macht `y`|`math.pow(2, 3)` ➝ `8.0`|
|`math.sin(x)`|**Sinus** van een hoek in **radialen**|`math.sin(math.pi/2)` ➝ `1.0`|
|`math.cos(x)`|**Cosinus** van een hoek in **radialen**|`math.cos(0)` ➝ `1.0`|
|`math.tan(x)`|**Tangens** van een hoek in **radialen**|`math.tan(math.pi/4)` ➝ `1.0`|
|`math.radians(x)`|Zet graden om naar radialen|`math.radians(90)` ➝ `1.57...`|
|`math.degrees(x)`|Zet radialen om naar graden|`math.degrees(math.pi)` ➝ `180.0`|
|`math.pi`|De waarde van π (pi)|`math.pi` ➝ `3.14159...`|
|`math.e`|De wiskundige constante **e**|`math.e` ➝ `2.71828...`|
|`math.floor(x)`|Rondt **af naar beneden**|`math.floor(3.7)` ➝ `3`|
|`math.ceil(x)`|Rondt **af naar boven**|`math.ceil(3.1)` ➝ `4`|

# 8 Condities 
## 8.1 `if, elif, else -statements`
Met een eenvoudige `if`-verklaring kun je controleren of een voorwaarde waar is en vervolgens een actie uitvoeren.
De `else`-verklaring wordt uitgevoerd als de voorwaarde in de `if` niet waar is.
Met `elif` kun je meerdere voorwaarden controleren in plaats van alleen één.

```python
if x > 10:
    print("x is groter dan 10")
elif x == 10:
    print("x is precies 10")
else:
    print("x is kleiner dan 10")
```

# 9 Logische operatoren
## 9.1 `and`, `or`, en `not`
Deze **logische operatoren** worden vaak gebruikt in **voorwaardelijke** statements en **logische vergelijkingen** om complexere beslissingen te maken in programma's.

|**Operator**|**Beschrijving**|**Voorbeeld**|**Resultaat**|
|---|---|---|---|
|`and`|Retourneert `True` als beide voorwaarden waar zijn.|`x > 3 and y < 15`|`True` als beide waar zijn.|
|`or`|Retourneert `True` als één van de voorwaarden waar is.|`x > 3 or y < 15`|`True` als één waar is.|
|`not`|Keert de waarde van de voorwaarde om.|`not x > 3`|`True` als x niet groter is dan 3.|

```python
x = 5
y = 10
z = 15

if x > 3 and (y < 15 or z > 10):
    print("De combinatie van voorwaarden is waar.")
```

# 10 Loops
## 10.1 `For`-loop
De `for`-loop wordt vaak gebruikt wanneer je van tevoren weet hoe vaak je een actie wilt herhalen.

```python
for i in range(5):  # Van 0 t/m 4
    print(i)
```

## 10.2 `While`-loop
De `while`-loop wordt gebruikt wanneer je wilt blijven herhalen zolang een bepaalde voorwaarde waar is. Je weet vaak niet van tevoren hoeveel iteraties je zult doen. 

```python
while True:
    user_input = input("Type 'stop' om te stoppen: ")
    if user_input == 'stop':
        break  # Verlaat de loop
```


# 11 Functies maken
**Functies** worden gebruikt om code te groeperen die een specifieke taak uitvoert, wat hergebruik en overzichtelijkheid bevordert. Ze helpen duplicatie van code te vermijden en maken programma's gemakkelijker te onderhouden. Functies kunnen parameters aannemen, gegevens verwerken en resultaten teruggeven. Hierdoor kun je complexe programma's modulair en efficiënter opbouwen.

```python
def begroet(naam):
    print(f"Hallo, {naam}!")

begroet("Emma")
```

# 12 Lijsten en Operaties
**Lijsten** worden gebruikt om meerdere waarden in één variabele op te slaan, waardoor je gegevens georganiseerd kunt beheren, doorzoeken, toevoegen en manipuleren. Ze zijn flexibel, omdat ze waarden van verschillende typen kunnen bevatten en dynamisch van grootte kunnen veranderen.

```python
my_list = [1, 2, 3, 4]
my_list.append(5)      # Voeg toe
my_list.pop(2)         # Verwijder index 2
my_list[1] = 99        # Wijzig item
```

# 13 Strings manipuleren
Stringmanipulatie maakt het gemakkelijker om met tekstuele gegevens te werken, zoals gebruikersinvoer, bestandsinhoud of output.

| **Manipulatie**                  | **Voorbeeld**               | **Beschrijving**                                              |
| -------------------------------- | --------------------------- | ------------------------------------------------------------- |
| **Concatenatie**                 | `"Hallo" + " wereld!"`      | Twee strings samenvoegen.                                     |
| **Herhalen**                     | `"Ha!" * 3`                 | Een string meerdere keren herhalen.                           |
| **Indexeren**                    | `s = "Python"` `s[0]`       | Toegang tot een specifiek teken in een string met een index.  |
| **Slicen**                       | `s[0:3]`                    | Een deel van een string ophalen met een bereik van indexen.   |
| **Omzetten naar kleine letters** | `"Hallo".lower()`           | Zet alle letters in een string om naar kleine letters.        |
| **Omzetten naar hoofdletters**   | `"Hallo".upper()`           | Zet alle letters in een string om naar hoofdletters.          |
| **Verwijderen van witruimte**    | `" Hallo ".strip()`         | Verwijdert overtollige witruimte aan het begin en einde.      |
| **Vervangen**                    | `"Hallo".replace("o", "a")` | Vervangt een substring door een andere string.                |
| **Splitsen**                     | `"Hallo wereld".split()`    | Splits een string op basis van een delimiter (zoals spaties). |
| **Formattering**                 | `f"Hallo, {naam}!"`         | Dynamisch waarden invoegen in een string met f-strings.       |

```python
s = "Hallo, wereld!"
print(s.lower())   # Kleine letters
print(s.upper())   # Hoofdletters
print(len(s))      # Lengte van string
```

# 14 Dictionaries
Het doel van **dictionaries** is om gegevens op te slaan in paren van **sleutels** en **waarden**, waardoor je snel en efficiënt toegang hebt tot specifieke gegevens op basis van hun unieke sleutel. Dit maakt dictionaries ideaal voor het organiseren van gegevens die een duidelijke koppeling of mapping hebben, zoals namen en adressen of product-ID's en prijzen.

```python
my_dict = {"naam": "Anna", "leeftijd": 25}
print(my_dict["naam"])     # Toegang tot waarde
my_dict["leeftijd"] = 26   # Update waarde
```

