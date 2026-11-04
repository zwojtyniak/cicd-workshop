# Baseline — pomiar stanu wyjściowego

Plik uzupełniasz w ZADANIU 01. Czasy odczytujesz w zakładce **Actions**. Wystarczy dokładność
do sekundy.

## Czasy kroków — przebieg na `main`

| Krok                        | Czas   |
|:----------------------------|:-------|
| Set up job                  | 1 s     |
| Checkout                    | 1  s    |
| Set up Node                 | 0 s     |
| Install dependencies        | 41 s    |
| Install Playwright browsers | 17  s   |
| Unit tests                  | 1  s    |
| API tests                   | 20 s   |
| UI tests                    | 2m 28s |
| Upload Playwright report    | 3s     |
| Post Set up Node            | 0s     |
| Post Checkout               | 1s     |
| Complete job                | 0s     |
| **Cały przebieg**          | 3m 56s |

## Czas do pierwszego czerwonego sygnału

| Branch                | Czas samego testu | Od startu przebiegu do informacji o błędzie |
|:----------------------|:------------------|:----------------------------------------------|
| `demo/failing-unit`   | 1m 2s             | 57s                                           |
| `demo/failing-search` | 4m 41s            | 4m 36s                                        |

Co na `demo/failing-unit` stało się z testami API i UI:

## `demo/failing-lint` i `demo/failing-security`

| Branch                  | Wynik przebiegu | Dlaczego tak |
|:------------------------|:----------------|:-------------|
| `demo/failing-lint`     | 4m success      |              |
| `demo/failing-security` | 3m57s success   |              |

## Pięć problemów obecnego pipeline’u

1.
2.
3.
4.
5.

## Pomiary z kolejnych zadań

Zadanie 3:

Ad 5:
czas kroku Install dependencies: 25s
czas kroku Install Playwright browsers: 8s
całkowity czas przebiegu: 3m 25s

Ad 6:
w logu kroku Cache Playwright browsers powinien pojawić się komunikat Cache restored from key, - tak
krok Install Playwright browsers powinien zostać pominięty i mieć szarą ikonę, - tak
cały przebieg powinien być o kilka sekund krótszy. Większej różnicy nie będzie, bo najdłużej trwają testy UI, a nimi zajmiemy się później.: 3m 14s

Co	Przed	Po
Czas do informacji o błędzie lintu	nigdy	?
Install dependencies	6 s	? 20s
Instalacja przeglądarek, pierwszy przebieg	8s s	?
Instalacja przeglądarek, drugi przebieg	18 s	? 0s
Cały przebieg	3:25s	? 3m14s

