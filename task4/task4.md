# Домашка

1. [Описание-языка](#Описание-языка)
1. [пример1](#пример1)
1. [пример2](#пример2)
1. [пример3](#пример3)

## Описание-языка
Автомат описывается так: сначала 3 числа (мощность алфавита, количество состояний, количество переходов). Алфавит -- множество строк, записанных через пробел. Он записывается во второй строке (ровно столько строк, какова мощность алфавита). Потом для каждого состояния от `1` до `n` (где `n` -- их количество) в отдельной строке записывается номер состояния и является ли оно терминальным (`term/notterm`). Каждый номер от `1` до `n` должен встречаться ровно 1 раз. Потом в `m` строках описываются переходы, где каждый переход это два числа -- номер состояния откуда идет переход, номер состояния куда идет переход и еще элемент алфавита через пробел. По переходу на строку.

## пример1
```
2 3 4
0 1
1 term
2 term
3 notterm
1 2 0
2 1 1
1 3 1
2 3 0
```

Автомат принимающий множество строк вида `0`, `01`, `010`, `0101`, `01010`,.... (пустую в том числе).

## пример2
```
2 2 4
aa bb
2 notterm
1 term
1 1 aa
1 2 bb
2 2 aa
2 2 bb
```

Автомат принимающий только строки состоящие из `aa`.

## пример3
```
1 2 2
u
1 notterm
2 term
1 2 u
2 2 u
```
Автомат который принимает все непустые строки.
