# Библиотека APK

Два независимых Android-приложения в одном репозитории (Gradle flavors):

| Приложение | applicationId | Папка |
|---|---|---|
| Kussia88 кликер | `com.kussia.clicker` | `app/src/kussia/` |
| Слива кликер | `com.sliva.clicker` | `app/src/sliva/` |

У каждого свои игра (`assets/index.html`), иконка и название, а общая оболочка WebView лежит в `app/src/main/`.
Разные `applicationId` значит, что установка одного приложения не заменяет другое.

Сборка запускается при каждом пуше в `main` и выкладывает на сайт (GitHub Pages) библиотеку APK. Список приложений лежит в `site/apps.json`: чтобы добавить новое, допишите туда запись.
APK подписываются постоянным ключом `app/debug.keystore`, поэтому новые версии ставятся поверх старых как обновление.

## Добавить клипы в Kussia88 кликер
Положите ролик в `app/src/kussia/assets/clips/` под следующим номером (`m16.mp4`, H.264 + AAC, ~480×280) и увеличьте `CLIPS` в `app/src/kussia/assets/index.html`.
