Publisering på ditt hjemmeområdet på internett [toppen]
-------------------------------------------------------

* [Windows](#windows)
* [Mac](#mac)
* [Linux](#linux)
* [Terminal](#terminal)
* [Bidra](#bidra)

# Windows
1. Under "Computer" trykk "Map Network drive"
>![](ms_step1.png)

2. Skriv inn server-adresse som bå bildet, men med ditt studentnummer. Huk av for "Connect using different credentials"
>![](ms_step2.png)

3. Skriv inn "ADA\sxxxxxx" der xxxxxx er ditt studentnummer, og passord. Vurder selv om du ønsker at passordet skal huskes - gjør dette kun dersom du har et sikkert passord på din PC, som automatisk kommer på.
>![](ms_step3.png)

4. Du får nå opp en mappe med ditt hjemmeområde. Alt som legges inne i www-mappen havner på nett.
>![](ms_step4.png)

5. HTML-filer kan legges direkte i denne mappen, eller du kan legge det i undermapper
>![](ms_step5.png)

6. Ditt hjemmeområde er nå synlig under "Computer", og tilgjengelig som en hvilken som helst annen mappe, for kopiering og lagring.
>![](ms_step6.png)

7. Dersom du har lagt fila "webprosjekt.html" under www-mappen, vil den være tilgjengelig for browseren med url'en "student.cs.hioa.no/~sxxxxxx/webprosjekt.html" der xxxxxx er ditt studentnr.
>![](ms_step7.png)

[Til toppen](#toppen)


# Mac

1. Finder > Go > Connect to Server.
>![](mac_step1.png)

2. Skriv inn server-adresse som bå bildet, men med ditt studentnummer, begge steder i adressen. 
>![](mac_step2.png)

3. Skriv inn ditt passord. Velg selv om du vil huske passordet i "Keychain"
>![](mac_step3.png)

4. Du vil nå få opp ditt hjemmeområde som en "drive" på din mac (tilsvarende som når du installerer programmer). Driven vil være dilgjengelig via et disk-ikon på ditt skrivebord, og i finder. Det du nå legger i mappen "www" på ditt hjemmeområde, blir synlig på nett.
>![](mac_step5.png)

5. Dersom du nå legger en HTML-fil i din www-mappe og kaller den `webprosjekt.html` kan du åpne den i en browser via adressen "student.cs.hioa.no/~sxxxxxx/webprosjekt.html" der xxxxxx er ditt studentnummer.
>![](mac_step6.png)


[Til toppen](#toppen) 



#Linux
Det vil variere mellom de ulike linux- distribusjonene hvordan dette gjøres via GUI, men her er en veiledning fra **Ubuntu 12.04 LTS**. Det er sannsynligvis svært likt på de fleste andre moderne distroer.

1. Fra filmenyen i Nautilus (Gå feks. via "Home Folder"), trykk "Go > Location". Du får da opp et utforskervindu, med en adresselinje. Skriv inn adressen som på bildet, men med ditt studentnummer.
>![](linux_step1.png)

2. Skriv inn "ADA" under Domain, og ditt passord i passordfeltet. Velg selv hvor lenge passordet skal huskes - husk bare passordet dersom du har aktivert automatisk utlogging/låsing av maskinen din.
>![](linux_step2.png)

3. Du får nå opp et utforskervindu med ditt hjemmeområde. Alt som legges i www-mappen havner på nett.
>![](linux_step3.png)

4. Du kan nå feks. lage et HTML-dokument her, kalt `webprosjekt.html`. Www-mappen i ditt hjemmeområde er tilgjengelig som en vanlig mappe, fra alle programmer.
>![](linux_step4.png)

5. Dette dokumentet er nå tilgjengelig via internett, på adressen "student.cs.hioa.no/~sxxxxxx" der xxxxxx er ditt studentnummer.
>![](linux_step5.png)

6. Hjemmeområdet ditt er også tilgjengelig via terminal. Det vil variere hvor området blir montert opp avhengig av distribusjon. For Ubuntu 12.04 havner mappen i `~/.gvfs/sxxxxxx` der xxxxxx er ditt studentnr. Er du usikker på hvor mappen havnet kan du skrive `$ mount` og se etter linjen med "gvfs". 
>![](linux_step6.png)

Det er også mulig å montere opp (mounte) hjemmeområdet manuelt i terminal, som et hvilket som helst samba-share. Da kan du få det i den mappen du ønsker. For denne løsningen, google "mount samba share [din favoritt-distro]"

[Til toppen](#toppen)


# Jobbe i terminal [terminal]
I både linux og Mac har du flere muligheter for å jobbe via terminal. Foreløpig vil vi forutsette at man mounter opp sitt hjemmeområde som beskrevet over, først.

For mac vil hjemmeområdet finnes under `/Volumes/sxxxxxx` der xxxxxx er ditt studentnr.

    	alfreb$ cd /Volumes/s173682/
		alfreb$ ls
		alfreb$ cd www
		alfreb$ ls -l
		...
		-rw-r--r--   1 alfreb  staff     34 Aug 19  2011 verden.php
		drwxr-xr-x   2 alfreb  staff  16384 Sep  2 15:47 webprosjekt
		-rw-r--r--   1 alfreb  staff    132 Sep  2 13:37 webprosjekt.html 

For hvor området havner i Linux, se forrige avsnitt. 

Når du har funnet frem til hvor hjemmeområdet ditt ligger, kan du redigere filene der direkte, feks. med emacs:

		alfreb$ emacs webprosjekt.html

Når du lagrer vil filen oppdateres direkte på server, og være tilgjengelig for hele verden.		

[Til toppen](#toppen)

#Bidra til denne fila! [bidra]
Dersom du ser ting som kunne vært beskrevet bedre, eller dersom du feks. har funnet ut hvordan man kobler seg til via et annet OS, føl deg fri til å forke repositoriet, oppdatere denne fila, committe, pushe og sende pull-request. Er bidraget seriøst og nyttig blir det inkludert her.