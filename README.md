# zapret-discord-youtube-vrchat

Сборка на основе [flowseal/zapret-discord-youtube](https://github.com/flowseal/zapret-discord-youtube).
Оригинальный проект: [bol-van/zapret](https://github.com/bol-van/zapret).

## Изменения

- В `list-general` добавлены домены vrchat.
- Добавлен фильтр windivert для photon engine.
- Часть фейков заменена на сгенерированные из firefox.
- UDP порты 5055, 5056, 27001 и 27002 исключены из игрового фильтра.
- Во все `.bat` файлы добавлена стратегия:

```
--filter-udp=5055,5056,27001,27002 --dpi-desync=fake --dpi-desync-repeats=12 --dpi-desync-any-protocol=1 --dpi-desync-fake-unknown-udp="%BIN%quic_initial_quic_egress_yandex_net_no_kyber_ff.bin" --dpi-desync-cutoff=n4
```

## Исполняемые файлы

Файлы `WinDivert.dll`, `WinDivert64.sys` и `winws.exe` заменены на файлы из релиза [zapret v72.13](https://github.com/bol-van/zapret/releases/tag/v72.13).

Проверить идентичность файлов:

```
fc /b "путькфайлу1" "путькфайлу2"
```

Сравнить хэши:

```
certutil -hashfile "путькфайлу" SHA256
```
