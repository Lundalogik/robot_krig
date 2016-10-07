# Robotkrig

Lagen ska försöka replikera en fördefinierad **peanut butter jelly**-smörgås.
Det ska de göra med hjälp av en robot. Varje lag har en en egen robot.

Varje omgång ges lagen möjligheten att ge sin egen eller en någon av de andra lagens robot en *action*. Man får dock inte lägga en *action* mot någon av de andra lagens robot två omgångar på raken. Man kan också välja att inte lägga någon *action* på varken sin egen eller någon lags robot.

Varje lag har 1 minut på sig att bestäma vilken *action* de ska lägga(Den första rundan är 2 minuter). Lagen får slå tärning om vilken som får börja lägga action först. Så lagen får en minut på sig att skriva ner sin *action* som ska köras. Därefter får man vänta på sin tur för att exekvera *action*'en.

**De olika objekten är:**

 - **Brödskiva**
 - **Sylt**
 - **Jordnötssmör**

**Sylt** och **Jordnötssmör** samlas in med hjälp av **skedar**.

**Robotarna kan utföra tre stycken actions med de här objekten:**

- **Collect**
- **Apply**
- **Shift(Tallrik/Stack)**

***

**Collect**

Man anger ett *objekt* som roboten ska samla in. Då samlar roboten in *1 enhet* enhet av det *objektet*. OBS! Bara en. Varje gång man kör en **collect** lägs det *objektet* i robotens stack.
*Stacken* har plats för 3 stycken *objekt*. Varje gång man collectar knuffas *objektet* in i *stacken*. Är *stacken* full så knuffas det sista objektet ut ur *stacken*.

``` javascript
// Så här funkar stacken
stack = ['bröd', 'bröd', 'bröd'];
stack.push('sylt');

$ stack
['sylt', 'bröd', 'bröd']
```

***

**Apply**

Den applicerar det *objekt* som ligger överst i stacken på **tallriken** eller på det lager som är överst på **tallriken**. **Jordnötsmör** och **Sylt** kan inte appliceras om **tallriken** är tom. Är robotens *stack* tom så får man långsamt stryka en **sked** över det översta lagret eller på den tomma **tallriken**. Alternativt använda valfri deltagares hand istället för sked(OBS man vinner inget på detta).

**Apply**'as **Sylt** på **Sylt** eller **Jordnötssmör** på **Jordnötssmör** så blir det ett lager av det *objekt*'et

***

**Shift**

Den tar bort det första/översta *objektet* som ligger på tallriken eller det första/översta *objektet* som ligger i robotens *stack*. Laget måste specifiera vart de vill exekvera *actionen*. Finns ingen objekt tas ingen bort.

***

**Varje lag skall innehava följande**

- **Brödskivor**
- **Jordnötssmör**
- **Sylt**
- **Tallrik**
- **Skedar**

Objekten kommer bara i storleken *1 enhet*. *1 enhet* **Brödskiva**, *1 enhet* **Jordnötsmör** och *1 enhet* **Sylt** (rimliga mängder jordnötssmör och sylt på skedarna(vad som är rimligt är högst oklart)).

Den som först får sin smörgås att se ut som den fördefinierad **peanut butter jelly**-smörgåsen vinner...

...alternativt den som har en smörgås som är mest lik den fördefinierade smörgåsen efter 30 minuter vinner.
