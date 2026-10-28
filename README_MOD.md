# ⛏ Kopacz AFK Farmer - Fabric Mod (Minecraft 1.21.11 & 1.21.4)

Natywny, kliencki mod (Client-Side) do Minecrafta stworzony na bazie bota automatyzacji.

Działa w 100% w grze – bez potrzeby symulowania Windows API, bez problemu z utratą fokusu okna, z pełną synchronizacją z tickami silnika gry.

---

## 🚀 Gotowe pliki do gry (.jar)
W głównym katalogu przygotowane są skompilowane pliki `.jar`:
- 👉 **`kopacz-fabric-1.21.11.jar`** – wersja dla Minecraft **1.21.11**
- 👉 **`kopacz-fabric-1.21.4.jar`** – wersja dla Minecraft **1.21.4**

Wystarczy przenieść odpowiedni plik do folderu:
`%appdata%\.minecraft\mods` (lub folderu instancji `.mooclient` / Prism Launcher).

*Wymagania:* Minecraft **1.21.11** lub **1.21.4**, **Fabric Loader** oraz **Fabric API**.

---

## 🎮 Klawisze i Sterowanie

| Klawisz | Akcja | Opis |
|---|---|---|
| **`~`** (Tylda / Grawis) | **Włącz / Wyłącz Kopanie** | Szybkie włączenie lub zatrzymanie bota kopiącego stoniarkę |
| **`K`** | **Menu Ustawień (GUI)** | Otwiera główne menu konfiguracji z tłem kota górnika w centralnym oknie |
| **`J`** | **Farma Jabłek (Osobny klawisz)** | Niezależne uruchomienie / zatrzymanie modułu automatycznej farmy jabłek |

> 💡 **Wygodna zmiana klawiszy (Rebinding):**
> 1. **Bezpośrednio w menu moda**:
>    - W zakładce `⛏ Ruch` znajdziesz przyciski: `[ ⌨ Kopanie: ~ ]` oraz `[ ⌨ Menu GUI: K ]`.
>    - W zakładce `🍎 Jabłka` znajduje się przycisk: `[ 🍎 Klawisz Farmy Jabłek: J ]`.
>    - Wystarczy kliknąć przycisk i nacisnąć dowolny nowy klawisz na klawiaturze lub myszce (`ESC` = anuluj, `BACKSPACE` = odepnij).
> 2. **W standardowym menu Minecrafta**:
>    - Wejdź w `Opcje` ➜ `Sterowanie` ➜ `Przypisanie klawiszy` ➜ kategoria **⛏ Kopacz By Miśka**.

---

## 🎨 Menu GUI

- **Centralne okno konfiguracji** ze zdjęciem kota-górnika w tle i szklanymi, przezroczystymi przyciskami.
- **Lewy wysuwany panel (Drawer zakładek)**: przycisk `[◀]` / `[▶]` w lewym górnym rogu wysuwa panel zakładek (`⛏ Ruch`, `🔧 Naprawa`, `📦 Skrzynie`, `🔄 Reconnect`, `🗑 Drop`, `💬 Czat`, `🍎 Jabłka`, `⚡ Makro`, `📁 Profile`).
- **Prawy wysuwany panel (Drugi sidebar - Statystyki bota)**:
  - Przycisk `[📊]` w prawym górnym rogu paska nagłówka płynnie wysuwa/chowa panel statystyk.
  - **Tło z kotem plażowym (`cat3.jpg`)**: stylowe tło z kotkiem w okularach przeciwsłonecznych i koktajlem na plaży przy zachodzie słońca!
  - **Efekt Frosted Glass (Rozmyte tło za itemami)**: sekcja z listą przedmiotów posiada rozmyte tło (`cat3_blur`) z szklanym, ciemnym przyciemnieniem, dzięki czemu napisy i trójwymiarowe ikony itemów Minecrafta mają doskonały kontrast i czytelność!
  - **Statystyki ogólne**:
    - ⏱ **Łączny czas**: całkowity czas pracy bota (np. `01:52:18`).
    - ⛏ **Wykopane bloki**: łączna liczba wykopanych bloków.
    - 🔄 **Sesje bota**: licznik uruchomień bota.
    - ⚡ **Bloki/h (sesja)**: tempo kopania w bieżącej sesji.
    - 📦 **Podniesione sztuki**: łączna liczba podniesionych przedmiotów.
    - 🗑 **Wyrzucone sztuki**: łączna liczba wyrzuconych śmieci/bloków.
    - 🍖 **Zjedzone sztuki**: łączna liczba zjedzonych posiłków.
    - 💬 **Wysłane komendy**: licznik komend wysłanych na serwer.
  - **Szczegółowa lista przedmiotów**:
    - **Tryb `[Wszystko]`**: widok 3 kolumn obok siebie (`Podniesione`, `Wyrzucone`, `Zjedzone`) z ikonkami Minecrafta i licznikami dokładnie jak na zrzucie ekranu.
    - **Filtry `[Podniesione]`, `[Wyrzucone]`, `[Zjedzone]`**: rozszerzony widok wybranej kategorii na pełną szerokość z pełnymi nazwami, formatowaniem tysięcy i przeliczeniem na stacki.
    - **Płynne przewijanie**: kółko myszy (scroll) oraz przyciski `[▲]` i `[▼]` do przeglądania dowolnej liczby itemów.
    - **Interaktywne tooltips**: najechanie kursorem na dowolny item wyświetla nazwę, dokładną liczbę sztuk, przelicznik na stacki oraz ID w grze.
    - **Przycisk `[✕ Wyzeruj]`**: bezpieczne zerowanie statystyk do zera.
    - **Automatyczny zapis**: wszystkie statystyki zapisywane są trwale w konfiguracji (`kopacz_stats.json`).
- **⛏ Ruch i Stoniarka**:
  - **Tryby trasy bota**:
    - 🔁 **Obieg (Lewo ➔ Tył ➔ Prawo ➔ Przód)**: ruch po obwodzie stoniarki w lewo.
    - 🔁 **Obieg (Prawo ➔ Tył ➔ Lewo ➔ Przód)**: ruch po obwodzie stoniarki w prawo.
    - ↔ **Linia (Prawo ⟷ Lewo)**: ruch wahadłowy wzdłuż wyznaczonej szerokości.
    - 🛑 **Stój w miejscu**: kopanie bez przemieszczania się postaci.
    - 🌀 **Spin (Obracaj się 360° i kop)**: postać obraca się płynnie wokół własnej osi o 360° i ciągle kopie stoniarkę.
      - **Spokojne tempo**: domyślnie `2.0°/tick` (~9 sekund na pełen obrót 360°), dzięki czemu postać nie kręci się za szybko i dokładnie wykopuje każdy odnawiający się blok dookoła.
      - **Pełna regulacja**: przyciski `[-]` i `[+]` oraz klikalne presety tempa (`1.0°`, `1.5°`, `2.0°`, `2.5°`, `3.0°`, `4.0°/tick`) z czytelnym przelicznikiem czasu obrotu.
  - Wybór trybu myszy: trzymanie LPM lub zadany CPS.
  - 🛠 **Wybór narzędzia do kopania (Kilof / Siekiera / Łopata / Motyka)**:
    - Przycisk `[Narzędzie: ⛏ Kilof]` pozwala jednym kliknięciem przełączyć docelowe narzędzie pracy:
      - ⛏ **Kilof** – tradycyjna stoniarka, rudy, kamień, głęboki łupek.
      - 🪓 **Siekiera** – automatyczne rąbanie drewna, pni, kłód i desek.
      - 🥄 **Łopata** – kopanie piasku, żwiru, ziemi, gliny.
      - 🌾 **Motyka** – uprawy, liście, siano, gąbka, sculk.
    - Mod automatycznie wyszukuje i dobiera najlepsze narzędzie danego typu (według tieru i enchantów: Wydajność, Szczęście, Jedwabny dotyk, Niezniszczalność) z hotbara oraz podmienia z ekwipunku.
    - 🔨 **Pełna obsługa naprawy w kowadle**: bot automatycznie naprawia w kowadle wybrane narzędzie (kilof, siekierę, łopatę lub motykę) używając właściwego surowca lub zapasowego narzędzia tego samego typu!
  - 🛡 **Ochrona narzędzia przed zniszczeniem** oraz **automatyczna zmiana** na zapasowe narzędzie wybranego typu.
  - 🍗 **Automatyczne jedzenie podczas kopania (Auto-Food)**:
    - **Wybór slotu z jedzeniem**: kliknij przycisk `[🍱 Slot: ...]`, aby wybrać konkretny slot (`Slot 1` .. `Slot 9`), `Druga ręka` (Offhand) lub `Auto` (dowolny slot z jedzeniem na hotbarze).
    - **Podgląd slotu na żywo**: tooltip w GUI informuje dokładnie, jaki przedmiot i w jakiej ilości znajduje się w wybranym slocie oraz czy jest to zdatne do spożycia jedzenie.
    - **Regulacja progu głodu**: kliknij przycisk `[🍖 Głód: ...]`, aby ustawić, kiedy bot ma zjeść (presety `≤12`, `≤14`, `≤16`, `≤18` pałek głodu z 20).
    - **Płynna automatyzacja**: gdy postać zgłodnieje, bot na ułamek sekundy wstrzymuje ruch, bezpiecznie spożywa posiłek z wybranego slotu, po czym przywraca kilof do ręki i natychmiast kontynuuje kopanie.
    - **Status na HUD**: aktualny stan głodu i informacja o jedzeniu wyświetla się bezpośrednio w lewym górnym rogu ekranu gry.
  - 🔧 **Zakładka: Naprawa (Auto-naprawa komendą lub w kowadle)**:
    - 💬 **Auto-naprawa komendą**:
      - Wpisuje komendę naprawczą na czacie (np. `/repair`, `/fix` lub `/napraw`), gdy kilof ma mało użyć.
      - **Wymóg poziomu XP (Level Check)**: konfigurowalny minimalny poziom gracza (np. `≥30 lvl`, `≥50 lvl` lub brak wymogu).
      - **Wymóg bloku i ilości**: konfigurowalny blok/przedmiot (np. Blok diamentu, Blok złota, Diament) oraz wymagana ilość sztuk w eq (np. 1, 2, 5 sztuk lub pobieranie z trzymanego w ręku przedmiotu).
      - **Inteligentna zamiana kilofa z ekwipunku (Fallback Auto-Swap)**: jeśli gracz nie posiada wymaganego poziomu XP lub nie ma wystarczającej liczby bloków/materiałów do naprawy, bot **automatycznie zamienia kilof na kolejny sprawny kilof z paska lub ekwipunku**.
      - **Bezpieczne zatrzymanie (Stop Protection)**: jeśli w całym ekwipunku nie ma żadnego innego sprawnego kilofa, bot **natychmiast przerywa kopanie i wyłącza się**, w 100% chroniąc cenny kilof przed zniszczeniem!
      - Możliwość ustawienia **drugiej opcjonalnej komendy** (np. `/repair all` lub `/potwierdz`) z regulowanym odstępem czasu (np. 0.5s, 1s, 2s).
      - Regulacja progu trwałości kilofa (`≤10`, `≤20`, `≤30`, `≤50`, `≤100`, `≤200`, `≤500`).
      - Przycisk `[⚡ Przetestuj wpisanie komend teraz]` do natychmiastowego testu na żywo.
    - 🔨 **Auto-naprawa w kowadle**:
      - Pełna automatyzacja naprawy w kowadle: bot przerywa kopanie, odwraca kamerę w stronę kowadła, wkłada zepsuty kilof i diamenty/materiał, odbiera naprawiony kilof i wraca kamerą do kopania!
      - Ustawienie kierunku kowadła (`w lewo ⬅`, `w prawo ➔`, `w tył ⬇`, `w przód ⬆`, `w dół ⤓`, `w górę ⤒`, `własny 🎯`).
      - Przycisk `[🎯 Ustaw z kamery]` i regulacja kąta (Pitch).
      - Przycisk `[⚡ Przetestuj naprawę w kowadle]`.
  - 🔄 **Pod-zakładka: Reconnect (Auto-reconnect & wejście na tryb)**:
    - **Działa tylko podczas kopania**: Auto-Reconnect aktywuje się **wyłącznie**, gdy bot aktywnie kopał w chwili rozłączenia. Gdy grasz ręcznie, bot jest wyłączony lub jesteś na innym serwerze, mod w żaden sposób nie ingeruje w ekran rozłączenia.
    - **Bezpieczna izolacja innych serwerów**: wejście na inny serwer natychmiast resetuje procedurę reconnectu z poprzedniego serwera, nie blokuje klawiszy, nie klika kompasem i nie zamyka ekwipunku ani menu.
    - **Automatyczne ponowne łączenie**: po wyrzuceniu z serwera (kick/restart/disconnect) w trakcie kopania AFK, ekran rozłączenia odlicza czas i łączy z powrotem na serwer, na którym trwało kopanie.
    - **Własne IP serwera**: pole na adres serwera (np. `mc.serwer.pl`). Jeśli zostawisz puste, bot automatycznie połączy się z serwerem, na którym było uruchomione kopanie.
    - **⏺ Nagrywanie kliknięć wejścia na dany tryb**:
      1. W pod-zakładce `Reconnect` kliknij `[⏺ Nagraj kliknięcia]`.
      2. Menu zamknie się, a w lewym górnym rogu ekranu pojawi się status `[NAGRYWANIE WEJŚCIA NA TRYB]`.
      3. Kliknij prawym przyciskiem myszy (PPM) na kompas / przedmiot wyboru trybów, a w otwartym GUI serwera kliknij slot swojego trybu.
      4. Naciśnij klawisz `[K]`, aby zakończyć nagrywanie – sekwencja zostanie natychmiast zapisana i wyświetlona w podglądzie kroków!
    - **⚡ Przetestuj dołączanie na tryb teraz**: przycisk, który od razu wykonuje zapisaną procedurę na żywo w grze (bez konieczności czekania na wyrzucenie).
    - **Alternatywne metody**: możliwość wyboru metody `🧭 Kompas (GUI)` (automatyczne wyszukiwanie po nazwie) lub `💬 Komenda` (np. `/prison`).
    - **Czas w lobby & wznawianie bota**: ustawienie opóźnienia w lobby serwera (domyślnie 2-3s na załadowanie gracza i przedmiotów) oraz automatyczne wznowienie kopania po udanym wejściu.
- **Komendy i Autobloki (`/blokiall`, `/cx`)**:
  - Automatyczne wpisywanie `/blokiall` co zadany czas.
  - **Pełna ochrona listy Zostawiaj**: bot **nigdy nie wyrzuci** bloków mineralnych powstałych z `/blokiall`/`/autobloki`, jeśli dany przedmiot lub jego surowiec znajduje się na liście `🛡 Zostawiaj` (np. dodanie `diamond`, `diament` lub `diamond_block` w 100% chroni bloki diamentu przed wyrzuceniem).
  - **Próg wyrzucania bloków mineralnych**: opcja określająca, ile łącznie bloków musi powstać w ekwipunku, zanim bot je wyrzuci (regulacja przyciskami `[-]`/`[+]` oraz kliknięcie na gotowe presety np. 1, 16, 32, 64, 128, 256, 576 bloków).
  - Automatyczne wytwarzanie CobbleX (`/cx`) przy zadanej liczbie stacków bruku.
- **Wyrzucanie itemów (Drop)**:
  - **Trzy intuicyjne pod-zakładki w opcji Wyrzut**:
    - 📦 **Sloty**: klasyczna siatka 4x9 slotów z podglądem Twoich realnych itemów w czasie rzeczywistym, oznaczeniami slotów i slotem kilofa.
    - 🗑 **Wyrzucaj (N)**: lista śmieci do usunięcia (np. cobblestone, dirt, granit). Bot wyrzuca te przedmioty z ekwipunku.
    - 🛡 **Zostawiaj (N)**: lista cennych przedmiotów chronionych (np. diamond, netherite, złoto). Bot **NIGDY** nie wyrzuci tych przedmiotów!
  - **Dwie niezależne listy (Wyrzucaj vs Zostawiaj)**:
    - 🛡 **Lista do Zostawienia (Ochrona)**: przedmioty na tej liście mają absolutny priorytet – nawet jeśli ich slot zostanie zaznaczony do wyrzutu lub włączony jest tryb listy, bot ich **nigdy nie wyrzuci**.
    - 🗑 **Lista do Wyrzucenia**: przedmioty, których bot ma się pozbywać podczas kopania (wraz z blokami mineralnymi z `/blokiall`).
    - **Dodawanie przedmiotów**: wpisz ID/nazwę i kliknij `[➕ Dodaj]` lub kliknij `[✋ Z ręki]`, aby natychmiast dodać blok trzymany w ręce.
    - **Zarządzanie listami**: kafelki z ikonami przedmiotów, nazwami, przyciskiem `[✕]` do usunięcia, paginacją stron oraz przyciskiem `[🗑 Wyczyść]`.
  - **Tryb: Co wyrzucać**:
    - 📦 **Zaznaczone sloty**: bot sprawdza i wyrzuca przedmioty ze wskazanych slotów w siatce 4x9 ekwipunku (chroniąc listę zostawiania).
    - 🧱 **Itemy z listy**: bot skanuje cały ekwipunek i wyrzuca przedmioty pasujące do listy wyrzutu oraz bloki z `/blokiall` (lista zostawiania i kilofy są zawsze chronione).
  - **Warunki: Kiedy wyrzucać (Wyzwalacze)**:
    - ⏱ **Co jakiś czas (Interwał czasowy)**: regulacja `[-]`/`[+]` oraz klikalne presety (1m, 2m, 3m, 5m, 10m, 15m, 30m lub WYŁ).
    - 📦 **Co ileś stacków (Próg zapełnienia)**: wyrzuca, gdy łączna liczba itemów do wyrzucenia osiągnie wybrany próg (1, 2, 3, 5, 9, 18, 36 stacków lub WYŁ).
    - 🎒 **Gdy full EQ**: natychmiastowe wyrzucenie, gdy w ekwipunku skończy się wolne miejsce.
  - 🎯 **Kierunkowe wyrzucanie przedmiotów (Drop Direction & Kamera)**:
    - **Wybór kierunku wyrzutu**: przycisk `[🧭 Wyrzut: ...]` pozwala wybrać precyzyjny kierunek wyrzucania:
      - `pod siebie ⤓` (Pitch 90° – bezpośrednio pod nogi/stopy, np. do leja zbierającego lub kraty).
      - `w lewo ⬅` (Yaw -90°, Pitch 35° – wyrzucanie w lewo na ziemię/do zsypu).
      - `w prawo ➔` (Yaw +90°, Pitch 35° – wyrzucanie w prawo).
      - `w tył ⬇` (Yaw 180°, Pitch 35° – wyrzucanie za plecy).
      - `w przód ⬆` (Yaw 0°, Pitch 35° – wyrzucanie przed siebie).
      - `w górę ⤒` (Pitch -90° – wyrzucanie prosto w sufit/zbierak).
      - `własny 🎯` (indywidualny kąt pobrany z kamery gracza).
    - 🎯 **Przycisk `[🎯 Ustaw z kamery]` (jak w module Kowadła)**:
      - Stań w docelowym miejscu, spójrz celownikiem dokładnie tam, gdzie bot ma wyrzucać śmieci i kliknij przycisk `[🎯 Ustaw z kamery]`. Mod pobierze i zapisze dokładny kąt patrzenia (Yaw oraz Pitch), ustawi kierunek na `własny 🎯` i wyświetli potwierdzenie na czacie.
    - 📐 **Kąt nachylenia głowy (Pitch)**:
      - Przycisk `[📐 Pitch: ...]` pozwala cyklicznie przełączać kąt pionowy wyrzutu (`90° pod siebie`, `60° stromo w dół`, `35° naturalnie na ziemię`, `0° na wysokości oczu`, `-90° w górę`).
    - 🛡 **Płynny, realistyczny ruch kamery (Anti-Cheat Safe)**:
      - W momencie wyzwolenia wyrzutu bot wstrzymuje ruch, płynnie obraca kamerę w stronę wyznaczonego miejsca (z ludzkim wygładzaniem ruchu bez teleportera, w 100% niewykrywalnym przez GrimAC i Vulcan), otwiera ekwipunek, wyrzuca przedmioty ze wskazanych slotów w wybranym kierunku, bezpiecznie zamyka okno i płynnie przywraca kamerę dokładnie na stoniarkę, wznawiając kopanie!
  - **Tryby dla każdego slotu indywidualnie** na siatce 4x9:
    - 🟩 **`↓` (Zielony)**: wyrzuca cały stack ze slotu.
    - 🟧 **`↓1` (Złoty / Pomarańczowy)**: wyrzuca nadmiar, zostawiając dokładnie 1 item (blokuje slot przed wpadaniem innych śmieci).
    - ⬛ **Szary**: slot ignorowany (brak wyrzucania).
    - 🟦 **`⛏` (Niebieski)**: chroniony slot kilofa na hotbarze.
  - **Podgląd slotów w GUI**: każdy slot wyświetla aktualnie trzymany item z gry, a tooltip informuje, czy dany item jest bezpieczny, czy zostanie wyrzucony zgodnie z filtrem bloków.
  - **Sterowanie slotami**:
    - **L-Klik**: cykliczne przełączanie (`Brak` $\rightarrow$ `Cały stack` $\rightarrow$ `Zostaw 1` $\rightarrow$ `Brak`).
    - **P-Klik na ekwipunku**: szybkie ustawienie trybu `Zostaw 1`.
    - **P-Klik na hotbarze**: oznaczenie jako kilof `⛏`.
  - **Przyciski masowe**: `[↓ Cały stack]`, `[↓1 Zostaw 1]` oraz `[✕ Odznacz]`.
  - Wyrzucanie po zadanym czasie, po uzbieraniu stacków lub gdy ekwipunek jest pełny (w 100% w tle, bez utraty kopania).
- **🍎 Jabłka (Automatyczna farma jabłek z liści)**:
  - Dedykowana zakładka umieszczona bezpośrednio pod zakładką **💬 Czat**.
  - **Płynny cykl stawiania i ścinania**:
    - Stawia liście z wybranego slotu (domyślnie **Slot 2**) przez `0.25 s` (prawy przycisk myszy - PPM).
    - Następnie niszczy postawione liście nożycami z wybranego slotu (domyślnie **Slot 1**) przez `0.25 s` (lewy przycisk myszy - LPM).
    - Pełna regulacja czasów stawiania i ścinania (`[-]`/`[+]` oraz presety co 0.05s).
  - **Automatyczne uzupełnianie liści (Auto-Refill)**:
    - Gdy skończą się liście w slocie hotbara, bot sam otwiera ekwipunek i dobiera kolejny stack dowolnych liści (`LeavesBlock`) z głównego ekwipunku (sloty 9..35) do wyznaczonego slotu na pasku.
  - **Inteligentna naprawa i obsługa komendy `/repair`**:
    - Licznik użyć nożyc: bot automatycznie wysyła komendę `/repair` co zadany próg (domyślnie co `10` użyć nożyc).
    - Możliwość włączenia/wyłączenia naprawy `/repair` oraz zmiany komendy i progu użyć.
  - **Automatyczny crafting nowych nożyc w siatce 2x2**:
    - Gdy na serwerze nie ma komendy `/repair` lub jest wyłączona, a nożyce się zużyją i pękną:
    - Bot automatycznie otwiera ekwipunek podręczny (`E`), pobiera 2 sztabki żelaza (`iron_ingot`), układa je po przekątnej w siatce craftingu 2x2 (sloty 1 i 4), odbiera nowo stworzone nożyce i wkłada je bezpośrednio do Slotu 1 hotbara!
    - Po skończonym craftingu natychmiast płynnie wznawia cykl farmy jabłek.
  - **Status na żywo na ekranie (HUD)**:
    - Aktualna czynność (`Stawianie liści (PPM)...`, `Ścinanie nożycami (LPM)...`, `Uzupełnianie liści...`, `Crafting nożyc w 2x2...`, `/repair...`) wyświetla się bezpośrednio na HUD w lewym górnym rogu ekranu gry.
- **📦 Skrzynie (Auto-Chest Module - automatyczna obsługa skrzyń)**:
  - Trzecia zakładka w menu bota (`[ 📦 Skrzynie ]`).
  - **Pełna automatyzacja urobku i zapasów**:
    - Bot automatycznie wykrywa najbliższą skrzynię lub Ender Chesta w pobliżu stoniarki.
    - Po zapełnieniu ekwipunku lub uzbieraniu wyznaczonej liczby stacków cennych surowców, bot płynnie wstrzymuje kopanie, obraca kamerę w stronę skrzyni, otwiera ją prawym przyciskiem myszy, odkłada wszystkie wskazane surowce i cenne minerały, po czym dobiera brakujące sprawne kilofy oraz zapasowe jedzenie.
    - Po skończeniu automatycznie zamyka skrzynię i natychmiast wraca kamerą dokładnie na stoniarkę, wznawiając kopanie!
  - **Tryby działania skrzyni**:
    - **`[ 📤 Odkładaj do skrzyni ]`**: przenosi wyznaczone surowce i minerały z ekwipunku gracza do skrzyni.
    - **`[ 📥 Bierz ze skrzyni ]`**: pobiera wyznaczone przedmioty i zapasy ze skrzyni do ekwipunku gracza.
    - **`[ 🔄 Odkładaj i Bierz ]`**: tryb łączony – w trakcie jednego podejścia do skrzyni najpierw bezpiecznie odkłada surowce z listy odkładania, a następnie dobiera wskazane przedmioty z listy pobierania!
  - **Główny włącznik i test**:
    - Przełącznik **`[ 📦 Auto-Chest: WŁ / WYŁ ]`**.
    - Przełącznik trybu działania skrzyni **`[ 📤 Odkładaj ]` / `[ 📥 Bierz ]` / `[ 🔄 Odkładaj i Bierz ]`**.
    - Przycisk **`[ ⚡ Przetestuj ]`** – wykonuje natychmiast procedurę na żywo w grze i wyświetla w dymku (tooltipie) odległość oraz nazwę wykrytej skrzyni (np. `Ender Chest [2.1m]` lub `Beczka [1.8m]`).
  - **Dobieranie zapasów (Restock kilofów i jedzenia)**:
    - **⛏ Kilofy**: włącznik `[ ⛏ Kilofy: WŁ / WYŁ ]` z regulacją minimalnej liczby sprawnych kilofów w ekwipunku (`1` .. `9`). Jeśli masz mniej sprawnych kilofów, bot wyciąga je ze skrzyni.
    - **🍖 Jedzenie**: włącznik `[ 🍖 Jedzenie: WŁ / WYŁ ]` z regulacją minimalnej liczby sztuk jedzenia w ekwipunku (`4` .. `128`).
  - **Zasięg & Filtry typów skrzyń**:
    - **Zasięg**: regulacja od `1.5m` do `6.0m` (domyślnie `4.5m`) przyciskami `[-]`/`[+]` oraz klikalnymi presetami (`2.5m`, `3.5m`, `4.5m`, `5.0m`, `5.5m`).
    - **Ender Chest**: włącznik `[ Ender Chest: WŁ / WYŁ ]` – obsługa prywatnej skrzyni kresu.
    - **Zwykłe/Beczki**: włącznik `[ Zwykłe/Beczki: WŁ / WYŁ ]` – obsługa skrzyń zwykłych, skrzyń-pułapek, beczek (`Barrel`) oraz skrzyń shulkerowych (`Shulker Box`).
  - **Wyzwalacze uruchomienia**:
    - **Gdy pełny ekwipunek**: bot odkłada/pobiera surowce natychmiast, gdy skończy się wolne miejsce w głównym ekwipunku gracza.
    - **Po stackach cennych surowców**: włącznik z regulacją progu (`1` .. `10` stacków).
  - **Niezależne listy przedmiotów (Do odłożenia vs Do pobrania)**:
    - Pod-zakładka **`[ 📤 Do odłożenia (N) ]`**: lista przedmiotów i minerałów, które bot ma chować do skrzyni.
    - Pod-zakładka **`[ 📥 Do pobrania (N) ]`**: lista przedmiotów, które bot ma wyjmować ze skrzyni do swojego ekwipunku (np. złote jabłka, zapasowe mikstury, jedzenie, koks).
    - Pole tekstowe do wpisania dowolnego ID przedmiotu (np. `diamond`, `golden_apple`, `bread`, `emerald`).
    - Przycisk **`[ ➕ Dodaj ]`** – dodanie wpisanego przedmiotu do aktywnej listy.
    - Przycisk **`[ ✋ Z ręki ]`** – błyskawiczne dodanie do aktywnej listy przedmiotu trzymanego aktualnie w prawej ręce!
    - Interaktywne kafelki z ikonami 3D przedmiotów z Minecrafta, pełnymi nazwami, tagami (`📦 ODKŁADANY` / `📥 POBIERANY`) i przyciskiem `[ ✕ ]` do usuwania.
    - Paginacja stron oraz przycisk `[ 🗑 Wyczyść ]` dla aktualnie wybranej listy.
- **⚡ Makro (Własne sekwencje & Gotowce)**:
  - Ósma zakładka w menu bota, podzielona na dwie pod-zakładki: **`[ ⚡ Własne ]`** oraz **`[ 📦 Gotowce (N) ]`**.
  - **⚡ Własne (Nagrywanie i edytor)**:
    - **Wybór trybu nagrywania makra**:
      - **`[ 🎬 Same sekwencje ]`**: nagrywa wyłącznie czyste sekwencje akcji (komendy czatu, otwieranie/zamykanie GUI, klikanie slotów, użycia przedmiotów). Ignoruje ruch postaci (WASD, skoki) oraz obroty kamerą myszką – idealne do szybkich makr sklepu, targu, automatycznego handlu i craftingu bez ruszania celownikiem.
      - **`[ 🎬 Ruch i Kamera ]`**: pełne makro z rejestracją chodzenia po świecie (klawisze W, S, A, D, Spacja, Shift, Sprint) oraz ciągłych, płynnych kątów obrotu kamery (Yaw i Pitch).
    - **Nagrywanie na żywo (Live Recorder)**:
      - Kliknij `⏺ Rozpocznij nagrywanie` w menu `[K]`.
      - Mod przechodzi w tryb nagrywania z pulsującym wskaźnikiem na ekranie gry (`🔴 NAGRYWANIE WŁASNEJ SEKWENCJI` z informacją o wybranym trybie: Same sekwencje lub Ruch i Kamera).
      - Wpisuj dowolne komendy na czacie (np. `/sklep`, `/rynek`, `/crafting`, `/fix`) – zostaną automatycznie zarejestrowane.
      - Otwieraj menu i klikaj dowolne sloty / przedmioty – mod precyzyjnie zarejestruje indeks slotu, przycisk myszy (LPM/PPM) oraz nazwę przedmiotu.
      - Zamykanie menu klawiszem `E` / `ESC` zostaje zarejestrowane jako krok zamknięcia GUI.
      - Naciśnij klawisz `[K]`, aby zakończyć nagrywanie – mod zapisze wszystkie kroki i otworzy menu w zakładce `Makro ➔ Własne`.
    - **Zapisywanie do Gotowców**:
      - Wpisz nazwę gotowca (np. `RynekDiamenty`, `AutoSell`) w pole i kliknij `[ 💾 Zapisz w Gotowcach ]`.
      - Twoja sekwencja trafi prosto do bazy gotowych makr i zostanie zapisana w pliku `.json`.
    - **Odtwarzanie i Testowanie**:
      - Przycisk `⚡ Przetestuj sekwencję` natychmiast uruchamia nagraną sekwencję w grze krok po kroku (płynny ruch postaci, obroty kamery, komendy i kliknięcia).
      - **Warunki automatycznego uruchamiania sekwencji w bocie AFK**:
        - ⏱ **Czas**: Cyklicznie co zadany czas (np. co 60 sekund z presetami 15s, 30s, 60s, 120s, 180s, 300s, 600s).
        - ⚡ **Poziom XP**: Automatyczny start po osiągnięciu zadanego poziomu doświadczenia (np. po wbiciu 200 lvl XP z presetami 50, 100, 150, 200, 250, 300, 400, 500 lvl).
        - 📦 **Ilość bloku (Dowolny blok/przedmiot)**: Automatyczny start po uzbieraniu w ekwipunku zadanej liczby dowolnego bloku lub przedmiotu:
          - Możesz wpisać dowolne ID lub nazwę bloku (np. `cobblestone`, `diamond`, `obsidian`, `emerald`, `ancient_debris`).
          - Przycisk **`✋ Z ręki`** automatycznie pobiera i ustawia przedmiot trzymany w prawej ręce!
          - Regulacja progu sztuk `[-]`/`[+]` oraz presety (1, 16, 32, 64, 128, 256, 576 szt. / 9 st., 1152, 2304 / full EQ).
      - Regulacja opóźnienia między krokami (delay ticks / ms).
      - Przeglądanie listy kroków z paginacją (`[◀]` / `[▶]`) i możliwością usuwania poszczególnych akcji (`✖`).
      - Pole do ręcznego dodawania komend oraz przycisk `🗑 Wyczyść`.
  - **📦 Gotowce (Baza gotowych makr, AutoBuyTotem & Auto-Chest)**:
    - **🛡 Karta: AutoBuyTotem**:
      - Automatyczny zakup totemu w `/sklep` po osiągnięciu zadanego poziomu doświadczenia (XP).
      - Regulacja progu XP (`[-] [200 lvl] [+]`), opóźnienia kliknięć (`[-] [10 t] [+]`) oraz komendy sklepu (domyślnie `/sklep`).
      - Przycisk `[ ⚡ Przetestuj zakup totemu ]` – natychmiastowy zakup testowy w grze.
      - Przycisk `[ 📂 Wczytaj do edytora (Własne) ]` – ładuje wszystkie 5 kroków zakupu totemu do edytora `Własne`.
    - **📦 Karta: Auto-Chest (Skrót)**:
      - Szybki przełącznik modułu Auto-Chest bez wchodzenia do osobnej zakładki.
      - Przycisk szybkiego testu `[ ⚡ Przetestuj ]` oraz przycisk `[ 📦 Opcje skrzyń ➔ ]` natychmiast przekierowujący do pełnej konfiguracji skrzyń.
    - **Zarządzanie zapisanymi makrami**:
      - Każde nagrane makro możesz zapisać pod własną nazwą.
      - Przycisk `[ ⚡ Odtwórz ]` – natychmiastowe jednorazowe wykonanie danego makra w grze.
      - Przycisk `[ 📂 Edytuj ]` – załadowanie makra do edytora w pod-zakładce `Własne`.
      - Przycisk `[ ✖ ]` – usunięcie wybranego gotowca.
      - Przycisk `[ 📂 Otwórz folder z makrami na dysku ]` – otwiera katalog `.minecraft/config/kopacz_macros/` w eksploratorze Windows do udostępniania i tworzenia kopii zapasowych gotowych plików makr.
- **📁 Profile (Zarządzanie zapisanymi konfiguracjami)**:
  - Szósta zakładka w menu pod klawiszem `[K]`.
  - **Zapisywanie profili**:
    - Wpisz własną nazwę konfiguracji w pole tekstowe (np. `Prison`, `SkyBlock`, `Stoniarka1`, `Kopalnia`) i kliknij `[💾 Zapisz profil]`.
    - Aktualne ustawienia bota (trasa, czasy, komendy, filtry wyrzucania, zaznaczone sloty, sekwencje makro) zostaną trwale zapisane w osobnym pliku `.json`.
  - **Przełączanie i wczytywanie**:
    - Kliknij `[📂 Wczytaj]` przy dowolnym profilu – mod natychmiast załaduje wszystkie zapisane opcje i zaktualizuje GUI w locie.
    - Aktywny profil jest oznaczony zieloną gwiazdką (`★`).
  - **Zarządzanie**:
    - Przycisk `[💾 Zapisz]` przy profilu pozwala szybko nadpisać istniejący profil aktualnymi opcjami.
    - Przycisk `[✖]` usuwa zbędny profil z listy.
    - Paginacja stron (`[◀]`/`[▶]`) przy większej liczbie konfiguracji.
  - **Dostęp do plików**:
    - Przycisk `[📂 Otwórz folder z profilami na dysku]` jednym kliknięciem otwiera folder `.minecraft/config/kopacz_profiles/` w eksploratorze Windows, umożliwiając łatwe kopiowanie i dzielenie się profilami ze znajomymi.
- **📊 Boczny panel statystyk (Prawy side-bar z kotem cat3.jpg)**:
  - Otwierany przyciskiem **`[📊]`** / **`[▶]`** w prawym górnym rogu menu głównego.
  - **Dynamiczne centrowanie i zero kolizji**: menu automatycznie przesuwa się i balansuje na ekranie, dzięki czemu panel główny i boczny side-bar nigdy na siebie nie nachodzą niezależnie od skali interfejsu (GUI Scale).
  - **Czysty start od zera**: statystyki rozpoczynają się całkowicie wyzerowane i naliczają się na żywo wyłącznie w trakcie aktywnego kopania bota.
  - **Przezroczyste szklane przyciski kategorii**:
    - 3 niezależne kategorie: **`[Podniesione]`**, **`[Wyrzucone]`**, **`[Zjedzone]`**.
    - Szklane, przezroczyste tło przycisków sprawia, że zdjęcie kota na plaży (`cat3.jpg`) jest idealnie widoczne w tle.
  - **Karta statystyk ogólnych**:
    - Czas pracy bota, wykopane bloki, liczba sesji, tempo wydobycia (Bloki/h).
    - Liczba podniesionych przedmiotów, wyrzuconych sztuk, zjedzonego jedzenia i wysłanych komend.
  - **Lista przedmiotów z efektem Frosted Blur**:
    - Lekko rozmyte tło z ciemnym szklanym filtrem dla maksymalnego kontrastu i czytelności.
    - **Cenne surowce zawsze na samej górze w parach (Blok + Surowiec)**:
      - Najcenniejsze minerały są priorytetowo wyświetlane na samym szczycie listy z logicznym parowaniem:
      - 🟡 **Blok złota** $\rightarrow$ od razu pod nim **Sztabka złota** $\rightarrow$ Surowe złoto $\rightarrow$ Samorodek
      - 💎 **Blok diamentu** $\rightarrow$ od razu pod nim **Diament**
      - ⬛ **Blok netherytu** $\rightarrow$ od razu pod nim **Sztabka netherytu** $\rightarrow$ Pradawne zgliszcza $\rightarrow$ Odłamek
      - 🟢 **Blok szmaragdu** $\rightarrow$ **Szmaragd**
      - ⚪ **Blok żelaza** $\rightarrow$ **Sztabka żelaza**
      - 🔵 **Blok lazurytu** $\rightarrow$ **Lazuryt**, **Blok redstone** $\rightarrow$ **Redstone**, **Blok węgla** $\rightarrow$ **Węgiel**, **Blok miedzi** $\rightarrow$ **Sztabka miedzi** itd.
      - Pozostałe bloki masowe (cobblestone, kamień, ziemia) są wyświetlane poniżej, posortowane malejąco według ilości.
    - Ikony przedmiotów 16x16, nazwy oraz liczby sztuk.
    - Płynne przewijanie kółkiem myszy i przyciskami `[▲]` / `[▼]`.
    - Podgląd szczegółowych informacji w szklanym tooltipie po najechaniu myszą (ilość sztuk, stacki, registry ID).
  - **Przycisk `[✕ Zeruj]`**: natychmiastowe czyszczenie wszystkich liczników w pliku `config/kopacz_stats.json`.

