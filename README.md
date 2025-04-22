# Architektura Procesu Reklamacyjnego w Lotnictwie

## Pomysł

Podczas udziału w rekrutacjach natrafiłem na ciekawe zadanie dotyczące zrozumienia procesów biznesowych w branży lotniczej.  
Pytanie brzmiało: **„Jak powinien wyglądać proces obsługi reklamacji pasażerskich?”**

Obsługa reklamacji to kluczowy element doświadczenia klienta w lotnictwie. Sprawna i przejrzysta procedura potrafi znacząco poprawić wizerunek firmy – nawet w sytuacjach kryzysowych.

## Moje podejście

W ramach tego mini-projektu postanowiłem zaprojektować architekturę systemu do obsługi reklamacji:

1. Przedstawiam **główne wymagania funkcjonalne** systemu  
2. Definiuję **user stories** i **kryteria akceptacji**, podkreślające wartość dla pasażera  
3. Modeluję proces w notacji **BPMN 2.0**, pokazując zarówno ścieżkę użytkownika, jak i działania wewnętrzne

## Wymagania systemu

- Możliwość zgłoszenia reklamacji przez stronę internetową oraz aplikację mobilną
- Automatyczne przypisywanie zgłoszeń do odpowiednich działów na podstawie kategorii
- Aktualizacje statusu w czasie rzeczywistym, dostępne przez aplikację, stronę i email
- Automatyczne powiadomienia o zmianach statusu zgłoszenia
- Możliwość kontaktu z pasażerem w celu uzupełnienia dokumentów
- Opcja edycji lub anulowania zgłoszenia do momentu jego rozpatrzenia
- Przekazanie decyzji oraz ewentualnych zwrotów środków przez zintegrowany system płatności
- Rejestracja historii reklamacji i analiza najczęstszych problemów

## User Stories i Kryteria Akceptacji

- **User stories**: *„Jako [typ użytkownika], chcę [potrzeba], aby [cel]”*  
- **Kryteria akceptacji**: *„Jeżeli – Kiedy – Wtedy”*

Ta struktura pozwoliła mi ułożyć wymagania w sposób przejrzysty i logiczny.

## 1. Zgłoszenie reklamacji przez stronę lub aplikację

**User Story**  
Jako pasażer  
Chcę mieć możliwość złożenia reklamacji przez stronę lot.com lub aplikację mobilną  
Aby wygodnie i szybko zgłosić problem związany z moją podróżą

**Kryteria akceptacji**
- Jeżeli jestem zalogowany na stronie lub w aplikacji  
- Kiedy wybiorę opcję „Złóż reklamację” i wypełnię formularz  
- Wtedy moja reklamacja zostanie zarejestrowana i otrzymam potwierdzenie z numerem zgłoszenia

---

## 2. Aktualizacja statusu reklamacji

**User Story**  
Jako pasażer  
Chcę mieć dostęp do aktualnego statusu mojej reklamacji  
Aby wiedzieć, na jakim etapie jest moje zgłoszenie

**Kryteria akceptacji**
- Jeżeli moje zgłoszenie zostało przyjęte  
- Kiedy status zmieni się (np. „W trakcie rozpatrywania”, „Zakończone”)  
- Wtedy zobaczę nowy status w aplikacji i otrzymam e-mail z informacją

---

## 3. Prośba o dodatkowe informacje lub dokumenty

**User Story**  
Jako pracownik działu reklamacji  
Chcę móc poprosić pasażera o dodatkowe dokumenty lub dane  
Aby dokładnie rozpatrzyć jego zgłoszenie

**Kryteria akceptacji**
- Jeżeli reklamacja została zarejestrowana  
- Kiedy wybiorę opcję „Poproś o dodatkowe informacje”  
- Wtedy pasażer otrzyma e-mail z prośbą i możliwością przesłania załączników

---

## 4. Możliwość edycji lub anulowania zgłoszenia

**User Story**  
Jako pasażer  
Chcę mieć możliwość edytowania lub anulowania mojego zgłoszenia  
Aby móc poprawić błąd lub zrezygnować z reklamacji przed jej rozpatrzeniem

**Kryteria akceptacji**
- Jeżeli reklamacja nie została jeszcze rozpatrzona  
- Kiedy wejdę w szczegóły zgłoszenia  
- Wtedy będę mógł edytować dane zgłoszenia lub je anulować

---

## 5. Zwrot kosztów przez integrację z systemem płatności

**User Story**  
Jako pasażer  
Chcę otrzymać zwrot kosztów bezpośrednio po pozytywnym rozpatrzeniu mojej reklamacji  
Aby szybko odzyskać należne środki

**Kryteria akceptacji**
- Jeżeli reklamacja została rozpatrzona pozytywnie  
- Kiedy decyzja zostanie zatwierdzona  
- Wtedy system rozpocznie proces zwrotu, a pasażer otrzyma potwierdzenie przelewu

## Model procesu (BPMN 2.0)

Model procesu został podzielony na trzy panele (pool’e):

- **Pasażer**  
- **Dział Reklamacyjny** (system + pracownik)  
- **System Płatności**

![Reclamation_Process](https://github.com/user-attachments/assets/64b04e5d-60e4-4f02-9b5f-0e4d135b2fa5)

## Integracja z Jirą 

W celu lepszego zarządzania User Story oraz ich prioretyzacją zostało wykorzystano narzędzi Jira 

- Zdefiniowany backlog z 5 user stories
- Użycie epików i estymacji (Story Points)

<img width="1177" alt="Screenshot 2025-04-22 at 15 27 35" src="https://github.com/user-attachments/assets/3735835c-d539-4719-8d51-217b3f45996c" />




