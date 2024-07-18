# 01_lock 
Was passiert, wenn vendor weg ist, aber composer.json und ...lock noch da sind?

**Erwartung:** `composer update` bzw `install` liefert dann immer das gleiche vendor-Verzeichnis

	composer init
	composer require league/color-extractor:0.4.0

Die Erwartung wurde erfüllt. Wenn es sich wirklich eine blanke Erstinstallation handelt, dann funktioniert `composer install.

Falls Änderungen an der `composer.json` vorgenommen werden, muss aber `composer update` durchgeführt werden (klingt auch logisch, bei einem Install würde auch abgebrochen werden, mit einer entsprechenden Warnmeldung.)

Um ein neues Package hinzuzufügen, verwendet man `composer require`. Die `compose.json` wird nur in Ausnahmefällen manuell editiert!
			
Im Package `spatie/color` kann man in der `composer.json` die Verwendung von Abhängigkeiten bei verschiedenen PHP-Versionen sehen.

