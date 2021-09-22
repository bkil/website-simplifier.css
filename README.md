# Website Simplifier

A **Website Simplifier** (magyarul weboldal-egyszerűsítő) projekt célja egyéni CSS-fájlok összegyűjtése a különböző weboldalakhoz. Ezek a CSS-fájlok automatikusan eltüntetik a weboldalakról a felesleges elemeket, és csak a valódi tartalmat jeleníttetik meg a böngészővel.


## A projekt célja

Az alábbi példa a _The Hacker News_ weboldal egyik cikkét tartalmazza. Amint a képernyőképen látható, a weboldal tele van felesleges elemekkel. A valódi tartalmat a zölddel jelölt dobozok jelzik. Ez egy borítókép és nyolc bekezdésnyi szöveg.

<img src="https://codeberg.org/urbalazs/website-simplifier/raw/branch/main/doc/images/1-hacker-news-website.jpg"/>
<img src="https://codeberg.org/urbalazs/website-simplifier/raw/branch/main/doc/images/2-useful-content.jpg"/>

Egyéni CSS-fájl segítségével lehetőség van a felesleges elemeket eltüntetni. A bal oldalon az eredeti weboldal, a jobb oldalon pedig az egyszerűsített változata látható. Tisztább, szárazabb, biztonságosabb érzés, nemde?

<img src="https://codeberg.org/urbalazs/website-simplifier/raw/branch/main/doc/images/3-simplified-website.jpg"/>


## Hogyan működik

**A projekt csak Mozilla Firefox böngészőhöz (és variánsaihoz) ad támogatást.**

Az egyéni CSS-fájlok támogatásának bekapcsolásához:

1. Írd be a böngésző címsorába, hogy `about:config`.
2. Kattints a _Kockázat elfogadása és továbblépés_ gombra.
3. Az oldal tetején lévő keresőmezővel keress rá a `toolkit.legacyUserProfileCustomizations.stylesheets` beállításra.
4. Kapcsold át a beállítást `true` (igaz) értékre. Az alapértelmezett `false` (hamis) értékkel a Firefox figyelmen kívül hagyja az egyéni CSS-fájlokat.

A tároló `userContent` mappája tartalmazza az egyéni CSS-fájlokat. Ahhoz, hogy használni tudd valamelyiket közülük, a következő lépések szükségesek:

1. Keresd meg a Firefox profilmappáját. Ezt vagy a Firefox súgójában (☰ → Súgó → Több hibakeresési információ) vagy a címsorba az `about:support` beírásával lehet megkeresni.
2. A _Profilkönyvtár_ sorban kattints a _Könyvtár megnyitása_ gombra.
3. Hozz létre ebben a könyvtárban egy `chrome` nevű mappát. Ne tévesszen meg az elnevezés, ez nem egy másik böngészőre utal, hanem a Firefox ilyen néven hivatkozik a böngésző azon felületére, amely a megjelenített weboldalakat körülveszi.
4. Hozz létre egy `userContent.css` fájlt az újonnan létrehozott `chrome` mappába.
5. Válogasd össze azokat a CSS-fájlokat ebből a projektből, amelyekre szükséged van.
6. Másold be egymás után a kiválasztott fájlok tartalmát a `userContent.css` fájlba, és mentsd el a fájlt.
7. Indítsd újra a Firefox böngészőt.
8. Mostantól a kiválasztott weboldalak egyszerűsítve fogank megjelenni.


## Közreműködés

Ha szeretnél egy weboldalt egyszerűsítve nézni, de nem találod a listában, akkor két lehetőséged van:

1. Nyiss egy [issue](https://codeberg.org/urbalazs/website-simplifier/issues)-t, és add meg a weboldal címét.
2. Csináld meg a CSS-fájlt, és hozz létre egy [pull request](https://codeberg.org/urbalazs/website-simplifier/pulls)-et. Sablonként használd a tárolóban lévő `template.css` fájlt.
