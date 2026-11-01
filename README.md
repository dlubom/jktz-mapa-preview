# Podgląd mapy JKTZ

**[Otwórz stronę testową](https://dlubom.github.io/jktz-mapa-preview/)**

Jedna strona pokazuje wybrany otwarty PR z [dlubom/jktz-mapa](https://github.com/dlubom/jktz-mapa).

1. Otwórz [Preview selected PR](https://github.com/dlubom/jktz-mapa-preview/actions/workflows/preview.yml).
2. Wybierz Run workflow na main i wpisz numer PR.
3. Poczekaj na zielone resolve, build i publish. Strona pokaże numer PR i commit.

Pełny ZIP jest dostępny w Artifacts przez 15 dni. Rozpakuj go i uruchom `python3 serve.py`
(Python 3.9+), a następnie otwórz wypisany adres. Podkłady wymagają internetu.

Nowy udany Run zastępuje poprzedni podgląd. Nieudany build nie zmienia strony.
Zmiana head/base PR lub nowszy wybór blokuje starszy Run; do ponownego wyboru użyj nowego Run workflow.

To repozytorium zawiera tylko zaufaną konfigurację publikatora. Kod PR budowany jest na
osobnym runnerze, bez sekretów i uprawnień do publikacji. Dane nie trafiają do Git.

Źródła konfiguracji: `.github/preview-repository/preview.yml`, `scripts/preview.py`
i `scripts/preview-server.py` w repozytorium mapy. Aktualizacje konfiguracji przechodzą przez PR.
Produkcja pod adresem `https://dlubom.github.io/jktz-mapa/` jest publikowana osobno.
