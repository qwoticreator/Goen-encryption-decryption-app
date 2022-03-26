
<img src="app/src/main/ic_launcher-playstore.png" align="left"
width="200" hspace="10" vspace="10">


## About

Goen can hide the text given in the provided image and that image user can send to anyone freely.
The same image can be decrypted and data/text can be retrieved from it using this app.
Can be used for both- fun or security purposes.


## Как работает

Шифрование-
- Входные данные: код из 16 цифр, текст (который должен быть скрыт), изображение (в котором текст должен быть скрыт).
- Текст преобразуется в bytearray и передается в шифрование AES с использованием библиотеки шифрования Android.
- Зашифрованный текст в форме bytearray, преобразуется в кодировку Base64.
- Каждый символ строки base64 преобразуется в двоичное значение и объединяется в виде строки с завершающей строкой с обеих сторон.
- Двоичная строка затем вставляется в изображение с помощью метода LSB.
- Изображение появляется у вас на устройстве.

Дешифрование-
- Входные данные - код из 16 цифр (тот же, что использовался для шифрования),изображение (в котором скрыты данные).
- Двоичные данные, извлекаются из пикселей изображения, просто изменив процесс метода LSB.
- Двоичная строка преобразуется обратно в строку base64 и строка base64 снова декодируется в bytearray.
- Bytearray передается в алгоритм AES, и с помощью ключа данные расшифровываются.
- Окончательный расшифрованный bytearray преобразуется в текст (utf-8) и отображается на экране.

## Screenshots & Demo gif

[<img src="/screenshots/screens1.png" align="left"
width="200"
hspace="10" vspace="10">](/screenshots/screens1.png)
[<img src="/screenshots/screens2.png" align="left"
width="200"
hspace="10" vspace="10">](/screenshots/screens2.png)

[<img src="/screenshots/preview.gif" align="center"
width="200"
hspace="10" vspace="10">](/screenshots/preview.gif)



