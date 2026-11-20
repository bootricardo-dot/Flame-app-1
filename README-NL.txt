FLAME Android – Redesign v3
===========================

Dit is de volledige Android-projectmap voor FLAME. De app gebruikt een lokale HTML-interface in een Android WebView.

Wat is bijgewerkt
-----------------
- Premium donkere vormgeving met rode FLAME-accenten, afgeronde kaarten en vijf hoofdnavigatieschermen.
- Dashboard met calorieënring, macrodoelen, waterregistratie en trainingsstatus.
- Voedingsregistratie met handmatige invoer, Open Food Facts zoeken, favorieten, maaltijden en barcodecamera (afhankelijk van Android WebView-ondersteuning).
- Trainingsschema, oefeningencatalogus, trainingslogboek en progressieoverzichten.
- Doelen aanpassen en lokale JSON-back-up exporteren/importeren.
- Correctie van de weekplanning zodat een training wordt vastgelegd op de gekozen datum.
- Correctie van de knop Oefening toevoegen: deze voegt nu een oefening toe aan de catalogus in plaats van meteen een trainingslog te maken.

Projectstructuur
----------------
Upload de inhoud van deze ZIP naar de hoofdmap van de GitHub-repository. Behoud de mappenstructuur:
- app/
- .github/workflows/build-apk.yml
- build.gradle
- settings.gradle
- gradle.properties

APK bouwen via GitHub
---------------------
1. Upload/vervang de projectbestanden in de repository en commit naar main.
2. Open GitHub Actions.
3. Open de workflow Build FLAME APK en wacht op een groene status.
4. Download het artifact FLAME-debug-apk en pak de ZIP uit.
5. Installeer app-debug.apk op een Android-testtoestel.

Teststatus en beperkingen
-------------------------
- JavaScript-syntaxcontrole: geslaagd.
- AndroidManifest XML-controle: geslaagd.
- De volledige Android/Gradle-build en praktijktest op een echt toestel moeten nog via GitHub Actions en een Android-telefoon worden uitgevoerd.
- Productzoeken en barcode-opzoeken vereisen internet. Automatische barcodeherkenning is afhankelijk van de Android WebView-versie; handmatige barcode-invoer blijft beschikbaar.
- Registraties worden lokaal op het toestel opgeslagen. Maak regelmatig een back-up via Profiel > Instellingen & gegevens.
- Dit is een debug-APK, geen ondertekende Play Store-release.
