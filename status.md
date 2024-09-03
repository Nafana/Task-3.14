[< назад](./teams.md)
## **git status**
Команда `git status` отображает состояние рабочего каталога и раздела проиндексированных файлов. С ее помощью можно проверить индексацию изменений и увидеть файлы, которые не отслеживаются Git. Информация об истории коммитов проекта не отображается при выводе данных о состоянии.
<u>**Использование:**</u>

git status
Выводит список проиндексированных и неотслеживаемых файлов, а также файлов, удаленных из индекса Git.

<u>**Пояснения:**</u>

Команда `git statu`s относительно проста в использовании. Она показывает, какие изменения были внесены с помощью команд `git add` и `git commit`. Сообщения о состоянии также содержат инструкции по индексированию файлов либо отмене этой операции. В примере выходных данных ниже показаны три основные категории вызова `git status`:
```
# On branch main
# Changes to be committed:
# (use "git reset HEAD <file>..." to unstage)
#
#modified: hello.py
#
# Changes not staged for commit:
# (use "git add <file>..." to update what will be committed)
# (use "git checkout -- <file>..." to discard changes in working directory)
#
#modified: main.py
#
# Untracked files:
# (use "git add <file>..." to include in what will be committed)
#
#hello.pyc
```
<u>**Пример:**</u>

Перед отправкой изменений рекомендуется проверить состояние репозитория. Так вы сможете убедиться, что коммит включает только нужные данные. В следующем примере показано состояние репозитория до и после индексирования и отправки снимка состояния:
```
# Edit hello.py
git status
# hello.py is listed under "Changes not staged for commit"
git add hello.py
git status
# hello.py is listed under "Changes to be committed"
git commit
git status
# nothing to commit (working directory clean)
```