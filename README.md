Přehled k přednášce o webu:
=======================
### zdroje
> - https://github.com/dypsilon/frontend-dev-bookmarks
> - http://webplatformdaily.org/ - toto **velmi doporučuji sledovat** - něco jako cnn pro web developery :)
> - http://jankfree.org/
> - https://twitter.com/lukew Luke Woblewski twitter - autor knihy Mobile first, kterou velmi doporučuji všem, koho zajímá návrh uživatelských rozhraní: http://www.lukew.com/resources/mobile_first.asp
> - http://updates.html5rocks.com/
> - http://caniuse.com/ super užitečná databáze podpory různých features napříč různými verzemi rozšířených prohlížečů

### Několik zajímavých prezentací k tématu
####Paul Irish
> "Evangelizátor" html5/css3 - pracuje v Google a podílel se na celé řadě zajímavých projektů. Mimo jiné i na zmiňovaném Yeomanu.

- V této jeho přednášce více rozvíjí postupy, jakými dosáhnout **zvýšení rychlosti renderingu** html/css uživatelských rozhraní. Z názvu přednášky by se mohlo zdát, že se zaměřuje pouze na implementace paralaxovacího efektu. Ve skutečnosti použil paralaxu jen jako prostředek k vysvětlení toho, jak rendering v prohlížeči funguje, které operace jsou náročné a dlouhotrvající a jak to udělat, aby to bylo pěkné a přitom velmi rychlé: https://www.youtube.com/watch?v=R6TXuXV1bbY
- V této přednášce se naopak zaměřuje na různé kroky, které můžete udělat, abyste dosáhli **zrychlení načítání vašich webů a webových aplikací** - používá k tomu různé nástroje, o kterých jsem se zmiňoval. Je to opravdu zajímavé a doporučuji:
https://www.youtube.com/watch?v=R8W_6xWphtw

#### Luke Wroblewski
> Autor knihy Mobile first, kterou velmi doporučuji všem, kteří se zajímají o návrh uživatelských rozhraní http://www.lukew.com/resources/mobile_first.asp

- http://wordpress.tv/2014/11/05/luke-wroblewski-from-the-front-lines-of-multi-device-web-design/ - výborná přednáška na **téma návrhu webů pro široké spektrum zařízení**

#### Addy Osmani
> Vývojář z Google, který se podílí na vývoji Chrome browseru a na celé řadě dalších projektů spojených s webovým frontendem, mimo jiné napsal **knihu o návrhových vzorech v js**, která je dostupná zdarma na webu zde: http://addyosmani.com/resources/essentialjsdesignpatterns/book/ zajímavá je také **kniha Developing Backbone.js Applications** http://addyosmani.github.io/backbone-fundamentals/

- Přednáška k tématu rychlosti webu - obsahuje spoustu detailů, kterých jsem se v lepším případě možná jen dotknul a je to vážně i docela zábavné: https://www.youtube.com/watch?v=FEs2jgZBaQA
- http://addyosmani.com/blog/199-slides-on-front-end-tooling-workflows/ - užitečné nástroje pro webové vývojáře

#### Další zajímavé prezentace
- https://www.youtube.com/watch?v=R7iN5SFglMo&list=FLhaE_35EIY6VMKNybB_u03Q&index=105 Může být zajímavé jako příklad propojení PHP back-endu s JS front-endem. Je zde vidět, jak vše spojit tak, aby to dávalo smysl. Myslím, že to může být podobně užitečné i v případech, kdy na straně serveru není Symfony, ale řekněme Spring/Hibernate.
- http://www.samael.me.uk/2013/08/changing-workflow-from-java-to-nodejs.html Tady je článek, který by možná mohl posloužit jako odrazový můstek. Autor popisuje **vlastní zkušenost s vývojem aplikace, která byla nejprve komplet postavená na Spring/Hibernate, ale postupně ji přepsali tak, že ze serveru pouze při prvním načtení odešlou komplet HTML/JS/CSS aplikaci na klienta a dále již veškerá další komunikace probíhá pouze výměnou JSONů** a vše je tak mnohem rychlejší.
- **důležitá poznámka:** Pokud chceme, aby naše stránka byla indexovatelná vyhledavačem, není singlepage aplikace úplně optimálním řešením. I kdyby nám nemožnost, nebo velmi obtížná možnost indexace nevadila, stejně budeme bojovat s tím, že první načtení bude vždy velmi pomalé, protože je v takovém případě třeba poslat veškerý kód na klienta a teprve poté na klientu stránku sestavovat a synchronizovat stav aplikace. Lepší přístup by byl zajistit, že všechny stránky budeme umět sestavit jak na klientu, tak na serveru. To ale vyžaduje mít nějaké MVC jak na straně klienta, tak na serveru - umožnit sestavení stránky na obou stranách. Posledním trendem jsou právě izomorfní aplikace, které by to měly usnadňovat sdílením kódu na klientu i serveru tak, aby nebylo nutné pracovat s dvěma různými MVC frameworky. Tyto aplikace fungují tak, že vždy při prvním načtení se na klienta pošle stránka kompletně vygenerovaná na rychlém serveru a teprve od okamžiku, kdy je vše v prohlížeči, se již dále nic nereloaduje a další komunikace probíhá přes JSONy. Nemám s tím vůbec žádnou zkušenost, ale zmiňuji to, protože se mi to jeví velmi zajímavé.
- http://nerds.airbnb.com/isomorphic-javascript-future-web-apps/ - velmi zajímavý článek týkající se právě takových, výše zmiňovaných aplikací. Bude-li vás zajímat toto téma, mohu poslat spoustu dalších materiálů. Výklad k tomu nedám, protože se to sám snažím pochopit, ale můžu snad pomoci alespoň získat další informace.

### Nástroje / užitečné odkazy
* http://nodejs.org/ - Základní prerekvizita. Abyste vůbec mohli zkoušet věci, které jsem zmínil, je třeba nainstalovat node.js - běhový engine javascriptu V8 z chrome. Node je zdarma a pomocí balíčků npm je pro něj k dispozici obrovské množství modulů.
* http://yeoman.io - Scaffolding tool - generátor aplikací. Yeoman vám umožní bez námahy připravit strukturu adresářů, konfiguraci task runneru, nainstalování závislostí tak, abyste mohli bez bolestí a s minimální časovou investicí začít pracovat na projektu snad úplně libovolného typu. Pro yeoman existuje obrovské množství generátorů všech možných typů aplikací, se kterými si hned můžete začít hrát a zkoumat je.
* http://lesscss.org/ - css preprocesor less
* http://sass-lang.com/ css preprocesor sass
* http://bower.io/ - package manager. Např: používáte ve vaší aplikaci nějaký rozšířený jquery plugin, který má nějaké další závislosti? Definujte vše v souboru bower.json v rootu vaší aplikace.
* http://codepen.io/ - prostor pro testování a sdílení frontend kódu
* http://getbootstrap.com - responzivní front-end framework
* http://purecss.io/ - velmi lightweight front-end knihovna - nevýhodou i výhodou současně je, že toho ani moc neumí
* http://sublimetext.com - Asi nejlepší textový editor, na který jsem narazil. Jako první věc je dobré rovnou doinstalovat balíček package control, který vám umožní snadno instalovat další rozšíření - např. podporu pro syntaxi less, sass, jade,... nebo různé pomůcky jako gitgutter, které jsem tuším zmínil.
* http://atom.io - Atom editor od githubu - zatím ve velmi early fázi. V podstatě je to klon sublimetextu, ale komplet napsaný v html/less/js. Z toho plyne, že jej lze snadno hackovat a veškerou jeho funkcionalitu přizpůsobovat dle vlastních potřeb. Upravím, reloaduji a pokračuji.
* https://github.com/sindresorhus/pageres - Zajímavá pomůcka umožňující snad generovat screenshoty webů. Je to napsané nad node.js a využívá node modul phantomjs (http://phantomjs.org/)
* http://gruntjs.com/ - Asi nejpoužívanější javascript task runner. Existuje pro něj neuvěřitelné množství pluginů. Umožní vám automatizovat snad cokoliv, na co si vzpomenete. Od automatických překladů lessů, coffee scriptu, jade šablon, po concatenaci, minifikaci až po deployment na vzdálený server, nebo cokoliv jiného.
* http://gulpjs.com/ - Další task runner, který v poslední době získává na popularitě. Narozdíl od Gruntu podporuje pipelining, takže při kombinaci většího množství operací se soubory je výrazně výkonnější
* https://github.com/addyosmani/grunt-uncss - Odstraní z výsledného css všechny definice, které na stránkách, které specifikujete, nejsou využity a tím zmenší objem css. Klade ale nároky na to vylistovat všechny obrazovky se všemi použitými elementy, protože jinak vám odstraní i definice, které potřebujete.
* https://github.com/postcss/autoprefixer - velmi užitečné - umožní vám umožní očistit váš kód od prefix balastu. Můžete si sami stanovit jaké prohlížeče chcete podporovat - lze definovat různými způsoby jako např. i chci pokrýt: 99% uživatelů dle globálních statistik, nebo explicitně jmenovat,...
* https://chocolatey.org/ - Toto jsem asi vůbec nezmiňoval - package manager pro Windows. Může velmi usnadnit instalování / konfigurování, které je třeba podstoupit, než lze začít s Windows nějak rozumně pracovat.
* http://bliker.github.io/cmder/ - Toto je spíš taková zajímavost - vylepšení konzole ve windows. Pro pohodlnou práci s node.js je ale třeba nakonfigurovat.
* http://scottjehl.github.io/picturefill/ - srcset polyfill - doplní podporu pro srcset do zastaralých prohlížečů - nyní je podpora jen ve Webkitu a odvozeném Blink, tedy v Chrome
* http://modernizr.com/ - Detekce features prohlížeče. Spíše než detekovat prohlížeč a podle výsledku větvit kód, je mnohem lepší detekovat podporu konkrétní feature a větvit na základě výsledku této detekce. Takový přístup je více "future proof". Vůbec vám pak nemusí vadit změna stupně podpory v nových verzích prohlížečů. Právě naopak.
* http://requirejs.org/ - Javascript module loader
* http://expressjs.com/ - Node.js webserver, který je součástí např. MEAN stacku, který je zmíněný dále
* http://www.webpagetest.org/ - měření rychlosti webu - open source projekt. Je možné instalovat lokálně a používat například v automatizovaných testech.
* https://developers.google.com/speed/pagespeed/insights/ - Vytvoří sestavu doporučení, jak optimalizovat váš web tak, abyste zvýšili rychlost načítání a zlepšili použitelnost na mobilních zařízeních.

###Webové aplikace na Node.js
Node.js není užitečný jen jako prostředí pro spouštění různých nástrojů pro vývoj, ale lze nad ním stavět i samotnou webovou aplikaci - viz odstavec o izomorfních aplikacích výše.

Existují již knihy (např. http://www.manning.com/sholmes/), které se návrhem takových aplikací s javascriptem na serveru zabývají. Poměrně snadno si můžete zkusit jak taková aplikace vypadá právě pomocí již zmiňovaného Yeomanu. Stačí si nainstalovat odpovídající yeoman generátor a pomocí něj vytvořit kostru např. MEAN aplikace (MEAN = Mongo (NoSQL db), Express (Node.js webserver a routování), Angular, Node). MEAN je pouze jednou z mnoha možností, jak moderní web postavit. MEAN není izomorfní - angular si na node na serveru spouštět nechcete.

### Kontakty
> Kontakty na lidi v čechách, kteří se výše zmíneným zabývají a jsou v tom opravdu dobří. Jistě existují další.
