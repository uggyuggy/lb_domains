# .lb domain names

## 🎯 Purpose

This repository purpose is to daily share the list of `.lb` domain names. (As I have not found another public share of this list for now)

So people don't have to do it on their side too (as long as list is updated here of course).



## ☕ Sample

```
$ curl -s -L https://github.com/uggyuggy/lb_domains/raw/main/lb.txt -o lb.txt
$
$ wc -l lb.txt 
2659 lb.txt
$
$ head lb.txt
# .lb domain names extracted from nameservers on 20Jun2024 15:48 UTC
3mplast.com.lb.
3w.com.lb.
4g.com.lb.
4media.com.lb.
605.com.lb.
a.com.lb.
aa.org.lb.
aaasarl.com.lb.
aab.org.lb.
$
```


## 📰 Informations

- Data is retrieved using DNS "zone walking" method

- There is no garantee of anything (I hope the zone is "full".. but who knows except the registry ?)

- When writing this, I think there is no domains at the apex of the lb. zone.
All seems to be under SLDs like `.com.lb.`, `.org.lb.`, `.net.lb.` ...


- You may be interested by some other "zone walked" TLDs.
Look into https://github.com/maaaaz/dnsdumps repo which provides others
(`.lb` discussed into https://github.com/maaaaz/dnsdumps/issues/1)

- There is around 2659 domain names (as the time of writing this page)

- The file served here should be updated 1 time per day to not overload the remote servers for no reason.

- The file contains an additional comment line at the top starting with `#` that contain an UTC date information.

- For now there is a single comment line, but in case I add more in the future, you may better remove everything that start with a `#`

- The domain names end with `.lb.` (Ending dot, as FQDN)

- The domain names are provided sorted ( `LC_ALL=C sort -u`)

- It looks like there is no IDN domains for now

- If there is no domain list provided for a specific day, this could mean my script failed to build/push the list due to:
  - The DNS remote servers rejected me / blacklisted me
  - My script was not able to recover from some errors.
  - The .lb remote servers are down
  - My own client server running the script is down
  - Github was down :)
  - Network issue, DNS issue ...
  - ...
- You should be able to guess if the file has been updated successfully by checking either:
  - The date into the first comment line. `LC_TIME=C date -u +'%d%b%Y %H:%M UTC'`
  - The date of the last Github commit


## 🚧 Todo

- [x] Write README
- [x] Add emojis to the README (very important 🚨)
- [ ] Inform maaaaz/dnsdumps/issues/1
- [ ] Add more warning notifications in case of script failures
- [ ] Add more control to guess if something went wrong with script
- [ ] After I will be confident it's running as expected, possibly informing https://github.com/jschauma/tld-zoneinfo/
- [ ] ...




