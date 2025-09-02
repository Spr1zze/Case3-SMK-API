# API Case 3 – SMK API

Dette repo dokumenterer mit arbejde med **SMK API** (Statens Museum for Kunst).  
Opgaven er delt op i flere trin: forståelse af API’et, planlægning af løsning (UX/flow), dokumentation af valg samt refleksion.

---

## Del 1: Forstå API’et

**Base-URL:**  
https://api.smk.dk/api/v1

**Søgeparametre:**  
- `keys`
- `fields`
- `facets`
- `filters`
- `sort`
- `offset`
- `rows`

**Testeksempler:**  
- Test 1: `keys=*`  
- Test 2: `facets=has_image`  

**JSON-struktur (udvalgte felter):**
- **Titel:** `items[] -> documentation[] -> title`
- **Kunstner:** `items[] -> documentation[] -> author`
- **Årstal:** `items[] -> documentation[] -> year_of_publication`
- **Thumbnail:** `items[] -> production_dates_notes[] -> image_thumbnail`

---

## Del 2: Planlægning (UX/Flow)

Min planlagte løsning blev opdelt i flere trin, som alle er markeret som *done*.  
Se screenshots nederst i README for et visuelt overblik.

---

## Del 3: Dokumentation af valg

Jeg anvender følgende query-parametre:

- **Keys:** `*` (alle)  
- **Facets:** `has_image`  
- **Sort:** `created` (sortering efter hvornår data er tilføjet)  
- **Offset:** `100` (start fra række 100)  
- **Rows:** `20` (vis 20 rækker ad gangen)  

**Samlet URL:**
https://api.smk.dk/api/v1/art/search?keys=%2A&fields=&facets=has_image&sort=created&offset=100&rows=20

**Felter anvendt i frontend (cards):**
1. Navn på kunstværket  
2. Kunstner  
3. Årstal  

Disse valg blev truffet, fordi det er de mest naturlige informationer, man som bruger forventer at se først.

> **Note om licens:**  
> Hvis jeg havde brugt faktiske data eller billeder fra SMK, ville jeg have krediteret med teksten:  
> *“Al data og billeder fra SMK Open – Statens Museum for Kunst”*.  
> Dette er et licenskrav fra SMK.

---

## Del 4: Refleksion

Arbejdet med SMK API’et var rent teoretisk og baseret på læsning af dokumentationen.  

- I starten virkede det uoverskueligt med lange URL’er fyldt med parametre.  
- Efter at have eksperimenteret i Swagger UI begyndte tingene at give mening – især hvad base-URL og endpoints betyder.  
- Jeg føler mig stadig presset ved tanken om at implementere API’er i rigtige projekter, da det virker komplekst og forskelligt fra API til API.  

**Konklusion:**  
Det er udfordrende, men jeg ser frem til at skulle bruge API’er i praksis og dermed blive tvunget til at lære det ordentligt.

---

## Screenshots
(se filer i repoet)
