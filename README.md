# ThanksAbu
Исправляет битые изображения на имиджборде 2ch.hk, а также добавляет поддержку воспроизведение webm через VLC-плагин для Safari

## Как оно работает
Данный скрипт заменяет код, отвечающий за просмотр контента в сплывающем элементе. Если пользователь открывает картинку, то скрипт смотрит тип сжатия и, если
 это все таки jpeg, то заглядывает глубже. А именно, ищет в жипеге секцию JIFF-APP0, смотрит ее длину и, если она кастрированная, добавляет нехватающие пару байтов и вписывает верное значение в поле length (спасибо за наводку анонам из /d/).
 
 Если пользователь открывает webm, mp4 и mp3, то вместо html5-плеера используется плеер от VLC.

## Установка
1. Установите расширение Tampermonkey (http://tampermonkey.net).
1. Установите плагин VLC для Safari (достать VLC-webplugin с главной страницы оффсайта пока невозможно, можно здесь https://nightlies.videolan.org/build/macosx-intel/).
1. Создайте пользовательский скрипт в Tampermonkey, вставив в него содержимое из *ThanksAbu.js*.
1. **ВАЖНО**: установите параметр скрипта "Запускать при" в значение "document-idle" (как показано на пикче ниже). Иначе скрипт Абу будет перекрывать наши старания.
![Настройка скрипта](https://raw.githubusercontent.com/Chupik/ThanksAbu/master/images/AbuSettings.png)
1. Пользуйтесь.

## Вопросы на возможные ответы
**Q:** Это не вишмастер случаем?!

**A:** Исходники полностью открыты, смотрите и ищите закладку.

