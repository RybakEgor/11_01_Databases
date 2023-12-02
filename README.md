# Домашнее задание к занятию «Базы данных, их типы» - `Рыбак Егор`

---

### Задание 1. СУБД

### Кейс
Крупная строительная компания, которая также занимается проектированием и девелопментом, решила создать 
правильную архитектуру для работы с данными. Ниже представлены задачи, которые необходимо решить для
каждой предметной области. 

Какие типы СУБД, на ваш взгляд, лучше всего подойдут для решения этих задач и почему? 
 
1.1. Бюджетирование проектов с дальнейшим формированием финансовых аналитических отчётов и прогнозирования рисков.
СУБД должна гарантировать целостность и чёткую структуру данных.

1.1.* Хеширование стало занимать длительно время, какое API можно использовать для ускорения работы? 

1.2. Под каждый девелоперский проект создаётся отдельный лендинг, и все данные по лидам стекаются в CRM к 
маркетологам и менеджерам по продажам. Какой тип СУБД лучше использовать для лендингов и для CRM? 
СУБД должны быть гибкими и быстрыми.

1.2.* Можно ли эту задачу закрыть одной СУБД? И если да, то какой именно СУБД и какой реализацией?

1.3. Отдел контроля качества решил создать базу по корпоративным нормам и правилам, обучающему материалу 
и так далее, сформированную согласно структуре компании. СУБД должна иметь простую и понятную структуру.

1.3.* Можно ли под эту задачу использовать уже существующую СУБД из задач выше и если да, то как лучше это 
реализовать?

1.4. Департамент логистики нуждается в решении задач по быстрому формированию маршрутов доставки материалов 
по объектам и распределению курьеров по маршрутам с доставкой документов. СУБД должна уметь быстро работать
со связями.

1.4.* Можно ли к этой СУБД подключить отдел закупок или для них лучше сформировать свою СУБД в связке с СУБД 
логистов?

1.5.* Можно ли все перечисленные выше задачи решить, используя одну СУБД? Если да, то какую именно?

*Приведите ответ в свободной форме.*

---
### Ответ:

1.1
Для данной задачи можно рассмотреть использование реляционных СУБД. Формированием финансовых аналитических отчётов будет происходить с помощью SQL запросов. Данные в табличной форме позволят соблюдать структуру, следить за целостностью и связностью данных. Прогнозирование рисков будет выполняться на основе анализа накопленных данных. Из основных популярных реляционных СУБД можно предложить следующие:PostgreSQL , MySQL.
1.2
Для создания лендингов и CRM, которые должны быть гибкими и быстрыми, рекомендуется использовать тип СУБД, который обеспечивает высокую производительность и адаптируемость к различным бизнес-требованиям. Один из таких типов - это использование NoSQL баз данных, таких как MongoDB или Apache Cassandra
1.3
Реляционные СУБД обеспечат надежное хранение данных и возможность организации информации в соответствии с иерархией структуры компании.
Кроме того, для обеспечения простоты и понятности структуры базы данных, следует тщательно спроектировать её схему, определив необходимые таблицы, поля и связи между ними. Для этого можно использовать методологию нормализации данных, которая поможет избежать избыточности и неоднозначности информации.
1.4
Реляционные СУБД, например PostgreSQL, по нескольким причинам: Она поддерживает стандарты SQL и предоставляют возможность выполнения сложных запросов и операций, таких как присоединение таблиц и агрегация данных. Проектируется, учитывая отношения между таблицами и имеет индексы для ускорения запросов, что увеличивает производительность работы со связями. А также поддерживает обработку пространственных данных.

---

### Задание 2. Транзакции

2.1. Пользователь пополняет баланс счёта телефона, распишите пошагово, какие действия должны произойти для того, чтобы 
транзакция завершилась успешно. Ориентируйтесь на шесть действий.

2.1.* Какие действия должны произойти, если пополнение счёта телефона происходило бы через автоплатёж?

*Приведите ответ в свободной форме.*

---
### Ответ:
2.1.
1. Идентификация пользователя. например, ввод логина-пароля в личном кабинете
2. Выбор способа оплаты
3. Ввод суммы пополнения
4. Подтверждение транзакции
5. Обработка платежа сестиемой - проверка наличия средств, зачисление на счёт
6. Отображение результата - результат транзакции

---

### Задание 3. SQL vs NoSQL

3.1. Напишите пять преимуществ SQL-систем по отношению к NoSQL. 

3.1.* Какие, на ваш взгляд, преимущества у NewSQL систем перед SQL и NoSQL.

*Приведите ответ в свободной форме.*

---
### Ответ:
1. Структурированные данные: SQL-системы хорошо подходят для структурированных данных, таких как данные, хранящиеся в таблицах с жестко определенными схемами. Это обеспечивает более строгий контроль над данными и их целостностью.
2. Поддержка сложных запросов: SQL-системы обеспечивают богатый набор операций для выполнения сложных запросов, включая объединения, вложенные запросы и агрегирование данных. Это делает SQL-системы более подходящими для аналитики и отчетности.
3. Транзакционная поддержка: SQL-системы поддерживают ACID-транзакции, что обеспечивает надежность и целостность данных при выполнении операций в базе данных.
4. Моделирование данных: SQL-системы являются хорошим выбором для приложений с большим количеством сущностей и взаимосвязей, поскольку они предоставляют структурированный способ моделирования и запроса данных.
5. Уровень безопасности: SQL-системы, как правило, имеют более высокий уровень безопасности, позволяют легко установить ограничения на доступ к данным для разных пользователей, а также применять различные аутентификационные механизмы.
---

### Задание 4. Кластеры

Необходимо производить большое количество вычислений при работе с огромным количеством данных, под эту задачу 
выделено 1000 машин. 

На основе какого критерия будете выбирать тип СУБД и какая модель *распределённых вычислений* 
здесь справится лучше всего и почему?

*Приведите ответ в свободной форме.*

---
### Ответ:
Для выбора подходящего типа СУБД и модели распределенных вычислений, следует учитывать следующие критерии:
- Тип решаемых задач: Необходимо определить, являются ли задачи обработки данных сложными или реляционными, и выбирайте соответствующий тип СУБД
- Типы обрабатываемых данных: Необходимо выбрать тип, который поддерживает необходимый формат данных
- Перспективы роста и масштабирования: Необходимо учитывать возможности масштабирования и роста данных в будущем, выбирая СУБД, который может адаптироваться к изменениям и увеличению объема данных
- Отказоустойчивость: СУБД должна иметь механизмы обеспечения безопасности данных и восстановления после сбоев.
- Распределенность: СУБД должна позволять распределять данные и запросы на выполнение между несколькими серверами для увеличения пропускной способности и ускорения обработки.

Для интенсивных вычислений и крупномасштабных приложений для анализа данных было реализовано множество системных архитектур, включая параллельные и распределенные системы управления реляционными базами данных, такие как: 
- MapReduce
- Apache Hadoop
- HPCC
---


