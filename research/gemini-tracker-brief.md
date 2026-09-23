# Brief dla Gemini: tracker dowiezienia utworów (projekt 10xDevs 4)

Wklej **cały ten plik** na początek rozmowy. Jesteś sparring-partnerem do doprecyzowania **problemu i zakresu**, nie product managerem, który zamyka specyfikację.

Po rozmowie poproś Gemini o jeden plik markdown według szablonu na dole. Ten plik wróci do Cursora jako wejście do `/10x-idea-check` (werdykt) i `/10x-shape` (discovery z człowiekiem). Nie zastępuje PRD.

---

## Kim jest autor (ja)

- Software developer (Capgemini). Projekt kursowy **nie** dotyczy pracy ani platformy DGEM (katalogi, blueprinty, VueFlow, Lumina) — to świadomie odcięte (IP / zgody).
- Producent w Abletonie, zespół + projekty solowe.
- Uczy się też pianina — ten trop **odłożony** na ten kurs, chyba że rozmowa znajdzie jeden bardzo wąski brak, którego nie pokrywają istniejące apki (nie szukamy „lepszego Simply Piano”).
- Doświadczenie z AI: ukończone AI Devs 3 oraz wcześniejsza edycja 10xDevs; studia inż. informatyka, spec. AI (ML/DL). Umie pracować z agentami; nie potrzebuje apki „żeby mieć AI w środku”.
- Dostęp do społeczności **Kończę Tracki** (Michał Gutkowski): można podpytać o ból, **nie** zbierać backlogu funkcji.

## Kontekst kursu (meta — to NIE są wymagania produktu)

Edycja **10xDevs 4.0**, lekcja m1l1: od pomysłu do PRD. Teraz jesteśmy **przed** kodem i **przed** PRD.

Łańcuch skilli (kolejność stała):

1. `/10x-idea-check` — czy warto iść na sesję planistyczną, jaki zakres. Rozmowa.
2. `/10x-init` — katalogi `context/` (jeszcze nie zrobione).
3. `/10x-shape` — discovery z autorem; zapis `context/foundation/shape-notes.md`. Agent **nie wymyśla** wizji, FR-ów ani reguł, których autor nie podał.
4. `/10x-prd` — PRD ze `shape-notes.md`. Potem stack i implementacja (moduł 2+).

Termin zgłoszenia, na który celuję: **4 listopada 2026, 23:59** (jedyne okno na wyróżnienie). Pierwsze zgłoszenie ustala oceniany zakres. Szacunek pojemności: deklarowane ~2 h dziennie (~10–14 h/tydzień realniej, praca + studia). Heurystyka kursu: jeśli pierwszy działający przepływ po godzinach > ~tydzień — obetnij MVP.

Żeby **Builder** w ogóle był osiągalny później, pomysł musi dać się rozwinąć do: kontroli dostępu stosownej do typu apki, CRUD sensownego dla domeny, **reguły biznesowej** (nie pusta lista), dokumentów kontekstowych, ≥1 testu z perspektywy użytkownika. Publiczny URL opcjonalny. AI **w produkcie nie jest wymagane**. Złożoność nie jest kryterium. Ostateczna ocena należy do prowadzących, nie do tej rozmowy.

Greenfield, stack dowolny — **nie wybierajcie stosu** w tej rozmowie (to osobny skill po PRD).

## Decyzje już podjęte (traktuj jako twarde, chyba że autor je odwoła)

- Nie ruszamy pracy / DGEM / Luminy / danych firmowych.
- Nie budujemy produktu **w** Abletonie na v1. Brak publicznego REST API biblioteki `.als`. Oficjalnie: Live Object Model w **Max for Live** (sterowanie **otwartym setem**: tracki, klipy, device’y). Python MIDI Remote Scripts tylko **wewnątrz** Live. M4L często wymaga Suite. To może być haczyk *po* MVP, nie fundament.
- Nie generator muzyki AI, nie OCR, nie banki, nie marketplace.
- Kierunek roboczy: narzędzie **obok** DAW (uniwersalne: Ableton to ścieżka do folderu, nie integracja).

## Nad czym się zastanawiam (problem, nie lista epików)

Ból, który chcę rozstrzygnąć: **dowiezienie**, nie kolejny instrument.

Typowe objawy (do ataku / obrony, nie do kopiowania 1:1 do specyfikacji):

- cmentarzysko utworów na 80%;
- wiele bounce’ów, nie wiadomo który jest „aktualny mix”;
- notatki z sesji giną (chat, głowa, projekt Live);
- zespół: która wersja idzie na próbę;
- pokusa rozrostu: referencje, mastering, feedback AI, stem’y, deadliny wytwórni — to rozsadza kursowe MVP.

Kandydat na **jedną** regułę (wybrać jedną na v1, nie obie):

- A: tylko jeden plik oznaczony jako aktualny mix na utwór;
- B: nie wolno statusu „mix”, dopóki checklista aranżu nie jest domknięta.


## Czego chcę od Ciebie (Gemini)

Rób:

- Zaostrzaj problem: kto konkretnie (ja solo / zespół?), jaki użyteczny rezultat po 5 minutach użycia.
- Porównuj A vs B vs inną **jedną** regułę z życia studia — z uzasadnieniem, którą łatwiej dowieźć do 4.11.
- Oddziel **pierwszy działający kamień** od **MVP zgłoszeniowego**.
- Zaproponuj 3 pytania do społeczności Kończę Tracki o **problem** (nie „co apka powinna mieć”).
- Flaguj rzeczy, które brzmią jak startup, nie jak narzędzie dla jednego producenta.
- Oznacz jasno: `DECYZJA AUTORA` vs `SUGESTIA GEMINI` vs `OTWARTE`.

Nie rób:

- PRD, user stories w formacie Jira, listy FR-001…, wyboru stacku, architektury, bazy, hostingu, „dodajmy LLM”.
- Spekulacji, że Ableton „na pewno ma API” poza LOM/M4L i skryptami wewnątrz Live.
- Traktowania wymogów Buildera jako feature requestów produktu (to ograniczenie kursu, nie user story).
- Zatwierdzania zakresu za autora.

Jeśli czegoś nie wiem: napisz założenie. Nie przeprowadzaj kwestionariusza 20 pytań — max 5, jeśli bez nich nie da się rekomendować.

## Szablon wyniku (jedyny plik, który wracam do Cursora)

Zapisz jako `research/gemini-tracker-summary.md` (lub wrzuć do `D:\www\10xdevs4\research\`). Nagłówki zostaw po polsku, w tej kolejności — mapują się na późniejsze `shape-notes` / PRD, ale **to nadal notatki z dyskusji**, nie zatwierdzony produkt.

```markdown
# Gemini summary — tracker dowiezienia

- Data rozmowy:
- Model:
- Autor potwierdza ten plik: [tak/nie — uzupełnię w Cursorze]

## Seed (słowami autora)
[1–3 zdania; nie przepisuj na pitch]

## Problem i rezultat
- Kto korzysta w v1:
- Jaki użyteczny rezultat:
- Co jest poza wartością (nie „miło mieć”):

## Persona (v1)
- Solo producent / zespół / oba — i dlaczego v1 jest węższe:

## Proponowana reguła biznesowa (jedna)
- Wybrana (A / B / inna):
- Uzasadnienie:
- Odrzucone warianty:

## Kamień vs MVP (4.11)
- Pierwszy działający przepływ:
- Zamierzone MVP:
- Świadome non-goals:

## Kontrola dostępu (zgrubnie, bez stacku)
- Kto się loguje w v1 i po co:

## CRUD, który ma sens w domenie
- Jakie encje (utwór, plik, checklista…):
- Czego świadomie nie modelujemy:

## Wejście z Kończę Tracki
- 3 pytania do społeczności:
- Wnioski, jeśli już są odpowiedzi:

## Ableton / M4L
- Rola w v1 (powinno być: brak albo tylko ścieżka do folderu):
- Co ewentualnie PO zgłoszeniu:

## Sugestie Gemini (niezatwierdzone)
- …

## Otwarte pytania do /10x-shape
- …

## Czego NIE robić na podstawie tej rozmowy
- …
```

Gdy szablon jest kompletny, zakończ krótkim akapitem: „To materiał do sesji planistycznej, nie specyfikacja.”
