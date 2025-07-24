# Z80 PC - Komputer 8-bitowy i moje plany

## Wymagania
- RAM: Najlepiej 32KB
- EEPROM: 32KB, nie więcej
- ROM: Najlepiej 16MB, 4MB to dosłowne minimum (system plików [SimpleFS](https://github.com/na-razie-bez-nicku/SimpleFS) wymaga)
- Będzie BIOS, który załaduje system operacyjny z dysku (pamięci Flash)
- Na początku będzie tylko procesor i RAM z terminalem przez USB. Nie będzie żadnej pamięci EEPROM, tylko będzie Arduino Uno, które przez konwerter UART (w uproszczeniu przez USB) będzie ładował program do RAMu.

## Działanie z Arduino jako Loader programu
1. Arduino się włącza i czeka na program
2. Komputer (nie 8-bitowy) przez USB przesyła program do Arduino
3. Arduino zapisuje program do RAMu
4. Arduino odłącza się od RAMu, procesor się podłącza
5. Arduino resetuje procesor
6. Procesor wykonuje program

## Znane komponenty
- CPU: Z84C0006PEC
- RAM: Toshiba TC55257APL-10 32KB
