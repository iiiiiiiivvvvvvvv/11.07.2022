# Инструкция по работе с GIT

## Что такое GIT?
GIT является самой популярной системой контроля Версий.

## Подготовка репозитория
Для создания репозитория используется команда *git init*.

## Создание коммитов
Создать коммит (commit) - значит зафиксировать изменения любых файлов, входящих в репозиторий. Любые файлы, созданные или измененные вами и для которых вы не выполнили git add после редактирования, не войдут в ваш коммит.

### Просмотр состояния репозитория
Для просмотра состояния репозитория используется команда *git status*.

 ### Добавление файла в коммит
 Для добавления файла в коммит используется команда *git add*. Для этого достаточно в терминале с папкой текущего репозитория написать *git add <название файла>*


 ### Сохранение коммита
 Для сохранения коммита используется команда *git commit*. Команда в терминале *git commit -m "<сообщение к коммиту>"*.

## Перемещения между коммитами
Чтобы перемещаться между коммитами  нужна команда *git checkout <название коммита>*.

## Журнал изменений
Для просмотра изменений используется команда *git log* 

## Удаление веток 
Удаление уже ненужных веток выполняют командой *git branch -d <название ветки>*

## Ветки в GIT
Для создания нового отвитвления (*ветки*) используется команда *git branch <название ветки>*. для перехода в ветку команда *git checkout <название ветки>*.

## Слияние веток и решение конфликтов 
 Слияние веток выполняется командой *git merge <название ветки>*. ветка не должна быть текущей.
 Команды Git, с помощью которых можно разрешить конфликты слияния
Общие инструменты
git status
Команда status часто используется во время работы с Git и помогает идентифицировать конфликтующие во время слияния файлы.
git log --merge
При передаче аргумента --merge для команды git log будет создан журнал со списком конфликтов коммитов между ветками, для которых выполняется слияние.
git diff
Команда diff помогает найти различия между состояниями репозитория/файлов. Она полезна для выявления и предупреждения конфликтов слияния.
Инструменты для случаев, когда Git прерывает работу в самом начале слияния
git checkout
Команда checkout может использоваться для отмены изменений в файлах или для изменения веток.
git reset --mixed
Команда reset может использоваться для отмены изменений в рабочем каталоге или в разделе проиндексированных файлов.

 Общий подход к разрешению конфликтов такой:
Непосредственно разрешить конфликт одним из двух рассмотренных немного ниже способов. Либо, если возникновение конфликта стало неожиданным для вас, можно выполнить git merge --abort. Эта команда прервет слияние и вернет все, как было.
Сообщить Git, что мы разрешили конфликт, добавив все файлы с разрешенными конфликтами в индекс. Сделать это можно уже знакомой командой git add <конфликтный файл> для каждого конфликтного файла.
Продолжить слияние, выполнив git merge --continue. Либо вручную создать merge-коммит уже знакомой командой git commit.

Выше мы уже сказали, что существует два способа разрешать конфликты, вот они:
Первый способ. Разрешить конфликт вручную. Тогда мы можем самостоятельно изменить конфликтные файлы, сделав их такими, какими мы хотим их видеть.
Второй способ. Просто выбрать один из двух файлов.

## Удаление веток
Удаление веток выполняется командой *git branch -d <название ветки>*.
