# Prigovor RIK-u: biračko mesto u UAE

**Stranica: https://srbsuae-spec.github.io/prigovor-rik-uae/**

Republička izborna komisija (RIK) nije odredila nijedno biračko mesto u Ujedinjenim Arapskim Emiratima za izbore za narodne poslanike 25. oktobra 2026. Za glasanje u UAE prijavilo se više od 500 birača. Ova stranica svakom biraču pravi formalni prigovor RIK-u sa njegovim podacima i otvara ga u njegovom mejlu. Prigovor šalje sam birač, sa svoje adrese.

*English summary: a one-page form for Serbian voters in the UAE. It fills in a formal objection to Serbia's Republic Electoral Commission about the missing polling station, then opens it in the voter's own mail app. No server, nothing is stored.*

## Pitanje Ambasadi u Abu Dabiju

**https://srbsuae-spec.github.io/prigovor-rik-uae/ambasada.html**: mejl Ambasadi Republike Srbije u Abu Dabiju (izbori.abudhabi@mfa.rs) za birače koji su dobili potvrdu o upisu u birački spisak, a biračko mesto u UAE ipak nije otvoreno. Pita koliko je prijava primljeno, da li su Ambasada i MSP predložili biračko mesto, zašto UAE nije na listi i da li može naknadno da se odredi. Stranica ima 30 verzija teksta (kraće, srednje, duže) i 15 predmeta, da mejlovi ne bi bili isti. Mejl ne sadrži JMBG ni dokumenta.

## Vesti i status

**https://srbsuae-spec.github.io/prigovor-rik-uae/vesti.html**: kratak pregled šta je urađeno (RIK, mediji, međunarodne institucije, pravni koraci) sa linkovima na objave u medijima.

## Kako se koristi

1. **Pripremi priloge** (dodaju se ručno u mejlu):
   - kopija važećeg pasoša ili lične karte;
   - snimak ekrana e-maila kojim si poslao/la zahtev za glasanje u inostranstvu;
   - snimak ekrana e-mail obaveštenja Ambasade o uspešnoj prijavi, ako si ga dobio/la.
2. Otvori stranicu i popuni: ime i prezime, JMBG, adresu prebivališta u Srbiji, e-mail, gde si se prijavio/la (Abu Dabi ili Dubai) i gde živiš.
3. Pregledaj tekst prigovora. Možeš da ga izmeniš.
4. Klikni dugme za svoj mejl: Gmail, Outlook, Yahoo ili mejl aplikaciju. Otvara se nov mejl sa popunjenim primaocima, predmetom i tekstom.
5. **Dodaj priloge** i pošalji.

Ako nijedno dugme ne radi, na dnu stranice postoje dugmad za kopiranje svakog polja posebno: svi primaoci, predmet i tekst.

## Kome ide mejl

**Prigovor sa ličnim podacima** (ime, JMBG, adresa, dokumenta) ide **samo RIK-u**, preko zvaničnih adresa:

| | Adresa |
|---|---|
| **Prima** | rik@parlament.rs |
| **CC** | izbori@parlament.rs |

Lične podatke i dokumenta ne šalji organizacijama, organizatorima akcije, u grupe ni preko društvenih mreža. CeSID je to i javno zatražio.

**Posle slanja (neobavezno), dva mejla bez ličnih podataka:**

| Kome | Adrese | Sadržaj |
|---|---|---|
| Organizatorima akcije, za brojanje | studentiublokadidijaspora@gmail.com | da je prigovor poslat, grad prijave, mesto boravka i datum |
| Organizacijama za praćenje izbora | cesid@cesid.rs, bojan.klacar@cesid.rs, prijavi@crta.rs, sofija.mandic@cepris.org | opis problema: šta se desilo, gde i kada |

## Privatnost

- Stranica je jedan statičan HTML fajl. Nema servera, baze, kolačića ni analitike.
- Ono što upišeš ostaje u tvom pregledaču i nestaje kad zatvoriš stranicu.
- Podaci napuštaju tvoj uređaj samo u mejlu koji ti pošalješ RIK-u. Mejlovi organizatorima i organizacijama ne sadrže ime, JMBG, adresu ni dokumenta.

## Napomene o tekstu

- Tekst i predmet su namerno bez slova č, ć, š, ž i đ (pišu se c, s, z, dj). Tako ih nijedna mejl aplikacija ne kvari. Isto važi i za ono što korisnik upiše.
- Tekst je napravljen po prigovoru koji je birač iz Dubaija poslao RIK-u 5. 10. 2026.
- Rod (podneo/podnela, dobio/dobila) se predlaže prema JMBG-u i može da se promeni.

## Gde radi

Testirano 5. 10. 2026:

| Uređaj | Gmail | Outlook | Yahoo | Mejl aplikacija |
|---|---|---|---|---|
| Android (Pixel 8 Pro, Chrome) | ✅ | ✅ | ✅ | ✅ (ponudi izbor aplikacije) |
| iPhone (iOS 26) | ✅ | ✅ | ✅ | ✅ (Mail) |

Na telefonu dugmad otvaraju aplikacije direktno: na Androidu preko `intent:` linkova, na iPhone-u preko `googlegmail://`, `ms-outlook://` i `ymail://`. Na računaru otvaraju veb verzije Gmail-a, Outlook-a i Yahoo-a.

Ako je stranica otvorena unutar WhatsApp-a, Vibera ili Instagrama, otvori je u Chrome-u ili Safariju. Ugrađeni pregledači tih aplikacija često ne puštaju otvaranje mejl aplikacije.

Stranica ne radi kao Claude Artifact na telefonu, jer claude.ai prikazuje stranicu u zaključanom okviru koji zabranjuje otvaranje drugih aplikacija. Zato je ovde, na GitHub Pages.

## Izmene

Cela stranica je u [`index.html`](index.html): HTML, CSS i JavaScript, bez zavisnosti. Za izmenu teksta prigovora menja se funkcija `napravi()`, za primaoce prigovora lista `CC`, a za mejlove bez ličnih podataka funkcija `obavestenja()` i lista `OBS`. Posle push-a na `main`, GitHub Pages osveži stranicu za oko minut.

Za drugu zemlju možeš da napraviš fork i promeniš tekst, mesta i adrese ambasade.
