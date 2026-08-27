# parking-app


jak ma działać aplikacja i cały algorytm.

Idea:
Użytkownik otwiera aplikację i widzi mapę miasta. Na tej mapie znajdują się markery dostępnych parkingów.Po kliknięciu na marker użytkownik widzi: nazwę parkingu lub ulicę, ogólną liczbę miejsc, liczbę miejsc dostępnych, liczbę miejsc zajętych
Użytkownik wybiera interesujący go parking i może zobaczyć schemat tego parkingu.Na schemacie każde miejsce ma swój numer, np.:
M1 zajęte, kolor czerwony
M2 wolne, kolor zielony
M3 wolne, kolor zielony itd. Użytkownik może wybrać interesujący go parking oraz zbudować trasę do niego.

Kamery:
Mamy jedną na wjezdzie drugą na wyjezdzie. Zakładamy ze oba wjazdy są jednocześnie wyjazdami. Oznacza to że karemy mają działać w podobny sposób. Każda kamera pobiera dane i przekazuje je do systemu.

//Załóżmy ze mamy odliczoną ilość miejsc na parkingu. Każde miejsce jest oznaczone liniami. ale auta stali nie obok siebie a np rzez jesno miejsce | W | W | W | S | W | S | W | W | W | (S - samochód, W - miejsce wolne).

//Załózmy że kamera nie złapała całego numeru reestracyjnego (np. GS820 a nie GS8204G). 
--System może wykorzystywać dane z parkometru jako dodatkowe źródło informacji w przypadku niepełnego lub niepewnego odczytu numeru rejestracyjnego.
I takim sposobem w sumie możemy też sprawdzać ile osób kupuje bilety(latwiej dla pani sprawdzającej) i o której godzinie. Ona będzie odrazu wiedziała które to auto, za ile minut po wjechaniu kupił ten bilet oraz ewentualnie za jaki czas ma tam pójść.

Przy wyjezdzie zparkingu kamera tak samo sczytuje numer oraz miejsce do którego trn samochód jest przypisany. status miejsca się zmienia na "Wolny"

//Mamy jeden pas dla wjazdu drugi do wyjazdu. Kiedy ona reestruje że samochód wjechał i tak musi poczekać aż wjedzie na któreś miejsce

Baza:
Co ma się znajdować:
    Apka:
nazwa parkingu
adres
współrzędnych
liczbie wszystkich miejsc
liczbie miejsc wolnych
liczbie miejsc zajętych
Ilość miejsc wolnych/zajętych
    Każde miejsce parkingowe powinno mieć:
numer miejsca, np. M1, M2, M3
status, np. wolne lub zajęte
    System powinien przechowywać:
numer rejestracyjny samochodu
parking, na którym znajduje się samochód
miejsce, na którym znajduje się samochód
czas wjazdu
czas wyjazdu
informację o bilecie, jeżeli parking korzysta z parkometru

Aplikacja:
//Można tez dodac ceny tych parkingów
1)Strona główna:
Użytkownik otwiera aplikacje i widzi mape miasta oraz dostępne parkingi(z jego lokalizacji). Wybiera klikając jego marker
2)Po wybraniu parkinga:
Widzi nazwę parkingu, agres, liczbę wscwstkich, zajętych i wolnych miejsc. Do tego może być przycisk "Pokaz miesca" i "Nawiguj"
"Pokaż miejsca"
Po wybraniu tej opcji użytkownik muszi widzieć układ tego parkingu oraz miejca wolne/zajęte
"Nawiguj"
Po wybraniu opcji „Nawiguj” aplikacja może uruchomić nawigację do wybranego parkingu.

Computer vision:
Kamera muszi wykryć samochód. Następnie go numer. Złapanie na które miejsce wjezdza samochód i przywiązanie go do tego miejsca. Na tej podstawie status miejsca zostaje zmieniony na „zajęte”. Po wyjeździe tego samochodu system ponownie odczytuje numer rejestracyjny i zmienia status na "wolny"



Wygląd: 
https://www.figma.com/board/QTf6EXzLwUsUHnzM9j9nfG/plan-parking?t=LPDDbDKA48CEB9if-6
https://www.figma.com/design/wAoru9nATrqZ6fIp9fhnbL/parking-app?node-id=0-1&t=184tLAITmYMnjAbL-1







