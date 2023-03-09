# Получение сведений о системе

## Цель работы

Получить сведения об используемой системе

## Исходные данные

1. Ноутбук DELL

2. Ubuntu 22.04 LTS, запущенная через Hyper-V

3. Интерпретатор командной оболочки 5.1.16(1)-release


## План

1. Выполнение команд в терминале операционной системы

2. Анализ данных

## Ход работы


1. Затем получим сведения о версии ядра:

```bash
root@lime-Virtual-Machine:/home/lime# uname -a
Linux lime-Virtual-Machine 5.15.0-27-generic #28-Ubuntu SMP Thu Apr 14 04:55:28 UTC 2022 x86_64 x86_64 x86_64 GNU/Linux
```

В результате выполнения данной команды была получена версия ядра - 5.15.0-27-generic, дата компиляции ядра - 14 апреля 2022 года.

2. Далее можно получить сведения о процессоре:

```bash
ragim@LAPTOP-6RGQFHF2:~$ cat /proc/cpuinfo | grep "model name"
root@lime-Virtual-Machine:/home/lime# cat /proc/cpuinfo | grep "model name"
model name	: 11th Gen Intel(R) Core(TM) i3-1125G4 @ 2.00GHz
model name	: 11th Gen Intel(R) Core(TM) i3-1125G4 @ 2.00GHz
model name	: 11th Gen Intel(R) Core(TM) i3-1125G4 @ 2.00GHz
model name	: 11th Gen Intel(R) Core(TM) i3-1125G4 @ 2.00GHz
```

Команда верно вывела результат, что в системе используются четыре выделенных ядра

3. Далее получим последние 30 строк логов системы:

```bash
root@lime-Virtual-Machine:/home/lime# dmesg | tail -n 30
[    4.783070] IPv6: ADDRCONF(NETDEV_CHANGE): eth0: link becomes ready
[    4.804163] loop8: detected capacity change from 0 to 8
[   15.300416] kauditd_printk_skb: 34 callbacks suppressed
[   15.300418] audit: type=1400 audit(1678345590.213:45): apparmor="DENIED" operation="capable" profile="/usr/lib/snapd/snap-confine" pid=805 comm="snap-confine" capability=12  capname="net_admin"
[   15.300575] audit: type=1400 audit(1678345590.213:46): apparmor="DENIED" operation="capable" profile="/usr/lib/snapd/snap-confine" pid=805 comm="snap-confine" capability=38  capname="perfmon"
[   15.322366] audit: type=1400 audit(1678345590.233:47): apparmor="DENIED" operation="capable" profile="/usr/lib/snapd/snap-confine" pid=805 comm="snap-confine" capability=4  capname="fsetid"
[   15.658791] audit: type=1400 audit(1678345590.569:48): apparmor="DENIED" operation="capable" profile="/usr/lib/snapd/snap-confine" pid=900 comm="snap-confine" capability=12  capname="net_admin"
[   15.658798] audit: type=1400 audit(1678345590.569:49): apparmor="DENIED" operation="capable" profile="/usr/lib/snapd/snap-confine" pid=900 comm="snap-confine" capability=38  capname="perfmon"
[   16.222619] audit: type=1400 audit(1678345591.133:50): apparmor="DENIED" operation="capable" profile="/usr/lib/snapd/snap-confine" pid=1029 comm="snap-confine" capability=12  capname="net_admin"
[   16.222628] audit: type=1400 audit(1678345591.133:51): apparmor="DENIED" operation="capable" profile="/usr/lib/snapd/snap-confine" pid=1029 comm="snap-confine" capability=38  capname="perfmon"
[   16.832282] rfkill: input handler disabled
[   48.562223] audit: type=1326 audit(1678345623.473:52): auid=1000 uid=1000 gid=1000 ses=2 subj=? pid=1901 comm="snap-store" exe="/snap/snap-store/582/usr/bin/snap-store" sig=0 arch=c000003e syscall=314 compat=0 ip=0x7f269d63276d code=0x50000
[   50.689158] audit: type=1326 audit(1678345625.601:53): auid=1000 uid=1000 gid=1000 ses=2 subj=? pid=1901 comm="snap-store" exe="/snap/snap-store/582/usr/bin/snap-store" sig=0 arch=c000003e syscall=93 compat=0 ip=0x7f269d6293cb code=0x50000
[   50.724506] audit: type=1107 audit(1678345625.637:54): pid=526 uid=102 auid=4294967295 ses=4294967295 subj=? msg='apparmor="DENIED" operation="dbus_method_call"  bus="system" path="/org/freedesktop/PolicyKit1/Authority" interface="org.freedesktop.DBus.Properties" member="GetAll" mask="send" name=":1.6" pid=1901 label="snap.snap-store.ubuntu-software" peer_pid=541 peer_label="unconfined"
                exe="/usr/bin/dbus-daemon" sauid=102 hostname=? addr=? terminal=?'
[   50.724515] audit: type=1420 audit(1678345625.637:55): subj_apparmor=unconfined
[   50.725132] audit: type=1107 audit(1678345625.637:56): pid=526 uid=102 auid=4294967295 ses=4294967295 subj=? msg='apparmor="DENIED" operation="dbus_method_call"  bus="system" path="/org/freedesktop/PolicyKit1/Authority" interface="org.freedesktop.PolicyKit1.Authority" member="CheckAuthorization" mask="send" name=":1.6" pid=1901 label="snap.snap-store.ubuntu-software" peer_pid=541 peer_label="unconfined"
                exe="/usr/bin/dbus-daemon" sauid=102 hostname=? addr=? terminal=?'
[   50.725139] audit: type=1420 audit(1678345625.637:57): subj_apparmor=unconfined
[   50.738199] audit: type=1107 audit(1678345625.649:58): pid=526 uid=102 auid=4294967295 ses=4294967295 subj=? msg='apparmor="DENIED" operation="dbus_method_call"  bus="system" path="/org/freedesktop/PolicyKit1/Authority" interface="org.freedesktop.DBus.Properties" member="GetAll" mask="send" name=":1.6" pid=1901 label="snap.snap-store.ubuntu-software" peer_pid=541 peer_label="unconfined"
                exe="/usr/bin/dbus-daemon" sauid=102 hostname=? addr=? terminal=?'
[   50.738205] audit: type=1420 audit(1678345625.649:59): subj_apparmor=unconfined
[   50.738748] audit: type=1107 audit(1678345625.649:60): pid=526 uid=102 auid=4294967295 ses=4294967295 subj=? msg='apparmor="DENIED" operation="dbus_method_call"  bus="system" path="/org/freedesktop/PolicyKit1/Authority" interface="org.freedesktop.PolicyKit1.Authority" member="CheckAuthorization" mask="send" name=":1.6" pid=1901 label="snap.snap-store.ubuntu-software" peer_pid=541 peer_label="unconfined"
                exe="/usr/bin/dbus-daemon" sauid=102 hostname=? addr=? terminal=?'
[   50.738754] audit: type=1420 audit(1678345625.649:61): subj_apparmor=unconfined
[   52.008506] hv_balloon: Max. dynamic memory size: 1048576 MB
[   59.493935] Built 1 zonelists, mobility grouping on.  Total pages: 505240
[   59.493938] Policy zone: Normal
[   78.307010] kauditd_printk_skb: 2 callbacks suppressed
[   78.307013] audit: type=1326 audit(1678345653.217:64): auid=1000 uid=1000 gid=1000 ses=2 subj=? pid=1901 comm="pool-org.gnome." exe="/snap/snap-store/582/usr/bin/snap-store" sig=0 arch=c000003e syscall=93 compat=0 ip=0x7f269d6293cb code=0x50000
```

## Оценка результата

В результате лабораторной работы была получена базовая информация об используемой системе.

## Вывод

Таким образом мы научились, используя команды оболочки bash, собирать и анализировать необходимую нам информацию о системе.
