Компании хранятся в папках, у каждой кампании своя папка. Имя кампании = имя папки. Хранятся они в директории /data/campanies относительно корня проекта.

Структура кампании:
+ trunks.list - Список транков кампании. Каждый с новой с строки.
+ call_file.tpl - Шаблон call файла Asterisk. Имеет 2 переменные: \_\_number\_\_ - подставляет номер телефона для обзвона, \_\_trunk\_\_ - подставляет транк.
+ number.list - Список телефонов для обзвона. Каждый номер с новой строки.
+ finished.list - Список номеров по которым произведен обзвон. Каждый номер с новой стройки.
+ Папка logs - Логи запуска кампании.

```shell
USAGE:
   autocall <OPTIONS> <COMMAND> ...

   Скрипт автообзвона для Asterisk от Asko.Host


OPTIONS:
   -w <string>, --wait <string>       Пауза между звонками в рамках транка кампании, в секундах

   -q <count>, --queue_size <count>   Максимальное количество звонков в процессе.

   -c <count>, --channels <count>     Кол-во одновременных каналов транка.

   -d <1|0>, --is_debug <1|0>         Режим отладки.

   -h, --help                         Display this help screen and exit immediately.

   --no-colors                        Do not use any colors in output. Useful when piping output to other tools or
                                      files.

   --loglevel <level>                 Minimum level of messages to display. Default is info. Valid levels are: debug,
                                      info, notice, success, warning, error, critical, alert, emergency.


COMMANDS:
   This tool accepts a command as first parameter as outlined below:


   run

     Запустить обзвон


   list

     Список компаний
```