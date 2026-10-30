# AI Tennis Coach — MVP 0.1

## Uruchomienie
1. Rozpakuj archiwum.
2. Uruchom lokalny serwer HTTP w tym katalogu, np. `python -m http.server 8000`.
3. Otwórz `http://localhost:8000` w Chrome/Safari.
4. Na iPhonie możesz dodać stronę do ekranu początkowego (Safari → Udostępnij → Do ekranu początkowego). Aby użyć na iPhonie przez sieć lokalną, serwer musi być dostępny w LAN; dla instalacji PWA i dostępu do kamery/pliku zalecany jest HTTPS.

## Funkcje
- import wideo z urządzenia i odtwarzanie z osią czasu
- wykrywanie 33 punktów ciała przez MediaPipe Pose Landmarker (2D)
- nakładka szkieletu
- orientacyjne kąty łokcia, barku, biodra i kolana
- ręczne oznaczanie typów uderzeń i notatek
- podsumowanie sesji oraz eksport oznaczonych uderzeń do CSV
- podstawowa obsługa PWA / cache plików aplikacji

## Ograniczenia MVP
- AI analizuje pojedynczą sylwetkę 2D; nie jest to rekonstrukcja 3D ani certyfikowana analiza biomechaniczna.
- „Śledź ruch” analizuje próbki klatek w czasie rzeczywistym odtwarzania. Wydajność zależy od urządzenia i przeglądarki.
- Nie ma jeszcze automatycznego rozpoznawania uderzeń, detekcji kontaktu z piłką, trackingu piłki, prędkości ani RPM.
- Pierwsze uruchomienie wymaga internetu do pobrania MediaPipe i modelu. Nagranie pozostaje lokalnie w przeglądarce.

## Następny etap
1. Automatyczne wykrywanie faz uderzenia (preparation / acceleration / contact / follow-through).
2. Klasyfikacja forehand / backhand / serve.
3. Detekcja piłki i kalibracja geometrii kortu.
4. Historia treningów, porównania i raporty.
5. Backend opcjonalny do synchronizacji między iPhonem i komputerem.
