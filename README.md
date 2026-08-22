# vxwmguide
Более простая инструкция для vxwm на Arch Linux



### Установка на Arch Linux:


Установить Arch в ручную (можно использовать Installation guide) или через archinstall

если через archinstall настраиваем как обычно, но обязательно:
в Profile выбрать Type - Xorg, после выбрать Back вернуться обратно в Profile - Greeter, выбрать любой который нравится или без него (я выберу ly)



после установки и перезагрузки зайти в shell под своим юзером

(необязательно) обновить систему sudo pacman -Syu



xorg server xinitrc

xorg-server xorg-xinit

Все Зависимости которые понадобятся
sudo pacman -Sy libx11 libxft libxinerama base-devel git make gcc nano xorg (xorg-server xorg-xinit) 


git clone https://codeberg.org/wh1tepearl/vxwm.git
cd vxwm


make

sudo make clean install

зайти в nano ~/.xinitrc

пишем
#!/bin/sh

exec vxwm

или Если вы хотите перезагрузить vxwm без потери сеанса или для перезагрузки горячей конфигурации, добавьте что-то подобное в свой .xinitrc должно быть что-то вроде этого:

#!/bin/sh

vxwm &
exec sleep infinity


после ctrl+o и ctrl+x





терминал st

Скачайте или склонируйте репозиторий проекта: git clone https://git.suckless.org/st

Перейдите в папку с программой: cd st

Создайте файл конфигурации config.h на основе файла по умолчанию: cp config.def.h config.h

Соберите и установите терминал с помощью команды: sudo make clean install


обязательно устнавливаем firefox
