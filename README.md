Aby uruchomić aplikację należy:

Lokalnie:
Wymagania:
- Python 3.9 lub nowszy
- Zainstalowane zależności z requirements.txt

Kroki:
1. Sklonuj repozytorium:
    git clone https://github.com/twoj_uzytkownik/ml-api.git
    cd ml-api

2. Utwórz i aktywuj środowisko wirtualne (opcjonalne, ale zalecane):
    python -m venv .venv
    .venv\Scripts\activate 
   
3. Zainstaluj zależności:
    pip install -r requirements.txt
   
5. Uruchom aplikację:
    python app.py

Aplikacja będzie dostępna pod adresem: http://localhost:5000

Za pomocą Dockera
Wymagania:
- Zainstalowany Docker

Kroki:
1. Zbuduj obraz Dockera:
    docker build -t ml-api .

2. Uruchom kontener:
    docker run -p 5000:5000 ml-api

Aplikacja będzie dostępna pod adresem: http://localhost:5000

Dodatkowe opcje:

Uruchom w tle (detach mode):
    docker run -d -p 5000:5000 ml-api

Uwzględnij zmienne środowiskowe:
    docker run -p 5000:5000 -e FLASK_ENV=production ml-api

Za pomocą Docker Compose
Wymagania:
- Zainstalowany Docker i Docker Compose

Kroki:
1. Uruchom usługi:
    docker-compose up

Aplikacja będzie dostępna pod adresem: http://localhost:5000, a Redis na porcie 6379

Dodatkowe opcje:

Uruchom w tle:
    docker-compose up -d

Zatrzymaj usługi:
    docker-compose down
