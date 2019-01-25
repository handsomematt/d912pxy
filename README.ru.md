
# | [EN](https://github.com/megai2/d912pxy#d912pxy---directx9-to-directx12-api-proxy-for-guild-wars-2) | [RU](https://github.com/megai2/d912pxy#d912pxy---directx9-to-directx12-api-proxy-for-guild-wars-2-1) |

# d912pxy - "DirectX9 to DirectX12 API proxy for Guild Wars 2"

-Что делает эта штука?

-Позволяет играм, которые используют DirectX9, использовать DirectX12 без изменений в игровом коде. 

 К таким играм относится и Guild Wars 2, для которой и написана данная библиотека. Можете попробовать использовать эту библиотеку в других играх, возможно она будет работать.
 
 
 Этот проект ещё не завершен и находится в стадии альфа тестирования, возможны зависания, ошибки и вылеты!
 
 Текущая версия: v0.9.5.5 альфа
 Отзывы приветствуются!
 
# Результаты

Тестирование показывает, что дополнительные расходы при работе с d912pxy до 70% меньше, чем при работе с обычным DirectX9.
Реальная производительность зависит от сцены и от железа!

DX12:

https://cdn.discordapp.com/attachments/477036595019644928/524540609105756160/unknown.png 


DX9:

https://cdn.discordapp.com/attachments/477036595019644928/524541036626837504/unknown.png

   
# Требования

Windows 10, Видеокарта с поддержкой DirectX12, конкретно 12.1 feature level и 3+ Gb VRAM.

16 Gb системной памяти

(будет изменятся по мере оптимизации)
 
# Как использовать

1. Рекомендуется: Установите поле "Resolution" в настройках графики в "Fullscreen windowed"/"Windowed"
2. Выключите все оверлеи/аддоны
3. Скачайте последний доступный релиз [ссылка](https://github.com/megai2/d912pxy/releases/tag/v0.9.5.5a)
4. Распакуйте архив в папку с игрой, так чтобы папка d912pxy находилась в корневой папке игры.
5. Запустите d912pxy/install.bat
6. Запустите игру

# Как удалить

1. Запустите d912pxy/remove.bat
2. Удалите папку d912pxy
3. Готово

# Извесные проблемы

-Функция скриншотов не работает

# Решение проблем

## Случай 1
  Мир долго прогружается, прогружается по частям.
  
**Решение**

  d912pxy загружает шейдеры асинхронно, т.к. невозможно эффективно загружать шейдеры сразу.
  
  Такой подход может создать некоторые графические ошибки, но с другой стороны более эффективен по производительности.
  
  
## Случай 2
  Игра вылетает, зависает.
  
**Решение**

  Не обращайтесь в техподдержку игры, если установили d912pxy!
  
  Если игра падает без d912pxy, не спрашивайте об этом здесь, т.к. d912pxy не делает модификаций в игровых файлах.
    
  Удостоверьтесь, что игра работает без d912pxy.  
  
  Далее обновите графические драйвера и обновите DirectX9!
    
  (ссылка на установку dx9 https://www.microsoft.com/ru-ru/download/details.aspx?id=34429)
  
  Если проблема не решена, напишите о ней на github вместе со следующей информацией:
  
    1. Лог файл из папки P7logs
    2. Crash.dmp и d912pxy_crash.txt если он у вас появился
    
 Если вас попросят запустить дебаг версию, следуйте данной инструкции:
 
   0. Дебаг версия записывает огромное количество данных, не запускайте её надолго!
   1. Запустить d912pxy/remove.bat
   2. Запустить d912pxy/install_debug.bat
   3. Запустить игру
   4. Отправить лог файл и Crash.dmp на github

## Случай 3 

  Ошибки в графике
 
**Решение**

  1. Запустите d912pxy/remove.bat
  2. Запустите d912pxy/install_ps.bat
  3. Запустите игру, повторите найденную ошибку в графике.
  4. Запустите d912pxy/clean_shaders.bat
  5. Запустите d912pxy/remove.bat
  6. Запустите d912pxy/install.bat
  7. Запустите игру заново. Подождите пока шейдеры перекомпилируются.
  8. Если ошибка не исправлена, напишите о ней на github вместе с описанием того, как данную ошибку повторить.  
  
# Поддержка разработчика

 WMR 232397187043