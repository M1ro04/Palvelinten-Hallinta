__x)__ 

__Niemi 2025: H4 Tehtävät__

-Virtuaalipalvelin vuokrataan palveluntarjoajalta, minkä jälkeen sille asennetaan käyttöjärjestelmä ja tehdään tarvittavat alkutoimet.

-Oma huomio: Virtuaalipalvelimen käyttöönotto vaatii useita vaiheita, mutta komentorivillä tehtävät ylläpitotoimet ovat melko suoraviivaisia, kun komennot ovat tuttuja.

-Oma kysymys: Miten palvelimen lokeista voidaan erottaa tavalliset yhteysyritykset mahdollisista tietoturvauhista?

__Partanen 2025: Harjoitus 5 – a) Nimi__

-Verkkotunnuksen avulla verkkopalveluun pääsee helposti muistettavalla nimellä IP-osoitteen sijasta.

-Verkkotunnuksen ja palvelimen IP-osoitteen yhdistäminen helpottaa verkkopalvelun käyttöä ja mahdollistaa oman verkkosivun julkaisemisen omalla nimellä.

-Oma huomio: Verkkotunnus tekee verkkosivusta helpommin löydettävän, mutta sen toiminta riippuu oikein määritetyistä DNS-tietueista.

-Oma kysymys: Kuinka kauan DNS-tietueen muuttamisen jälkeen voi kestää, ennen kuin uusi IP-osoite toimii kaikkialla?



__a)__

-aloitin tehtävän ensimmäisellä tunnilla tekemällä käyttäjän upcloudiin ja vuokraamalla sieltä palvelimen.

-palvelimen kautta asensin koneelleni Debian 13. ja käynnistin sen MACOS terminaalissa. 
<img width="854" height="132" alt="Screenshot 2026-10-26 at 17 55 00" src="https://github.com/user-attachments/assets/9786d5c4-1351-4c7c-9f3e-a95c391210a7" />



__b)__

vuokrasin uplcoudin kautta virtuaalisen yksityispalvelimen (VPS) <img width="1468" height="823" alt="Screenshot 2026-10-26 at 18 07 47" src="https://github.com/user-attachments/assets/2852d0e6-9488-49d9-ab40-0ee15cb5a95f" />



__c)__ 

-Tehtävänä oli tehdä virtuaalipalvelimelle alkutoimet.

-aloitin tekemällä käyttäjän omalla nimelläni tein sen komennolla adduser miro.

-tämän jälkeen lisäsin sen sudo-ryhmään <img width="1704" height="282" alt="image" src="https://github.com/user-attachments/assets/50f9e955-e9f8-4490-ad64-ae1b1d26fa50" /> 

-Seuraavaksi testasin sudo oikeudet ja testasin myös komentoa sudo whoami <img width="1544" height="282" alt="image" src="https://github.com/user-attachments/assets/526ed953-1543-436b-8f28-0d0c53e6e423" /> 

-seuraavaksi tehtävässä piti asentaa palomuuri joten, asensin palomuurin komennolla: sudo apt install ufw -y <img width="1544" height="438" alt="image" src="https://github.com/user-attachments/assets/cfc27bed-c73d-40a0-9cc9-9fb0d3dcd178" /> 

-tämän jälkeen sallin SSH-yhteyden ennen palomuurin käyttöönottoa komennolla sudo ufw allow OpenSSH <img width="1544" height="144" alt="image" src="https://github.com/user-attachments/assets/326ce2f8-336d-4e72-b9ee-d4e04bf77c99" /> 

-seuraavaksi otin palomuurin käyttöön komennolla sudo ufw enable. Tarkistin tulosteen komennolla sudo ufw status verbose <img width="1544" height="454" alt="image" src="https://github.com/user-attachments/assets/c9d24985-1b75-4e5e-b283-2cdfd8e454b9" />

-tämän jälkeen päivitin kaikki ohjelmat ja boottasin koneen. 



__d)__

tehtävässä piti asentaa Webbipalvelin ja valitsin apachen, tämän asensin komennolla: sudo apt install apache2. <img width="2748" height="814" alt="image" src="https://github.com/user-attachments/assets/06cae0f1-58d3-466d-8dae-5444ee8e63a5" /> 

-tämän jälkeen asennus kysyy vahvistusta, joten painoin yes.

-Seuraavaksi tarkistin apachen tilan ja käynnistin sen komennoilla: sudo systemctl enable --now apache2 ja systemctl status apache2. <img width="2748" height="620" alt="image" src="https://github.com/user-attachments/assets/a762d1c1-91f7-4ccb-a4bc-c33230293fec" /> 

-tuloste näyttää active: active (running), joten tiedän, että se toimii kunnolla. 

-tämän jälkeen testasin verkkopalvelimen toiminnan laittamalla selaimeen http://omanpalvelimenip ja sain apache2 debian default page, joten tiedän että kaikki toimii. <img width="2904" height="1666" alt="image" src="https://github.com/user-attachments/assets/ac8ffe97-1234-47c6-8367-0415be67ad8c" />

-Tämän jälkeen loin oman HTML sivun.

-avasin apachen oletussivun muokattavaksi komennolla: sudo nano /var/www/html/index.html. poistin vanhan sisällön ja laitoin sinne uuden. 

-tämän jälkeen avasin taas sivun palvelimella ja tulokseksi tuli: <img width="2904" height="984" alt="image" src="https://github.com/user-attachments/assets/876f0d74-da83-4258-beef-d78b06a92bd2" />











