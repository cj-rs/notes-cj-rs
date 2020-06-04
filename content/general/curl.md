+++
+++
```
curl -w "@curlfmt" --connect-to r.cj.rs:443:127.0.0.1:443  -s -o /dev/null
```

```
    time_namelookup:  0.000097s
       time_connect:  0.001367s
    time_appconnect:  0.124008s   # After TLS
   time_pretransfer:  0.124560s
      time_redirect:  0.000000s
 time_starttransfer:  0.463918s   # Time to first byte
                    ----------
         time_total:  0.466945s
```

curlfmt file:
```
    time_namelookup:  %{time_namelookup}s\n
       time_connect:  %{time_connect}s\n
    time_appconnect:  %{time_appconnect}s\n
   time_pretransfer:  %{time_pretransfer}s\n
      time_redirect:  %{time_redirect}s\n
 time_starttransfer:  %{time_starttransfer}s\n
                    ----------\n
         time_total:  %{time_total}s\n
```
