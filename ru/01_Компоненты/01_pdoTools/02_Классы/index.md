Ядро компонента разделено на 3 класса: общий [pdoTools][1], работа с БД - [pdoFetch][2]</a> и работа с оформлением, то есть [pdoParser][3].

При установке в систему они регистрируются таким образом, чтобы вы могли быстро их запускать:
```
$pdoTools = $modx->getService('pdoTools');
$pdoFetch = $modx->getService('pdoFetch');
$pdoParser = $modx->getService('pdoParser');
```

pdoFetch наследует pdoTools, так что не нужно вызывать эти два класса вместе. Если вы хотите работать с БД, вызывайте один Fetch, а если нет - Tools.

Парсер вызывать вообще не нужно, он или включен в настройках MODX, или нет. pdoTools использует его для оформления чанков в любом случае.

[1]: /ru/01_Компоненты/01_pdoTools/02_Классы/01_pdoTools.md
[2]: /ru/01_Компоненты/01_pdoTools/02_Классы/02_pdoFetch.md
[3]: /ru/01_Компоненты/01_pdoTools/02_Классы/03_pdoParser.md