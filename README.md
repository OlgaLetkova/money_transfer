# Отчёт о тестировании приложения "Money Transfer"

## Краткое описание

26.08.2020 было проведено тестирование приложения "Money Transfer". На тестирование затрачено 2ч.

В результате тестирования выяснилось, что при пополнении счета клиента его баланс становится отрицательным.
 
## Описание тестов

Было проведено функциональное тестирование приложения "Money Transfer", которое используется для пополнения банковского счета. В результате тестирования необходимо было выяснить, что происходит со счетом клиента при пополнении его на 500_000_000.

Тестовые данные:
* текущий баланс счёта клиента - переменная типа `int`, значение - 2_000_000_000 (два миллиарда рублей)*
* сумма перевода - переменная типа `int`, значение - 500_000_000 (пятьсот миллионов рублей)
* переменная для хранения итогового значения - тип `int`

## Результаты

По итогам тестирования мы получили, что при пополнении баланса счета клиента на 500_000_000 баланс счета становится отрицательным.
В результате проведенного анализа можно сделать вывод, что для переменной для хранения итогового значения неправильно выбран тип целочисленного числа. При пополнении счета баланс становится таким, что выходит за границы типа int.
 
 Ссылка на баг-репорт: https://github.com/OlgaLetkova/money_transfer/issues/1

## Общие рекомендации

Рекомендуется смена целочисленного типа для переменной итогового значения с int на long. 