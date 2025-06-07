# MongoDB Test Service

## Opis projektu
MongoDB Test Service to prosta aplikacja w Pythonie, która testuje połączenie z bazą danych MongoDB, wykonuje podstawowe operacje CRUD oraz generuje raporty z wynikami testów w formatach HTML, CSV oraz ZIP.

## Funkcjonalności
- Testowanie połączenia z MongoDB
- Wstawianie i odczyt dokumentów z kolekcji
- Sprawdzanie zachowania pustej kolekcji
- Walidacja struktury dokumentów
- Generowanie raportów w formacie HTML i CSV
- Pakowanie raportów do archiwum ZIP

## Technologie
- Python 3.x
- Flask (opcjonalnie, jeśli chcesz rozszerzyć projekt o API)
- pymongo

## Instrukcja uruchomienia lokalnego

### Wymagania
- Python 3.7+
- MongoDB Atlas lub lokalna instancja MongoDB
- Virtualenv (zalecane)

### Kroki

1. Sklonuj repozytorium:
bash
git clone https://github.com/TwojLogin/mongodb-test-service.git
cd mongodb-test-service

Utwórz i aktywuj wirtualne środowisko:

bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# Linux/Mac
source .venv/bin/activate
Zainstaluj zależności:

bash
pip install -r requirements.txt
Ustaw zmienną środowiskową MONGO_URI na adres swojej bazy MongoDB:

Windows (PowerShell):

powershell
$env:MONGO_URI="mongodb+srv://user:password@cluster.mongodb.net/?retryWrites=true&w=majority"

Linux/Mac:

bash
export MONGO_URI="mongodb+srv://user:password@cluster.mongodb.net/?retryWrites=true&w=majority"
Uruchom aplikację:

bash
python app.py
Po uruchomieniu, w folderze projektu pojawią się pliki:

raport.csv
raport.html
raport_mongodb.zip (zawiera powyższe raporty)

Instrukcja wdrożenia na Render.com (opcjonalnie)
Załóż konto na Render.com i połącz z GitHubem.

Stwórz nowy Web Service, wybierając swoje repozytorium.

Dodaj zmienną środowiskową MONGO_URI w ustawieniach usługi (upewnij się, że hasło jest URL encoded).

Ustaw komendę startową (np. python app.py lub flask run).

Po wdrożeniu aplikacja będzie dostępna pod publicznym adresem URL Render.
