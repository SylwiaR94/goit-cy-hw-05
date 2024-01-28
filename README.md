**Ograniczenia systemu**
Checks:
fail: http.request_rate >= 2 and http.response_time.max < 600
fail: vusers.failed == 0
fail: http.response_time.p95 < 1000

1. Czas najwolniejszego żądania wynosi więcej niż 600 milisekund.
2. 720 użytkowników zakończyło swój scenariusz niepowodzeniem, więc warunek "vusers.failed == 0" zwrócił fail.
3. Mniej niż 95% użytkowników dostało odpowiedź na żądanie w ciągu mniej niż 1 sekundy.
