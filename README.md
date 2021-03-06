# SynergyPayanyway

## Установка

Для настройки системы перейдите по [адресу](https://www.moneta.ru/unitManagement.htm?_do_viewAccounts=true) в раздел **Редактировать счет** соответствующего счета.

Заполните Pay URL, Success URL и Fail URL значениями https://[domain]/gateway/payanyway/result, https://[domain]/gateway/payanyway/success, https://[domain]/gateway/payanyway/fail соответственно, подставив вместо [domain] адрес вашего магазина.

Обязательные параметры метода оплаты:

* *Id*

Идентификатор магазина в системе MONETA.RU. Соответствует номеру расширенного счета магазина.

* *Currency Code*

ISO код валюты, в которой производится оплата заказа в магазине. Значение должно соответствовать коду валюты счета получателя (MNT_ID).

Необязательные параметры метода оплаты:

* *Signature*

Код для идентификации отправителя и проверки целостности данных. Если в запросе есть данный параметр, то MONETA.RU сгенерирует собственный код на основе параметров запроса и сравнит его с данным параметром. Если параметр «MNT_SIGNATURE» и код сгенерированный MONETA.RU не совпадут, то MONETA.Assistant завершится с ошибкой. Является обязательным, если в настройках счета выставлен флаг «Подпись формы оплаты обязательна».

* *Locale*

(ru|en) Язык пользовательского интерфейса.

* *Payment System*

(1015 – МОНЕТА.РУ, 1020 – Яндекс.Деньги, 1017 – WebMoney и т.п.) Предварительный выбор платежной системы. Список доступных способов оплаты для заданного счета можно посмотреть на странице «Рабочий кабинет / Способы оплаты» ([https://www.moneta.ru/viewPaymentMethods.htm](https://www.moneta.ru/viewPaymentMethods.htm))

* *Payment System List*

Список (разделенный запятыми) идентификаторов платежных систем, которые необходимо показывать пользователю в MONETA.Assistant. Например, «1015,1017» - пользователю в MONETA.Assistant будут показаны только платежные системы МОНЕТА.РУ и WebMoney.
