# Nymind’s IPTV — TizenBrew TEST 0.6

Testovací samostatný modul. **Není to zásah do původního funkčního tizenbrew-iptv ani do Nymind’s TV 1.3.5.**

## Instalace

1. Vytvoř na GitHubu nový veřejný repozitář např. `nyminds-iptv-test`.
2. Nahraj do jeho **kořenové složky** soubory `package.json`, `README.md`, `LICENSE` a složku `app` se souborem `index.html`.
3. V TizenBrew → Module Manager → **Add GitHub Module** napiš `romangazdik-web/nyminds-iptv-test` (pouze pokud jsi repozitář takto pojmenoval).
4. Otevři `Nymind’s IPTV TEST 0.6`. V M3U Playlist zadej svoji soukromou Dropbox M3U URL **přímo na TV**, nikoliv do veřejného repozitáře.
5. Vyzkoušej ČT1 a jiný dříve funkční kanál. Stiskni Zpět pro návrat ze streamu. Na hlavní obrazovce tlačítko Zpět záměrně nepohlcujeme, aby fungoval návrat do TizenBrew. Když by návrat nezabral, použij Home.

## Důležité omezení

Přehrávání konkrétních streamů na Samsung Tizen 2017 **není ověřené**. TizenBrew může stránku servírovat jinak než GitHub Pages, takže HTTP HLS má šanci fungovat, ale neodstraňuje to automaticky CORS ani omezení kodeků. Používáme HTML5 video a případně HLS.js. Samsung AVPlay není v běžných TizenBrew modulech automaticky k dispozici.

## Soukromí a zálohy

V tomto balíčku není žádný soukromý M3U odkaz. Nezveřejňuj URL s tokenem ani samotný playlist. Seznam kanálů se načítá v TV; uložit adresu lze volitelným zaškrtnutím. Funkční modul `tizenbrew-iptv` nemaž.

## Co je nové oproti HTML 0.5

- TizenBrew manifest `package.json` pro modul typu `app`.
- Úprava tlačítka Zpět: z přehrávače na kanály, z hlavní obrazovky bez nekonečného reloadu.
- Registrace mediálních tlačítek v manifestu.
- Design a automatické kategorie z testované verze 0.5.
