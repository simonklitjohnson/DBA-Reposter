# DBA Reposter

DBA Reposter tager alle dine aktive opslag på DBA og poster et nyt, identisk opslag, for at holde dit opslag øverst i søgningen. Den lader det gamle opslag eksistere i 10 runs (scriptet kører 10 gange) før det slettes, men mindre kan sættes med --keep argumentet. Dette gør at folk som har favoriseret eller bogmærket en annonce ikke pludselig finder den deaktiveret efter reposting.  
  
Den reposter ikke opslag der er deaktiverede eller har kommentarer på sig.  
    
Scriptet er skrevet i Python og kræver følgende for at fungere:  
* Python 3 eller nyere  
* fuzzywuzzy (pip install fuzzywuzzy - husk at installere det til python3 og ikke 2.7)  
* requests (pip install requests - husk at installere det til python3 og ikke 2.7)  
  
Bruges således:  
```shell
python dbareposter.py username password [--keep=integer|default:10] [--premium=boolean|default:false] [--repostall=boolean|default:false] [--verify=boolean|default:true]  
--keep=value: Venter indtil scriptet er kørt x-antal gange før repostede listings slettes.   
--repostall=value: Hvis True repostes en listing selv hvis den er inaktiv eller har kommentarer.
--premium=value: Hvis True postes nye listings som premium. OBS: Det koster, hvis du ikke har DBA+.  
--verify=value: Slå SSL verifikation til eller fra, med argumenterne "True" og "False".  
