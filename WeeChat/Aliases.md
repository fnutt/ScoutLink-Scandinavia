# Alias-tips för JOTI för dig som använder WeeChat-klienten

## /TBAN
För att få /TBAN att fungera i WeeChat så skapar du en alias med kommandot
```
/alias add TBAN quote tban $1 $2 $3
```

För att bli påmind om parametrarna så skickar du bara kommandot `/tban`, hela kommandot är
```
/tban <#kanalnamn> <tid> <nick>
```

* Tiden är i sekunder om du bara ange siffror. För 10 minuter skriver du `10m` (eller 600 för 600 sekunder) och för en timme skriver du `1h` (eller 3600 för 3600 sekunder).
* Nick:et kommer översättas till lämplig banmask med automatik.

## OP/DEOP/VOICE/DEVOICE
Här följer fyra stycken alias för att enkelt ändra de egna rättigheterna i en kanal i stället för exempelvis det långa `/msg chanserv op <#kanalnamn> <nick>` och utan att använda exempelvis `!op` som vanliga användare ser.

### /OPUP
```
/alias add OPUP quote cs op $channel $nick
```

### /OPDOWN
```
/alias add OPDOWN quote cs deop $channel $nick
```

### /VOICEUP
```
/alias add VOICEUP quote cs voice $channel $nick
```

### /VOICEDOWN
```
/alias add VOICEDOWN quote cs devoice $channel $nick
```
