# Giełda Książek - Webowa Platforma Wymiany i Sprzedaży

Webowa aplikacja typu giełda książek, która umożliwia użytkownikom rejestrację, logowanie, zarządzanie własnym profilem oraz dodawanie ogłoszeń dotyczących książek na wymianę lub sprzedaż. Użytkownicy mogą przeglądać dostępne oferty, kontaktować się z innymi ogłoszeniodawcami za pomocą wbudowanego systemu wiadomości oraz personalizować swoje profile, dodając m.in. avatar i opis.

Projekt został stworzony przy użyciu PHP po stronie backendu oraz standardowych technologii frontendowych (HTML, CSS, JavaScript). Baza danych MySQL służy do przechowywania informacji o użytkownikach, książkach i wiadomościach.

## Kluczowe Funkcjonalności:

* **Uwierzytelnianie i Autoryzacja:**
    * Rejestracja nowych użytkowników.
    * Logowanie i wylogowywanie.
    * System sesji.
* **Zarządzanie Profilem Użytkownika:**
    * Wyświetlanie profilu własnego oraz innych użytkowników.
    * Możliwość edycji własnych danych (nazwa użytkownika, email, opis).
    * Możliwość zmiany hasła.
    * Przesyłanie i wyświetlanie avatara profilowego (z domyślnym obrazkiem placeholder).
* **Ogłoszenia Książkowe:**
    * Dodawanie nowych ogłoszeń książkowych (tytuł, autor, ISBN, opis, cena/wymiana).
    * Przesyłanie i wyświetlanie zdjęć okładek książek (z domyślnym obrazkiem placeholder).
    * Przeglądanie listy dostępnych książek.
    * Wyświetlanie szczegółów pojedynczej książki.
    * Możliwość usunięcia własnych ogłoszeń książkowych.
* **Komunikacja:**
    * System prywatnych wiadomości między użytkownikami.
    * Inicjowanie rozmowy z poziomu ogłoszenia książkowego.
    * Skrzynka odbiorcza (`messages.php`) z listą wątków konwersacji.
    * Podgląd pełnej konwersacji w danym wątku (`view_thread.php`) z możliwością odpowiedzi.
    * Wskaźnik nieprzeczytanych wiadomości.
* **Interfejs Użytkownika:**
    * Responsywny design dostosowany do różnych rozmiarów ekranu.
    * Stylizacja wiadomości inspirowana popularnymi komunikatorami (np. WhatsApp/Messenger).
    * Spersonalizowane logo strony.

## Użyte Technologie:

* **Frontend:**
    * HTML5
    * CSS3 (Flexbox, Grid, RWD)
    * JavaScript (drobne usprawnienia, walidacja po stronie klienta - *jeśli dodano*)
* **Backend:**
    * PHP (wersja 7.x lub nowsza)
* **Baza Danych:**
    * MySQL
* **Serwer WWW (środowisko deweloperskie):**
    * np. XAMPP, WAMP, MAMP (lub inny serwer obsługujący PHP i MySQL)
* **Kontrola Wersji:**
    * Git
    * GitHub

## Struktura Projektu:

/giełda_ksiazek_php/
|-- config/             # Pliki konfiguracyjne (np. połączenie z DB)
|-- includes/           # Wspólne elementy strony (header, footer)
|-- public/             # Główny folder dostępny publicznie (document root)
|   |-- css/            # Arkusze stylów CSS
|   |-- images/         # Statyczne obrazki (np. logo)
|   |-- uploads/        # Folder na pliki przesyłane przez użytkowników
|   |   |-- avatars/
|   |   |-- book_images/
|   |-- *.php           # Skrypty PHP i strony HTML generowane przez PHP
|-- schema.sql          # Schemat bazy danych
|-- README.md           # Ten plik

## Instalacja i Uruchomienie (Lokalnie):

1.  Sklonuj repozytorium: `git clone [URL_REPOZYTORIUM]`
2.  Zaimportuj plik `schema.sql` do swojej bazy danych MySQL/MariaDB (np. o nazwie `gielda_ksiazek_db`).
3.  Skonfiguruj połączenie z bazą danych w pliku `config/db.php`, podając swój host, nazwę użytkownika, hasło i nazwę bazy danych.
4.  Upewnij się, że foldery `public/uploads/avatars/` oraz `public/uploads/book_images/` istnieją i są zapisywalne dla serwera WWW.
5.  Umieść domyślne obrazki:
    * `public/uploads/avatars/default_avatar.png`
    * `public/uploads/book_images/placeholder.png`
6.  Skieruj swój lokalny serwer WWW (np. Apache w XAMPP) na folder `public/` jako document root lub otwórz projekt w przeglądarce przez `http://localhost/ścieżka_do_projektu/public/`.


---
