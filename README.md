# os2
## Содержание
[Системная информация](#1)

[Остановка системы](#2)

[Файлы и директории](#3)

[Дисковое пространство](#4)

[Пользователи и группы](#5)

[Мониторинг и отладка](#6)

[Дополнительные команды](#7)

<a name="1"><h2>Системная информация</h2></a>
arch, uname -m
отобразить архитектуру компьютера

![image](https://user-images.githubusercontent.com/99398496/196217269-d0d5d271-5c0a-4a17-b9e2-55c41b872efc.png)

uname -r
отобразить используемую версию ядра

![image](https://user-images.githubusercontent.com/99398496/196217381-0392c2b7-0df6-4491-986f-5f9d8c874a39.png)

dmidecode -q
показать аппаратные системные компоненты - (SMBIOS / DMI)

![image](https://user-images.githubusercontent.com/99398496/196223797-648530d6-e0be-40a4-9bc4-5800b871ff29.png)

hdparm -i /dev/hda
вывести характеристики жесткого диска

![image](https://user-images.githubusercontent.com/99398496/196224489-ed69b5c2-aa43-41c2-8160-6b43bce485d8.png)

hdparm -tT /dev/sda
протестировать производительность чтения данных с жесткого диска

![image](https://user-images.githubusercontent.com/99398496/196224695-99bd6f81-1228-4479-bda6-30ce21c302da.png)

cat /proc/cpuinfo
отобразить информацию о процессоре

![image](https://user-images.githubusercontent.com/99398496/196225160-c0518447-2a26-4a76-86a3-8766e071702e.png)

cat /proc/interrupts
показать прерывания

![image](https://user-images.githubusercontent.com/99398496/196225314-6d4f0a7a-cf69-4292-b4c9-43c8d154dd38.png)

cat /proc/meminfo
проверить использование памяти

![image](https://user-images.githubusercontent.com/99398496/196225785-afda5512-1e89-48ed-8ef0-fccb007dad94.png)

cat /proc/swaps
показать файл(ы) подкачки

![image](https://user-images.githubusercontent.com/99398496/196225904-8c056284-7b5a-4980-801b-ca42d6ef8fb3.png)

cat /proc/version
вывести версию ядра

![image](https://user-images.githubusercontent.com/99398496/196225994-5a16c801-664a-4124-9454-752943c683bd.png)

cat /proc/net/dev
показать сетевые интерфейсы и статистику по ним

![image](https://user-images.githubusercontent.com/99398496/196226108-eabdf299-08b7-4d8f-8163-c5f23066e3d1.png)

cat /proc/mounts
отобразить смонтированные файловые системы

![image](https://user-images.githubusercontent.com/99398496/196226214-0d741c5c-1e7a-4aef-8d50-f6c3fffce9a9.png)

lspci -tv
показать в виде дерева PCI устройства

![image](https://user-images.githubusercontent.com/99398496/196226913-f61499d6-5676-4f79-bd8b-285a2a462753.png)

lsusb -tv
показать в виде дерева USB устройства

![image](https://user-images.githubusercontent.com/99398496/196226978-247e1aca-30fe-4c51-91af-0891ab81e58c.png)

date
вывести системную дату

![image](https://user-images.githubusercontent.com/99398496/196235819-3f66c405-93ee-49b8-839a-02bda41f0290.png)

cal 2021
вывести таблицу-календарь 2021-го года

![image](https://user-images.githubusercontent.com/99398496/196235904-90c00812-457c-4133-84c3-c5111d9c60ef.png)

date 041217002020.00
установить системные дату и время ММДДЧЧммГГГГ.СС (МесяцДеньЧасМинутыГод.Секунды)

![image](https://user-images.githubusercontent.com/99398496/196237020-7c21ff27-0b5d-4b7d-9e71-946166f036f0.png)

clock -w
сохранить системное время в BIOS

![image](https://user-images.githubusercontent.com/99398496/196237147-bd33132f-00ae-4634-b4a8-093afb6189d0.png)

<a name="2"><h2>Остановка сисетмы</h2></a>
shutdown -h now, init 0, telinit 0
Остановить систему

shutdown -h hours:minutes &
запланировать остановку системы на указанное время

![image](https://user-images.githubusercontent.com/99398496/196237806-85f10a04-7597-4c60-8a75-c3a42e5e0100.png)

shutdown -c
отменить запланированную по расписанию остановку системы

![image](https://user-images.githubusercontent.com/99398496/196237888-fe0c0508-7992-46f5-9c8f-16d5b30de826.png)

shutdown -r now, reboot
перегрузить систему

logout
выйти из системы

![image](https://user-images.githubusercontent.com/99398496/196237969-131be252-ef43-447b-81e4-0fc72fd11506.png)

<a name="3"><h2>Файлы и директории</h2></a>
cd /home
перейти в директорию '/home'

![image](https://user-images.githubusercontent.com/99398496/196238029-8e209d18-98d9-4c3c-ae72-a299002cd709.png)

cd ..
перейти в директорию уровнем выше

![image](https://user-images.githubusercontent.com/99398496/196238067-c117f97a-9e21-4b11-8b2a-3f9bee4cd962.png)

cd ../..
перейти в директорию двумя уровнями выше

![image](https://user-images.githubusercontent.com/99398496/196238114-08fe61bb-b37a-4c3e-af58-3348249b00ad.png)

cd
перейти в домашнюю директорию

![image](https://user-images.githubusercontent.com/99398496/196238179-eb65a134-e7f1-4083-85c2-367898c2487a.png)

cd ~user
перейти в домашнюю директорию пользователя user

![image](https://user-images.githubusercontent.com/99398496/196238260-5f5f38f5-377d-48ff-b5c8-6812492b158c.png)

cd -
перейти в директорию, в которой находились до перехода в текущую директорию

![image](https://user-images.githubusercontent.com/99398496/196238342-3e931290-ebd7-4bc9-be5a-9fa0cd597b75.png)

pwd
показать текущую директорию

![image](https://user-images.githubusercontent.com/99398496/196238385-e40fd1b6-af4b-4494-98c6-8851a22867e5.png)

ls
отобразить содержимое текущей директории

![image](https://user-images.githubusercontent.com/99398496/196238431-d7ec90fa-477c-4e9d-b5de-787d85743e9b.png)

ls -F
отобразить содержимое текущей директории с добавлением к именам символов, храктеризующих тип

![image](https://user-images.githubusercontent.com/99398496/196238516-66aec5ce-a328-4588-954f-533df464bbcb.png)

ls -l
показать детализированое представление файлов и директорий в текущей директории

![image](https://user-images.githubusercontent.com/99398496/196238560-44fde2fe-5591-48b3-b201-0e5f2aaf2149.png)

ls -a
показать скрытые файлы и директории в текущей директории

![image](https://user-images.githubusercontent.com/99398496/196238611-5d84064f-05a6-4d2c-9ac4-36f35f1348c5.png)

tree, lstree
показать дерево файлов и директорий, начиная от корня (/)

![image](https://user-images.githubusercontent.com/99398496/196239939-140b5ffb-24fe-49ed-8c38-f4616081a90b.png)

mkdir dir1
создать директорию с именем 'dir1'

![image](https://user-images.githubusercontent.com/99398496/196240026-9a87cbb9-77a9-49e7-bf27-9a769334d070.png)

mkdir dir1 dir2
создать две директории одновременно

![image](https://user-images.githubusercontent.com/99398496/196240076-8ba6a127-d7eb-41ce-888e-225d63e4d40d.png)

mkdir -p /tmp/dir1/dir2
создать дерево директорий

![image](https://user-images.githubusercontent.com/99398496/196241118-bd85b76a-d099-4426-985e-d3c12cf4e9cc.png)

rm -f file1
удалить файл с именем 'file1'

![image](https://user-images.githubusercontent.com/99398496/196242140-ba4ae344-dd9c-44ef-95df-fa47aa9630b9.png)

rmdir dir1
удалить директорию с именем 'dir1'

![image](https://user-images.githubusercontent.com/99398496/196242219-6427b66e-87d0-464e-bfea-464a78681e54.png)

rm -rf dir1
удалить директорию с именем 'dir1' и рекурсивно всё её содержимое

rm -rf dir1 dir2
удалить две директории и рекурсивно их содержимое

![image](https://user-images.githubusercontent.com/99398496/196243924-66330568-0ece-4879-aebb-b976b7700c43.png)

mv dir1 new_dir
переименовать или переместить файл или директорию

![image](https://user-images.githubusercontent.com/99398496/196244054-40da9157-4ed2-4633-9bb3-e9b85c793f05.png)

cp file1 file2
сопировать файл file1 в файл file2

![image](https://user-images.githubusercontent.com/99398496/196244425-454a44e1-5bc2-4f0a-8357-9ec026699bdd.png)

cp dir/* .
копировать все файлы директории dir в текущую директорию

![image](https://user-images.githubusercontent.com/99398496/196246474-31bc39fc-51a6-4af9-8c07-fa0b462af828.png)

cp -a /tmp/dir1 .
копировать директорию dir1 со всем содержимым в текущую директорию

cp -a dir1 dir2
копировать директорию dir1 в директорию dir2

![image](https://user-images.githubusercontent.com/99398496/196246673-b47568d3-78c7-4f8b-8777-f6f03b543b19.png)

ln -s file1 lnk1
создать символическую ссылку на файл или директорию

![image](https://user-images.githubusercontent.com/99398496/196246920-cf8d3db6-bbc0-42f7-a42a-c7a843c29d25.png)

ln file1 lnk1
создать "жёсткую" (физическую) ссылку на файл или директорию

![image](https://user-images.githubusercontent.com/99398496/196247024-b7536094-7095-4a40-94ee-77894e27c2d9.png)

touch -t 2012250000 fileditest
модифицировать дату и время создания файла, при его отсутствии, создать файл с указанными датой и временем (YYMMDDhhmm)

![image](https://user-images.githubusercontent.com/99398496/196247684-3acb05e7-0d77-4773-8bd0-05a3b19224fa.png)

<a name="4"><h2>Дисковое пространство</h2></a>
df -h
отображает информацию о смонтированных разделах с отображением общего, доступного и используемого пространства (Прим.переводчика. ключ -h работает не во всех *nix системах)

![image](https://user-images.githubusercontent.com/99398496/196248467-1ec7bd73-2a05-485f-b585-764b96d7fc53.png)

ls -lSr |more
выдаёт список файлов и директорий рекурсивно с сортировкой по возрастанию размера и позволяет осуществлять постраничный просмотр

![image](https://user-images.githubusercontent.com/99398496/196248587-8ece110f-8e96-4015-b775-28740f60ce34.png)

du -sh dir1
подсчитывает и выводит размер, занимаемый директорией 'dir1' (Прим.переводчика. ключ -h работает не во всех *nix системах)

![image](https://user-images.githubusercontent.com/99398496/196248695-531b86e7-704f-4ff8-b609-d270ea13d1e3.png)

du -sk * | sort -rn
отображает размер и имена файлов и директорий, с соритровкой по размеру

![image](https://user-images.githubusercontent.com/99398496/196248806-429636ca-b43f-42c5-ad66-5f4f4305538e.png)

rpm -q -a --qf '%10{SIZE}\t%{NAME}\n' | sort -k1,1n
показывает размер используемого дискового пространства, занимаемое файлами rpm-пакета, с сортировкой по размеру (fedora, redhat и т.п.)

![image](https://user-images.githubusercontent.com/99398496/196249165-26223232-7f3a-4b01-862a-114815cff31a.png)

dpkg-query -W -f='${Installed-Size;10}\t${Package}\n' | sort -k1,1n
показывает размер используемого дискового пространства, занимаемое файлами deb-пакета, с сортировкой по размеру (ubuntu, debian т.п.)

![image](https://user-images.githubusercontent.com/99398496/196249440-f46c8d76-7442-4582-a5a0-f032ec767864.png)

<a name="5"><h2>Пользователи и группы</h2></a>
groupadd group_name
создать новую группу с именем group_name

groupdel group_name
удалить группу group_name

![image](https://user-images.githubusercontent.com/99398496/196249680-9fd4c7a1-5b51-4fb6-b11c-8a1b019278be.png)

groupmod -n new_group_name old_group_name
переименовать группу old_group_name в new_group_name

![image](https://user-images.githubusercontent.com/99398496/196250122-35f86695-d7cc-4368-a0bc-a65c06b17ba4.png)

useradd -c "Nome Cognome" -g admin -d /home/user1 -s /bin/bash user1
создать пользователя user1, назначить ему в качестве домашнего каталога /home/user1, в качестве shell'а /bin/bash, включить его в группу admin и добавить комментарий Nome Cognome

useradd user1
создать пользователя user1

![image](https://user-images.githubusercontent.com/99398496/196250605-9fd78f63-c9e7-43e7-a40b-2b56fb491fe5.png)

userdel -r user1
удалить пользователя user1 и его домашний каталог

![image](https://user-images.githubusercontent.com/99398496/196250685-e7772ecb-8042-4bdb-9f9d-131a52d8bebf.png)

usermod -c "User FTP" -g system -d /ftp/user1 -s /bin/nologin user1
изменить атрибуты пользователя

passwd
сменить пароль

passwd user1
сменить пароль пользователя user1 (только root)

chage -E 2005-12-31 user1
установить дату окончания действия учётной записи пользователя user1

pwck
проверить корректность системных файлов учётных записей. Проверяются файлы /etc/passwd и /etc/shadow

grpck
проверяет корректность системных файлов учётных записей. Проверяется файл/etc/group

newgrp [-] group_name
изменяет первичную группу текущего пользователя. Если указать "-", ситуация будет идентичной той, в которой пользователь вышил из системы и снова вошёл. Если не указывать группу, первичная группа будет назначена из /etc/passwd

<a name="6"><h2>Мониторинг и отладка</h2></a>
top
отобразить запущенные процессы, используемые ими ресурсы и другую полезную информацию (с автоматическим обновлением данных)

ps -eafw
отобразить запущенные процессы, используемые ими ресурсы и другую полезную информацию (единожды)

ps -e -o pid,args --forest
вывести PID'ы и процессы в виде дерева

pstree
отобразить дерево процессов

kill -9 98989, kill -KILL 98989
"убить" процесс с PID 98989 "на смерть" (без соблюдения целостности данных)

kill -TERM 98989
Корректно завершить процесс с PID 98989

kill -1 98989, kill -HUP 98989
заставить процесс с PID 98989 перепрочитать файл конфигурации

lsof -p 98989
отобразить список файлов, открытых процессом с PID 98989

lsof /home/user1
отобразить список открытых файлов из директории /home/user1

lsof -iTCP:59302
показать приложение, которое использует TCP-порт 59302 (не обязательно слушает)

strace -c ls > /dev/null
вывести список системных вызовов, созданных и полученных процессом ls

strace -f -e open ls > /dev/null
вывести вызовы бибилотек

watch -n1 'cat /proc/interrupts'
отображать прерывания в режиме реального времени

last reboot
отобразить историю перезагрузок системы

last user1
отобразить историю регистрации пользователя user1 в системе и время его нахождения в ней

lsmod
вывести загруженные модули ядра

free -m
показать состояние оперативной памяти в мегабайтах

smartctl -A /dev/hda
контроль состояния жёсткого диска /dev/hda через SMART

smartctl -i /dev/hda
проверить доступность SMART на жёстком диске /dev/hda

tail /var/log/dmesg
вывести десять последних записей из журнала загрузки ядра

tail /var/log/messages
вывести десять последних записей из системного журнала

<a name="7"><h2>Дополнительные команды</h2></a>
apropos …keyword
выводит список комманд, которые так или иначе относятся к ключевым словам. Полезно, когда вы знаете что делает программа, но не помните команду

man ping
вызов руководства по работе с программой, в данном случае, - ping

whatis …keyword
отображает описание действий указанной программы

gpg -c file1
шифрует файл file1 с помощью GNU Privacy Guard

gpg file1.gpg
дешифрует файл file1 с помощью GNU Privacy Guard

wget -r www.example.com
загружает рекурсивно содержимое сайта www.example.com

wget -c www.example.com/file.iso
загрузить файл www.example.com/file.iso с возможностью останова и продолжения в последствии

echo 'wget -c www.example.com/files.iso' | at 09:00
начать закачку в указанное время

ldd /usr/bin/ssh
вывести список библиотек, необходимых для работы ssh

alias hh='history'
назначить алиас hh команде history
