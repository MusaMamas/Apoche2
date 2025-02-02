## Name-based Virtual Host Support
IP-pohjaiset vaativat jokaiselle verkkosivustolle oman IP-osoitteen. Nimipohjaiset hyödyntävät asiakkaan HTTP-otsikkoa ja mahdollistavat useita verkkosivustoja samalla IP-osoitteella.

Apache valitsee ensin IP-pohjaisesti sopivimman isännän ja vasta sitten vertailee palvelinnimiä (ServerName, ServerAlias).
Ensimmäinen määritelty virtuaali-isäntä toimii oletuksena, jos tarkkaa osumaa ei löydy.

Jokaiselle verkkotunnukselle luodaan <VirtualHost>-lohko, jossa määritellään ServerName ja DocumentRoot. ServerAlias-direktiivi mahdollistaa useiden nimien yhdistämisen yhteen isäntään.

## Multiple Websites to Single IP Address
Apache mahdollistaa useiden verkkosivustojen isännöinnin yhdellä IP-osoitteella.
Asennus ja konfigurointi vaatii komentorivin käyttöä.

Päävaiheet:
Apache2-asennus ja oletussivun luonti.
Uuden virtuaali-isännän määrittäminen (/etc/apache2/sites-available -hakemistossa).
Sivuston testaus paikallisesti curl-komennolla.
DNS-nimen voi simuloida muokkaamalla /etc/hosts -tiedostoa.
Useiden virtuaalisten isäntien lisääminen yhdelle palvelimelle on mahdollista.
