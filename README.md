
## Upplýsingar um verkefnið

### Keyrsla verkefnis
Til að keyra verkefnið er hægt að sækja repoið og einfaldlega færa cmd eða terminal gluggann í möppuna sem þetta er og keyra:
__npm run browser-sync__
þá fer í gang localhost en til að geta gert þessa skipu þarf að vera sett upp node.js á vélina, einnig er hægt að keyra heimasíðuna gegnum þetta heimasvæði: https://notendur.hi.is/ojv1/vefforritun/h1/


### Uppsetning verkefnis
Heimasíðan er sett upp þannig að í rótinni þar sem index skráin er þar er einnig __styles.css__ ásamt __grid.css__ sem index síðar kallar beint í. fyrir utasíðar möppur með gefnu efni og útliti frá kennara eru möppurnar
* __fonts__
* __img__
* __pages__
* __scss__

#### fonts
okkur þótti skynsamlegra að eiga til fontinn sem eru ekki gjarnan innbyggð bara á servernum eða í rót verkefnisins þannig að við bættum við eins og t.d. Oswald og OpenSans og köllum á með __@font-face__ í __styles.scss__

#### img
í __img__ möppunni eru allar myndir sem við notuðum til að birta bæði starfsmennina og vörur ásamt myndum á forsíðu skv. fyrirmynd kennara, við vorum ekki að fara í það að vera með undirmöppur og flokka það nánar þar sem þetta var ekki ógrynni af myndum en í svona stærra og flóknara væri maður eflaust með betri sortunarferli á þessu

#### pages
í __pages__ möppuni felum við aukaundirsíðurnar eins og __cart.html__, __products.html__, __staff.html__ og kalla þær síðan í aðal __styles.css__ skjalið frá rót verkefnisins ásamt myndum og því sem er notað af hverri síðu fyrir sig.

#### scss
Við fórum kannski svolítið overboard í hugsununum þarna en við ætluðum að henda í __scss__ nánast fyrir hvert tilkvik að síðu, bæði til að forðast að við værum við puttana í skjali hjá hvor öðrum og einnig því það var bara svolítið kúl. en í möppunni __scss__ þá eru 10 __scss__ skjöl sem að eru síðan importuð með npm sass og keyrð til að vera hluti af einu stóru __styles.css__ skjali sem að html skrárnar lesa og túlka. __scss__ skrár sem við vorum að vinna með sem voru kannski "in hindsight" óþarfi eða gátu verið hluti af öðrum voru skrárnar eins og 

* __animation.scss__
* __fonts.scss__
* __variables.scss__

animationið hefði t.d. þar sem að við vorum ekki að vinna með einhver massa keyframes og þannig bara mátt eiga heima í viðeigandi scss skjali fyrir sína síðu, sama gildir um __fonts.scss__ það í raun hefði bara mátt eiga heima annahvort í __styles.scss__ eða __config.scss__ en meina hey...

en skipulagið var í raun ósköp einfalt það er spes scss skjal fyrir footer og header og þar sem hausinn og fóturinn á öllum síðum var meira og minna alveg eins fyrir utan breytingar á active_page þá er það notað í raun á öllum síðum en annars var skipulagið svona:
* __index.html__ <-> __index.scss__ 
* __staff.html__ <-> __Staff.scss__ 
* __cart.html__ <-> __cart.scss__ 
* __products.html__ <-> __products.scss__ 
* __*.html__ <-> __footer.html__ && __header.html__

en eftir að þessu er compileað með __sass__ þá verður þetta allt undir einu __styles.css__
* __*.html__ <-> __styles.css__

#### Upplýsingar um þá sem unnu verkefni
Hópurinn samanstóð af þremur einstaklingum
* __sot13@hi.is__ - Styrmir Óli Þorsteinsson
* __jva5@hi.is__ - 	Jón Valgeir Aðalsteinsson
* __ojv1@hi.is__ - Ólafur Jón Valgeirsson

Skiptum við meira og minna bara heimasíðunum með okkur og unnum saman að fínpússun og yfirferð og fórum yfir og gagngrýndum hjá hvor öðrum til að komast sem næst lausninni


## Lýsingar frá Kennara
*** 
# Hópverkefni 1

Verkefnið felst í því að smíða vef eftir forskrift.

Gefnar eru [fyrirmyndir](utlit/) í `500px`, `800px` og `1500px` með grind ásamt `1500px` án grindar og yfirliti yfir virkni vefs í `utlit/video.mp4`.

## Síður

Gögn fyrir síður eru í viðeigandi textaskrám (t.d. forsida.txt) undir `gogn/`. Myndir fyrir síður eru gefnar undir `img/`. Afrita þarf öll gögn á milli síðna, ekki er krafa um að setja upp sameiginlegan haus/fót á síðum.

Efni síðu skal ekki vera breiðara en `1200px`. Litir í haus og fæti skulu fylla út í allt lárétt pláss.

Síður hafa allar sama haus og sama fót. Vöruflokkar í fæti skulu allir vísa

Grunn leturstærð er 16px og fylgja allar aðrar leturgerðir eftirfarandi skala: `12 14 16 18 21 24 36 48 60`.

Litapalletta fyrir vef er `#000000`, `#ffffff`, `#afb281`, `#cee8ff`, `#fcffd2` og `#cc9694`.

Letur fyrir meginmál er Open Sans eða helvetica, arial eða sans-serif letur.
Letur fyrir fyrirsagnir er Oswald, Verdana eða serif letur.

Flest allt er sett upp í 12 dálka grind með `20px` gutter.

Öll bil eru hálft, heilt, tvöfalt eða þrefalt margfeldi af gutter. Hægt er að nota reglustiku tól (t.d. http://www.arulerforwindows.com/ eða http://www.pascal.com/software/freeruler/) til að finna nákvæmar stærðir en mestu skiptir að lausn svipi til en sé ekki nákvæmlega eins og fyrirmynd.

Allar hreyfingar gerast á `300ms` með `ease-in-out` hröðunarfalli.

Ekki þarf að útfæra neina virkni fyrir takka eða form.

## Hópavinna

Verkefnið skal unnið í hóp með þremur einstaklingum. Hafið samband við kennara ef ekki er mögulegt að vinna í hóp.

Notast skal við Git og GitHub. Engar zip skrár með kóða ættu að ganga á milli í hópavinnu, heldur á að „committa“ allan kóða og vinna gegnum Git.

## Lýsing á verkefni

`README.md` skrá skal vera í rót verkefnis og innihalda:

* Upplýsingar um hvernig keyra skuli verkefnið
* Lýsingu á uppsetningu verkefnis, hvernig því er skipt í möppur, hvernig CSS er skipulagt og fleira sem á við
* Upplýsingar um alla sem unnu verkefni
* Leyfilegt er að halda eftir þessari verkefnalýsingu en hún skal þá koma _á eftir_ ykkar lýsingu

## Tæki og tól

Setja skal upp Sass og stylelint fyrir verkefnið. Gefin er `styles.scss` skrá með grunn upplýsingum.

Gefin er `.stylelintrc` skrá sem segir til um hvernig lint fyrir `scss` skrár skuli háttað.

Í `.gitignore` er `styles.css` hunsað sem þýðir að það verður _ekki_ checkað inn. Það er gert vegna þess að það er búið til af sass út frá `styles.scss`

## Gefnar skrár

Eftirfarandi er sett upp í verkefni:

* `.stylelintrc` með upplýsingum um hvernig stylelint eigi að haga sér. Setja þarf upp `stylelint-config-primer` pakkann
* `.gitignore` sem hunsar algengar skrár, [sjá nánar](https://help.github.com/ignore-files/)
* `.gitattributes` sem kemur í veg fyrir ósamræmi sem geta komið upp þegar unnið er á milli stýrikerfa
* `.editorconfig` sem samræmir notkun á tabs og spaces, bilum [og fleira](https://editorconfig.org/)
* `index.html` með vísun í `styles.css` og `grid.css` ásamt tómum skrám fyrir `products.html`, `about.html` og `cart.html` undir `pages/`, halda skal þessu skipulagi
* `grid.css` til að sjá grid sem fyrirmynd er unnin eftir

Setja þarf upp `package.json` og sækja viðeigandi pakka til að tæki og tól sem verkefnið á að nýta virki.

## Mat

* 10% - `README` eftir forskrift, tæki og tól uppsett
* 20% – Snyrtilegt, gilt (skv. stylelint) CSS/Sass, gilt og aðgengilegt HTML
* 30% – Almennt útlit
* 10% – Forsíða
* 10% – Vörulista síða
* 10% – Um síða
* 10% – Kaupa síða

## Sett fyrir

Verkefni sett fyrir í fyrirlestri mánudaginn 8. október 2018.

## Skil

Einn aðili úr hóp skal skila fyrir hönd allra og skila skal undir „Verkefni og hlutaprófa“ á Uglu í seinasta lagi fyrir lok dags föstudaginn 26. október 2018.

Skil skulu innihalda:

* Nöfn allra í hóp ásamt notendanafni
* Slóð á GitHub repo fyrir verkefni, og dæmatímakennurum skal hafa verið boðið í repo ([sjá leiðbeiningar](https://help.github.com/articles/inviting-collaborators-to-a-personal-repository/)). Notendanöfn þeirra eru `arnar44`, `gorri4`, `mimiqkz`, `hinriksnaer`, `gunkol`, `freyrdanielsson` og `osk`
* Slóð á verkefnið keyrandi á vefnum

## Einkunn

Sett verða fyrir tíu minni verkefni þar sem átta bestu gilda 3,5% hvert, samtals 28% af lokaeinkunn.

Sett verða fyrir tvö stærri verkefni þar sem hvort um sig gildir 11%, samtals 22% af lokaeinkunn.

## Myndir

Myndir frá:

* [Innkaupakörfu íkon eftir Stephen Hutchings á www.flaticon.com](https://www.flaticon.com/authors/stephen-hutchings)
* Unsplash
  - https://unsplash.com/photos/MohB4LCIPyM
  - https://unsplash.com/photos/tpLz5aKdQmM
  - https://unsplash.com/photos/_T4w3JDm6ug
  - https://unsplash.com/photos/cOJgO4Zzs-w
  - https://unsplash.com/photos/PDX_a_82obo
  - https://unsplash.com/photos/ArGvQkA7iOw
  - https://unsplash.com/photos/5ExRBlHu1DA
  - https://unsplash.com/photos/b9dS7hpi67w
  - https://unsplash.com/photos/asBwpysXVB4
  - https://unsplash.com/photos/-s6XYBp1WTc
  - https://unsplash.com/photos/wKOKidNT14w

---

> Útgáfa 0.1
