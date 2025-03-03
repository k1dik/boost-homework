Домашнее задание
Студента группы ИУ8-<номер группы> < Ваша фамилия и имя >

1. Скачайте библиотеку boost с помощью утилиты wget. Адрес для скачивания https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz.
$ $ wget https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz
результат скачивания не скопировал(
2. Разархивируйте скаченный файл в директорию ~/boost_1_69_0
$ ~/boost_1_69_0
$ mkdir ~/boost_1_69_0
$ tar -xvzf boost_1_69_0.tar.gz -C ~/boost_1_69_0
смотреть папку output tarr.txt
3. Подсчитайте количество файлов в директории ~/boost_1_69_0 не включая вложенные директории.
$ ~/boost_1_69_0 не включая вложенные директории
$ find ~/boost_1_69_0 -maxdepth 1 -type f | wc -l
смотреть папку output header_files.txt
4. Подсчитайте количество файлов в директории ~/boost_1_69_0 включая вложенные директории.
$ ~/boost_1_69_0 включая вложенные директории
$ find ~/boost_1_69_0 -type f | wc -l
смотреть папку output cpp_files.txt
5. Подсчитайте количество заголовочных файлов, файлов с расширением .cpp, сколько остальных файлов (не заголовочных и не .cpp).
$  find ~/boost_1_69_0 -type f -name "*.hpp" | wc -l
$ find ~/boost_1_69_0 -type f -name "*.cpp" | wc -l
$ find ~/boost_1_69_0 -type f ! -name "*.hpp" ! -name "*.cpp" | wc -l
смотреть папку output other.txt
6. Найдите полный пусть до файла any.hpp внутри библиотеки boost.
$ find ~/boost_1_69_0 -name "any.hpp"
смотреть папку output asio_references.txt
7. Выведите в консоль все файлы, где упоминается последовательность boost::asio.
$ grep -r "boost::asio" ~/boost_1_69_0 > boost_asio_files.txt
смотреть папку output asio_references.txt
8. Скомпилирутйе boost. Можно воспользоваться инструкцией или ссылкой.
$ cd ~/boost_1_69_0
$ ./bootstrap.sh
$ ./b2
смотреть папку output b2.txt
9. Перенесите все скомпилированные на предыдущем шаге статические библиотеки в директорию ~/boost-libs.
$ mkdir ~/boost-libs
$ cp -r ~/boost_1_69_0/stage/lib/* ~/boost-libs
ничего не выводит
10. Подсчитайте сколько занимает дискового пространства каждый файл в этой директории.
$ du -sh ~/boost-libs/*
смотреть папку output boost_libs_sizes.txt
11. Найдите топ10 самых "тяжёлых".
$ du -sh ~/boost-libs/* | sort -rh | head -n 10
смотерть папку output top10_heaviest_files.txt
