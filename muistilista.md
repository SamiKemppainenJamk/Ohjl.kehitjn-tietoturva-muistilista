## Ohjelmistokehittäjän tietoturva muistilista

# Suunnittelu
- Security by design (uhkamallinnus) STRIDE 
+ (S)poofing 
+ (T)ampering
+ (R)epudiation
+ (I)nformation Disclosure
+ (D)enial of service
+ (E)levation of Privilige
- Least privilege kaikille (lisätään oikeuksia tarpeen vaatiessa)

# Autentikointi ja oikeudet
- Käytä olemassa olevia testattuja ja laajasti käytössä olevia kirjautumis- ja token-järjestelmiä
- Käytä salasanojen hashausta (Esim. Argon 2)
- MFA oletuksena aina kun mahdollista

# Syötteet ja hyökkäykset
- Kaikki ulkoinen data lähtökohtaoletuksena epäluotettavaa
    → Käyttäjien syöttämä data
    → URL-parametrit, query-stringit
    → HTTP-headerit (User-Agent, Referer)
    → Cookie-arvot, session-id:t
- Tiedostot ja uploadit
    → Käyttäjän lataamat tiedostot
    → Sähköpostiliitteet

# Secrets
- TSL kaikkialla (sisäinen liikenne mukaanlukien)
- Secrettien kanssa vain Secret Manager / Vault
- Avainten säännöllinen rotaatio

# Data ja yksityisyys
- Kerää vain pakollinen data
- Salaus levossa ja varmuuskopioinnissa
- Henkilötietojen pseudonymisointi 
  (muutetaan tiedot siten, ettei yksittäistä henkilöä tunnista ilman lisätietoja)
- GDPR: poisto, minimointi, audit trail
- Ei henkilötietoja lokiin

# Tiimi ja prosessit
- Code review aina 
- Dokumentoidut käytännöt
- Säännölliset tietoturvakoulutukset
- Vastuullinen haavoittuvuuksien raportointi
    
