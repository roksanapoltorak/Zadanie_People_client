# Zadanie_People_client

Uzupełnienie naszego klienta Restowego API o następujące metody:
  - delete_by_id: metoda ta powinna usuwać osobę o podanym ID. W razie braku odpowiedniego użytkownika rzucony powinien zostać wyjątek.
  - delete_by_name: metoda usuwająca wszystkich użytkowników posiadających dane imię. Nie rzuca wyjątku ale zwraca liczbę usuniętych ludzi.
  - add_from_file: metoda odczytująca z danego pliku rekordy osób a następnie dodająca je wszystkie używając metod RESTowego API.

Na przykład, zakładając, że client jest instancją naszej klasy PeopleClient:
client.delete_by_id(12) # usuwa osobę o id=12 lub rzuca wyjątek, jeśli takiej osoby nie ma,
client.delete_by_name('Janusz') # powinno usunąć wszystkich ludzi o imieniu Janusz i zwrócić ich usuniętą liczbę,
client.add_from_file(my_file) # Odczytuje osoby z pliku my_file i dodaje je wykonując odpowiednie zapytania.

Uwaga: 
- metody mogą wykonywać po więcej niż jedno zapytanie o ile jest to konieczne. 
- sygnatury metod, jak również spodziewane przez nie typy argumentów ustalacie sami, oczywiście w oparciu o omawiane na naszych spotkaniach dobre praktyki i zdrowy rozsądek.
- format pliku oczekiwany przez add_from_file jest dowolny, w szczególności może to być jeden z formatów obsługiwanych natywnie przez Pythona (json, csv, cokolwiek).
- do wywołania żądania DELETE służy funkcja requests.delete - w razie wątpliwości moduł requests ma przystępną dokumentację: http://docs.python-requests.org/en/master/
