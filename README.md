# tigervnc-cli
Used for adding, deleting, modifying, querying, starting and stopping of tigervnc.

不好意思啊，我英文差，基本都是机翻，通篇没有注释但是比较好懂，后期再慢慢补上注释吧。

```shell
example:
    tigervnc-cli -c check                   Confirm the status of all ports.
    tigervnc-cli -u user1 -c status         Confirm the service status of User1.
    tigervnc-cli -u user1 -l                ! Disable all ports for user1.
    tigervnc-cli -u user1 -l -p 3 4         ! Disable port 3 and port 4 of user1.

    ! <-- The symbol indicates that administrative privileges are required.
options:
  -h, --help            show this help message and exit
  -c COMMAND, --command COMMAND
                        operate tigervnc:
                        status   check service status
                        start    Start service
                        stop     Stop service
                        enable   Enable service and Start service
                        disable  Disable service and Stop service

  -u USER, --user USER  Enter username
  -p PORT [PORT ...], --port PORT [PORT ...]
                        Enter Port Number, Multiple entries can be made.

  -a, --add             ! Add Tigervnc Port
  -d, --delete          ! Delete Tigervnc Port
  -e EDIT, --edit EDIT  ! Input the modified port
  -s, --search          Search for user configuration
  -l, --locked          ! locked user
  -i, --unlocked        ! unlocked user
```