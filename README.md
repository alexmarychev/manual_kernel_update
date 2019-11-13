###HW1

1. Установил vagrant и packer.
2. Склонировал репозиторий ```https://github.com/dmitry-lyutenko/manual_kernel_update```
3. Запустил виртуальную машину и залогинился в нее.
4. Подключил репозиторий ```sudo yum install -y http://www.elrepo.org/elrepo-release-7.0-3.el7.elrepo.noarch.rpm```
5. Установил последнее ядро ```sudo yum --enablerepo elrepo-kernel install kernel-ml -y```
6. Обновил конфигурацию загрузчика ```sudo grub2-mkconfig -o /boot/grub2/grub.cfg``` и выбрал загрузку с новым ядром по умолчанию ```sudo grub2-set-default 0```
7. Создал образ системы с новым ядром с помощью packer.
8. Протестировал образ.
9. Добавил образ в Vagrant Cloud. Ссылка: https://app.vagrantup.com/alexmarychev/boxes/centos-7-5

