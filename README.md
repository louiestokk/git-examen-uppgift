# Fråga 1: Versionshantering vs vanliga filer
## Svar
Versionshantering är ett system som sparar/registrerar ändringar man gör i en fil eller projekt över tid. Detta gör att man kan återskapa specefika versioner senare, man kan se historik och samarbeta med andra utan att skriva över varandras kod.

** Skillnaden mellan att spara lokalt och git? ** Den stora skillnaden är att editorns vanliga sparaknapp sparar ändringarna i filen på datorn, medan Git sparar en version av ändringarna i historiken genom en commit. På så sätt kan man följa kodens utveckling och återställa äldre versioner.

## VG
Att Git sparar en tidslinje av frysta ögonblicksbilder betyder att varje commit sparar en bestämd version av projektet vid ett visst tillfälle. Varje commit blir en del av projektets historik, så att man kan gå tillbaka och se hur koden såg ut tidigare.

Att man fortfarande kan se alla tre TODO i den första committen på GitHub, trots att koden på datorn har ändrats, bevisar att Git bevarar tidigare versioner oberoende av de senare ändringarna. Den första committen skrivs inte över när man ändrar och sparar filen på nytt. I stället skapas nya commits som visar hur projektet har utvecklats. Därför kan man jämföra olika versioner och se exakt hur koden har förändrats över tid.

# Fråga 2: Arbetsytan, Staging och Commits
## svar
- git status visar vilka filer som har ändrats, vilka filer som är redo att sparas i en commit och vilka filer Git inte spårar ännu. Jag kör kommandot för att kontrollera projektets status.

- git add lägger till ändringar i stagingområdet, alltså de ändringar jag vill inkludera i nästa commit. Jag kör kommandot när jag har gjort ändringar som jag vill spara i Git.

- git commit sparar ändringarna från stagingområdet som en ny version i projektets historik. Jag kör kommandot när jag vill skapa en ny version och brukar skriva ett meddelande som beskriver vad jag har ändrat.

## VG
Man kan jämföra Git med att hantera viktiga dokument:

- Arbetsytan (arket på skrivbordet): Här arbetar jag med mina filer och gör ändringar i koden. Ändringarna finns på datorn, men de är ännu inte valda för nästa commit.

- Staging (kuvertet): När jag kör git add lägger jag de ändringar jag vill spara i nästa version i stagingområdet. Det är som att lägga rätt dokument i ett kuvert innan det skickas vidare.

- Commit (arkivlådan): När jag kör git commit sparas innehållet i stagingområdet som en ny version i Git-historiken. Det är som att lägga kuvertets innehåll i arkivlådan, där det bevaras som en del av historiken.

Git protesterar med meddelandet no changes added to commit om jag har ändrat en fil men inte kört git add, eftersom Git skiljer mellan ändringar i arbetsytan och ändringar som har valts ut i stagingområdet. Kommandot git commit sparar bara de ändringar som finns i stagingområdet, inte automatiskt allt jag har ändrat i editorn.

Därför är det viktigt att först kontrollera ändringarna med git status, sedan köra git add för de filer eller ändringar jag vill spara och till sist köra git commit för att skapa en ny version. På så sätt har jag kontroll över exakt vilka ändringar som hamnar i varje commit.

# Fråga 3: Lådan hemma vs Montern på GitHub
## svar
Mappen på min dator är mitt lokala repository där jag arbetar med koden och sparar ändringar med Git. Repot på GitHub är en kopia av projektets Git-historik som finns online och som jag kan dela med andra.

Kommandot git push skickar mina lokala commits till repot på GitHub, så att de senaste versionerna blir tillgängliga online.

## VG
Man kan tänka på Git som två olika minnesytor:

- Lådan hemma (det lokala repot): Här finns projektets Git-historik på min dator. Jag kan ändra filer, staga ändringar och skapa commits utan att behöva internet.

- Glasmontern på GitHub (det fjärranslutna repot): Här visas de commits som jag har skickat upp från min dator med git push. Andra kan se och hämta dessa versioner.

När jag ändrar kod i editorn förändras arbetsytan, men ändringarna blir inte automatiskt en del av Git-historiken. Först måste jag köra git add för att välja ändringarna och sedan git commit för att spara dem som en ny version i det lokala repot. Därefter kan jag använda git push för att skicka committen till GitHub.

Om jag har ändrat koden men glömt att köra git add och git commit, svarar Git Everything up-to-date när jag kör git push, förutsatt att det inte finns några andra lokala commits att skicka. Det beror på att git push bara skickar commits, inte osparade ändringar från arbetsytan eller stagingområdet.
