# sql-13-sample-
лаба 13
оздать резервную копию базы данных контактов на первом компьютере.

Для этого можно использовать команду BACKUP DATABASE в SQL Server Management Studio (SSMS) или скрипт T-SQL. Например:

java

BACKUP DATABASE ContactsDB
TO DISK = 'C:\Backup\ContactsDB.bak'
Здесь "ContactsDB" - это имя базы данных, а "C:\Backup\ContactsDB.bak" - путь к файлу резервной копии.

Перенести файл резервной копии на другой компьютер.

Это можно сделать через сетевую папку, USB-накопитель или любой другой способ передачи файлов между компьютерами.

Восстановить базу данных на втором компьютере.

Для этого можно использовать команду RESTORE DATABASE в SSMS или скрипт T-SQL. Например:

sql
Copy code
RESTORE DATABASE ContactsDB
FROM DISK = 'C:\Backup\ContactsDB.bak'
WITH REPLACE, RECOVERY
Здесь "ContactsDB" - это имя базы данных, а "C:\Backup\ContactsDB.bak" - путь к файлу резервной копии. Флаги REPLACE и RECOVERY указывают, что нужно заменить существующую базу данных (если она существует) и восстановить ее в состояние готовности.
