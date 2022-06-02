# This is my Git Tutorial
![Logo_Git](/Git-logo.svg "Логотип Git")
>**Git**
\- это бесплатная распределенная система управления версиями с открытым исходным кодом, предназначенная для быстрого и эффективного управления любыми проектами, от небольших до очень крупных.
***
## *Список команд для работы с Git:*

* [git init](#git-init)

* [git status](#git-status)

* [git add](#git-add)

* [git commit -m](#git-commit---m)

* [git log](#git-log)

* [git checkout](#git-checkout)

* [git checkout master](#git-checkout-master)

* [git diff](#git-diff)

* [git version](#git-version)

***
### ***git init***

\- преобразует текущий каталог в репозиторий Git. Создает подкаталог .git в текущем каталоге и позволяет начать регистрацию версий проекта. Большинство остальных команд Git невозможно использовать без инициализации репозитория, поэтому данная команда обычно выполняется первой в рамках нового проекта

***

### ***git status***

\- выводит список проиндексированных и неотслеживаемых файлов, а также файлов, удаленных из индекса Git.

***

### ***git add***

\- добавляет изменение из рабочего каталога в раздел проиндексированных файлов. Cообщает Git, что вы хотите включить изменения в конкретном файле в следующий коммит. Однако изменения регистрируются в нем только после выполнения команды git commit.

***

### ***git commit - m***

\- делает для проекта снимок текущего состояния изменений, добавленных в раздел проиндексированных файлов и создает комментарий. Перед выполнением необходимо использовать команду git add, чтобы добавить в проект изменения, которые будут сохранены в коммите.

***

### ***git log***

\- выводит полную историю коммитов в стандартном формате. Если выходные данные занимают более одного экрана, можно выполнить прокрутку с помощью клавиши Пробел или нажать q для выхода.

***

### ***git checkout***

\- позволяет вернутся к любому ранее сохраненному комиту. Вы можете просматривать файлы, компилировать проект, запускать тесты и даже редактировать файлы, не боясь потерять текущее состояние проекта. Никакие внесенные здесь изменения не будут сохранены в репозитории.

***

### ***git checkout master***

\- позволяет вернуться к актуальной версии файла после просмотра предыдущих комитов.

***

### ***git diff***

\- сравнивает записаную версию файла с последним коммитом. Если изменения внесены, но файл не сохранен - команда ничего не покажет.

***

### ***git version***

\- показывает версию Git установленную на компьютере

***

## *Перечень возможностей Git:*

* [cоздание новой ветки и переходов между ними](#создание-новой-ветки-и-переходов-между-ними)
* [cлияние веток](#слияние-веток)
* [конфликты при слиянии, их разрешение](#конфликты-при-слиянии-их-разрешение)
* [удаление ветки](#удаление-ветки)
* [замена последнего комментария в комите](#замена-последнего-комментария-в-комите)
* [исключение из отслеживания файла](#исключение-из-отслеживания-файла)
* [создание файла исключений](#создание-файла-исключений)
* [копирование удаленного репозитория](#копирование-удаленного-репозитория)
* [отправка изменений в удаленный репозиторий]()
* [получение последней версии удаленного репозитория]()

***
### *__Создание новой ветки и переходов между ними__*
1. Для создания новой ветки используется команда *git branch branch name*, где *branch_name* название создаваемой ветки.
2. Для перехода между ветками используется команда *git checkout branch _name*, где *branch_name* название целевой ветки.
***

### *__Слияние веток__*

1. Для осуществления слияния используется команда *git merge branch_name*, где *branch_name* - название, сливаемой с текущей веткой.
***

### *__Конфликты при слиянии, их разрешение__*
1. Конфликты при слиянии возникают при наличии противоречащих коммитов в сливаемых ветках.
***

### *__Удаление ветки__*
1. Перед удалением ветки убедитесь, что информация перенесена в другую ветку или уже не нужна.
2. Перейдите на ветку *master* с помощью команды *git checkout master* 
3. Для удаления введите *git branch -d branch_name*, где *branch_name* имя удаляемой ветки.
***

### *__Замена последнего комментария в комите__*
1. Исправить комментарий можно только в последнем комите
2. Для этого введите команду *git commit --amend -m "message"*, где *"message"* правильное описание комита.
***

### *__Исключение из отслеживания файла__*

Иногда в репозитории отслеживаются файлы, изменение которых бессмысленно отслеживать. Например изображения. Для того чтобы Git перестал отслеживать их и не выдавал предупреждений, необходимо сделать следующее:
1. Ввести команду *git rm --cached file_name*, где *file_name* имя файла исключаемого из кеширования
2. Записать в файл игнорирования *.gitignore* имя файла, исключенного из кеширования *file_name*.
3. Сохранить изменения.  
***

### *__Создание файла исключений__*

Изменения некоторых файлов бессмысленно отслеживать, но которые необходимы в работе проекта. Например изображения. Для того чтобы git не выдавал предупреждений, необходимо:
1. Создайте файл *.gitignore*
2. Внесите имя файла, который не будет отслеживаться
3. Сохраните изменения в файле с помощью клавиш *Ctrl + S*
4. С помощью команды *git add .gitignore* ссобщите Git, что вы хотите внести этот файл в следующий комит
5. Добавьте комит командой *git commit -m "commit_name"*, где *"commit_name"* комментарий к комиту.
***

### *__Копирование удаленного репозитория__*

Репозиторий, расположенный в аккаунте Github, можно скопировать для локальной работы следующим образом:
1. В аккаунте Github скопировать адрес репозитория
2. В терминале Visual Studio ввести команду git clone repo_url, где repo_url адрес репозитория

Результатом будет папка с файлами репозитория на вашем компьютере
***

## *Итоги семинара:*

За время семинара я узнал о Git и Markdown и немного научился с ними работать:)
***
*Этот файл был создан с помощью языка разметки Markdown. Если интересно, более подробно с ним можно ознакомиться*
[*здесь*](https://gist.github.com/Jekins/2bf2d0638163f1294637)