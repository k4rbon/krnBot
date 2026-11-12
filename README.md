<h1 align="center">krnBot</h1>

<p align="center">
  Bot Discord do prowadzenia serwera społeczności: tickety, moderacja, whitelista i blacklista,<br>
  z własnym panelem www do konfiguracji i podglądu historii.<br>
  Projekt i wykonanie: <b>krngg.dev</b>
</p>

<p align="center">
  <img src="screenshots/krnbot-01-serwer.png" width="860" alt="Panel krnBot: role i kanały serwera">
</p>

---

## O projekcie

krnBot przejmuje codzienną pracę administracji serwera Discord. Zgłoszenia trafiają do ticketów, kary są nakładane jedną komendą i zapisywane w historii, a nowi gracze przechodzą przez whitelistę z limitem podejść. Całą konfigurację ustawia się w przeglądarce, bez edytowania plików i bez restartu bota.

> Zrzuty ekranu pokazują tryb demonstracyjny ze zmyślonymi danymi. Kod źródłowy nie jest publiczny.

## Panel www

Panel działa obok bota i odświeża się na żywo, kiedy na serwerze coś się zmieni.

- **Serwer:** przypisanie ról zespołu (Support, Sprawdzający, Moderator, Admin) i ról nadawanych przez bota, z podglądem, kto je ma
- **Whitelista:** decyzje „zdana / niezdana”, limit podejść, odstęp między nimi i treść wiadomości do gracza
- **Tickety:** kategorie, zespoły odpowiedzialne za każdą z nich i pytania w formularzu
- **Historia:** kary, wyniki whitelisty, blacklista i transkrypty zamkniętych ticketów, z wyszukiwarką

<p>
  <img src="screenshots/krnbot-02-whitelista.png" width="420" alt="Whitelista">
  <img src="screenshots/krnbot-03-tickety.png" width="420" alt="Tickety">
</p>
<p>
  <img src="screenshots/krnbot-04-historia.png" width="420" alt="Historia whitelisty">
</p>

## Funkcje na Discordzie

**Tickety**
- Panel z przyciskami i formularzem dla każdej kategorii
- Przejmowanie ticketu, dodawanie i usuwanie osób
- Automatyczne zamykanie nieaktywnych zgłoszeń
- Transkrypt rozmowy zapisany po zamknięciu

**Moderacja**
- `/ban`, `/kick`, `/timeout`, `/mute` z czasem i powodem
- Ostrzeżenia `/warn` z numerami spraw i możliwością cofnięcia
- `/clear`, `/slowmode`, `/lock` i `/unlock` do porządku na kanałach
- Pełna historia spraw każdego gracza

**Whitelista i blacklista**
- Oznaczanie wyniku komendą albo w panelu, a bot sam nadaje role i wysyła wiadomość
- Historia podejść i cofanie decyzji
- Blacklista czasowa albo stała, z automatyczną rolą blokady

**Informacje**
- `/userinfo`, `/serverinfo`, `/ping`, `/pomoc`

## Technologie

| Część | Stos |
| --- | --- |
| Bot | Java 21, JDA (komendy slash, przyciski, formularze) |
| Panel www | Javalin, HTML/CSS/JS, aktualizacje na żywo przez SSE |
| Dane | SQLite |
| Bezpieczeństwo | Logowanie tokenem panelu, komunikacja bota i panelu podpisana kluczem API |

---

<h3 align="center">Potrzebujesz podobnego bota dla swojej społeczności?</h3>

<p align="center">
  Projektuję i buduję boty Discord oraz aplikacje mobilne i webowe dopasowane do Twoich potrzeb.<br>
  Napisz, czego potrzebujesz, a odezwę się z propozycją.
</p>

<p align="center">
  <a href="https://krngg.dev"><b>krngg.dev · kontakt →</b></a>
</p>

<p align="center"><sub>© krngg.dev. Wszelkie prawa zastrzeżone.</sub></p>
