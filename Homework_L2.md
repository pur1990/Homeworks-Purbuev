# Инструкция по работе с Git и работе с удаленными репозиториями

## Что такое Git?
***Git*** - это одна из реализаций распределенной системы контроля версий, поддерживающие как локальные, так и удаленные репозитории. Самая популярная реализация Git - это [GitHub](https://github.com)
## Подготовка репозитория
Для создания репозитория используется команда *git init*. Для этого необходимо открыть в терминале папку с будущим репозиторием и там написать *git init*.

## Создание коммитов

### Выполнение коммита
Для того, чтобы выполнить коммит используется команда *git commit*. Для этого в терминале с папкой-репозиторием необходимо написать *git commit -m "<сообщение к коммиту>"*. Сообщение к коммиту писать ***ОБЯЗАТЕЛЬНО!!!***.

### Добавление файла к коммиту
Для добавления файла к коммиту используется команда *git add*. Для этого в терминале с папкой-репозиторием необходимо написать *git add <название файла>*.

## Журнал изменений
Для просмотра истории коммитов испольщуется команда *git log*. Для этого в терминале с папкой-репозиторием пишем *git log*. В показанном журнале обязательно будут:
* Хеш (номер) коммита
* Дата и время коммита
* Автор коммита
* Текст сообщения к коммиту

## Перемещение между коммитами
Для перемещения между коммитами используется команда *git checkout*. Для этого в терминале с папкой-репозиторием необходимо написать *git checkout <хеш коммита>*. Хеш коммита можно взять из истории коммитов, про которую было рассказано в предыдущем пункте.

## Ветки в Git
Ветка - это набор commit (кружок), которые идут друг за другом. У ветки есть название, основную ветку чаще всего называют master. Если говорить простыми словами, то ветка master - это наш проект.

Другие ветки - это отдельное место для реализации нового функционала или исправление багов (ошибок) нашего проекта. То есть, с отдельной веткой вы делаете что угодно, а затем сливаете эти изменения в основную ветку master.

### Просмотр списка веток
Для просмотра списка веток используется команда *git branch*. Для этого в терминале с папкой-репозиторем необхоимо написать *git branch* и Вы увидите список всех существующих веток. Зеленым цветом и символом **звездочка** будет обозначена текущая актуальная ветка.

### Перемещение между ветками
Для перемещения между ветками используется команда *git checkout*. Для этого в терминале с папкой-репозиторием необходимо написать *git branch <название ветки>*. *ВЕТКА ОБЯЗАТЕЛЬНО ДОЛЖНА СУЩЕСТВОВАТЬ!*

### Создание веток
Для того, чтобы создать новую ветку вводим *git branch <название_ветки>* или *git checkout -b <название_ветки>*. Переключаться между ветками можно такой командой *git checkout <название_ветки>*. Названия веток должны быть уникальными.

## Слияние веток и разрешение конфликтов
После того, как вы завершили работу над своей задачей, ветку можно слить в master . Для этого нужно переключиться в ветку master и выполнить следующую команду *git checkout master*. Для слияния необходимо ввести команду *git merge <название_ветки>*. Команда *merge* берет все изменения из ветки *<название_ветки>* и добавляет их в ветку *master*. Для того чтобы посмотреть текущее состояние ветки, например, какие файлы добавлены или не добавлены для создания commit, можно выполнить команду *git status*.

## Удаление веток
Для того, чтобы удалить ветку, необходимо для начала убедиться, что все слияния были проведены и все конфликты были разрешены. Переключитесь на ветку *master* и введите команду *git branch -d <название_ветки>*. Вы можете убедиться в успешном удалении ветки, введя команду *git branch*.

## Графическое отображение ветвления
Для того, чтобы увидеть графическое отображение всех веток, необходимо ввести в терминале команду *git log --graph*.
