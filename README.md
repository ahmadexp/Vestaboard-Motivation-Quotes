## Send to your vestaboard one of the motivational quotes randomly.



/etc/systemd/system/vesta-moto.service

```
[Unit]
Description=Vestaboard Moto Quotes

[Service]
Type=oneshot
ExecStart=/usr/bin/python3 /usr/bin/Vesta.py

[Install]
WantedBy=multi-user.target
```


/etc/systemd/system/vesta-moto.timer

```
[Unit]
Description=Vestaboard Moto Quotes

[Timer]
OnCalendar=*-*-* *:00/5:05
Persistent=true

[Install]
WantedBy=timers.target
```

