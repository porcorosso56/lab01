## Laboratory work I

Данная лабораторная работа посвещена изучению утилит для разработки проектов

## Tasks

- [x] 1. Ознакомиться со ссылками учебного материала
- [x] 2. Выполнить инструкцию учебного материала
- [x] 3. Составить отчет и отправить ссылку личным сообщением в **Slack**

## Tutorial

```bash
$ export GITHUB_USERNAME=<porcorosso56>
$ export GIST_TOKEN=<*******************>
$ alias edit=<nano|vi|vim|subl>
```

```ShellSession
$ mkdir -p ${GITHUB_USERNAME}/workspace
$ cd ${GITHUB_USERNAME}/workspace
$ pwd
/home/Asus/porcorsso56/workspace

$ cd ..
$ pwd
/home/Asus

```

```ShellSession
$ mkdir -p workspace/tasks/
$ mkdir -p workspace/projects/
$ mkdir -p workspace/reports/
$ cd workspace
```

```ShellSession
# Debian
$ wget https://nodejs.org/dist/v6.11.5/node-v6.11.5-win-x64.zip
$ unzip -xf node-v6.11.5-win-x64.zip
$ rm -rf node-v6.11.5-win-x64.zip
$ mv node-v6.11.5-win-x64.zipnode
```

```ShellSession
$ ls node/bin
$ echo ${PATH}
$ export PATH=${PATH}:`pwd`/node/bin
$ echo ${PATH}
/home/Asus/bin:/usr/local/bin:/home/Asus/.local/bin:/usr/local/bin:/usr/bin:/cygdrive/c/Program Files (x86)/Intel/iCLS Client:/cygdrive/c/Program Files/Intel/iCLS Client:/cygdrive/c/Windows/system32:/cygdrive/c/Windows:/cygdrive/c/Windows/System32/Wbem:/cygdrive/c/Windows/System32/WindowsPowerShell/v1.0:/cygdrive/c/Program Files (x86)/NVIDIA Corporation/PhysX/Common:/cygdrive/c/Program Files (x86)/Intel/Intel(R) Management Engine Components/DAL:/cygdrive/c/Program Files/Intel/Intel(R) Management Engine Components/DAL:/cygdrive/c/Program Files (x86)/Intel/Intel(R) Management Engine Components/IPT:/cygdrive/c/Program Files/Intel/Intel(R) Management Engine Components/IPT:/cygdrive/c/WINDOWS/system32:/cygdrive/c/WINDOWS:/cygdrive/c/WINDOWS/System32/Wbem:/cygdrive/c/WINDOWS/System32/WindowsPowerShell/v1.0:/cygdrive/c/WINDOWS/System32/OpenSSH:/cygdrive/c/Program Files/CMake/bin:/cygdrive/c/Users/Asus/AppData/Local/Microsoft/WindowsApps:/cygdrive/c/Users/Asus/.babun:/cygdrive/c/Users/Asus/AppData/Local/GitHubCLI/bin:/cygdrive/c/Program Files/mingw-w64/x86_64-8.1.0-posix-seh-rt_v6-rev0/mingw64/bin:/cygdrive/c/Program Files/Sublime Text 3

$ mkdir scripts
$ cat > scripts/activate<<EOF
export PATH=\${PATH}:`pwd`/node/bin
EOF
$ source scripts/activate
```

```ShellSession
$ npm install -g gistup
$ ls node/bin
```

```ShellSession
$ cat > ~/.gistup.json <<EOF
{
  "token": "${GIST_TOKEN}"
}
EOF
```

## Report

```ShellSession
$ export LAB_NUMBER=01
$ git clone https://github.com/tp-labs/lab${LAB_NUMBER} tasks/lab${LAB_NUMBER}
$ mkdir reports/lab${LAB_NUMBER}
$ cp tasks/lab${LAB_NUMBER}/README.md reports/lab${LAB_NUMBER}/REPORT.md
$ cd reports/lab${LAB_NUMBER}
$ edit REPORT.md
$ gistup -m "lab${LAB_NUMBER}" # enter: yes↵
```

## Links

### Unix commands

- [ar](https://en.wikipedia.org/wiki/Ar_(Unix))
- [cat](https://en.wikipedia.org/wiki/Cat_(Unix))
- [cd](https://en.wikipedia.org/wiki/Cd_(command))
- [cp](https://en.wikipedia.org/wiki/Cp_(Unix))
- [cut](https://en.wikipedia.org/wiki/Cut_(Unix))
- [echo](https://en.wikipedia.org/wiki/Echo_(command))
- [env](https://en.wikipedia.org/wiki/Env_(shell))
- [ex](https://en.wikipedia.org/wiki/Ex_(editor))
- [file](https://en.wikipedia.org/wiki/File_(command))
- [find](https://en.wikipedia.org/wiki/Find)
- [ls](https://en.wikipedia.org/wiki/Ls)
- [man](https://en.wikipedia.org/wiki/Man_page)
- [mkdir](https://en.wikipedia.org/wiki/Mkdir)
- [mv](https://en.wikipedia.org/wiki/Mv)
- [nm](https://en.wikipedia.org/wiki/Nm_(Unix))
- [ps](https://en.wikipedia.org/wiki/Ps_(Unix))
- [pwd](https://en.wikipedia.org/wiki/Pwd)
- [rm](https://en.wikipedia.org/wiki/Rm_(Unix))
- [sed](https://en.wikipedia.org/wiki/Sed)
- [touch](https://en.wikipedia.org/wiki/Touch_(Unix))

### Package Managers

- [apt](http://help.ubuntu.ru/wiki/apt) | [dnf](https://en.wikipedia.org/wiki/DNF_(software)) | [yum](https://fedoraproject.org/wiki/Yum/ru)
- [brew](https://brew.sh) | [linuxbrew](http://linuxbrew.sh)
- [npm](https://docs.npmjs.com)

### Software

- [curl](https://www.gitbook.com/book/bagder/everything-curl/details)
- [wget](https://www.gnu.org/software/wget/manual/wget.pdf)
- [clang](https://clang.llvm.org)
- [g++](https://gcc.gnu.org/onlinedocs/gcc-4.0.2/gcc/G_002b_002b-and-GCC.html)
- [make](https://en.wikipedia.org/wiki/Make_(software))
- [open](https://developer.apple.com/legacy/library/documentation/Darwin/Reference/ManPages/man1/open.1.html)
- [openssl](https://www.openssl.org)
- [nano](https://www.nano-editor.org)
- [tree](https://linux.die.net/man/1/tree)
- [vim](http://www.vim.org)

## Homework

1. Скачайте библиотеку *boost* с помощью утилиты **wget**. Адрес для скачивания `https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz`.
```bash
$ wget https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz 
```
2. Разархивируйте скачанный файл в директорию `~/boost_1_69_0`
```bash
$ tar -xf boost_1_69_0.tar.gz
$ rm -rf boost_1_69_0.tar.gz
$ cd boost_1_69_0
```
3. Подсчитайте количество файлов в директории `~/boost_1_69_0` **не включая** вложенные директории.
```bash
$ ls -f . | wc -l
21
```
4. Подсчитайте количество файлов в директории `~/boost_1_69_0` **включая** вложенные директории.
```bash
$ find . -type f | wc -l
61193
```
5. Подсчитайте количество заголовочных файлов, файлов с расширением `.cpp`, сколько остальных файлов (не заголовочных и не `.cpp`).
```bash
$ find . -type f -name '*.h' | wc -l
296
$ find . -type f -name '*.cpp' | wc -l
13774
$ find . -type f '!' -name '*.cpp' -a '!' -name '*.h' | wc -l
47123
```
6. Найдите полный пусть до файла `any.hpp` внутри библиотеки *boost*.
```bash
$ find . -type f -name 'any.hpp'
./boost/fusion/include/any.hpp
./boost/fusion/algorithm/query/any.hpp
./boost/fusion/algorithm/query/detail/any.hpp
./boost/spirit/home/support/algorithm/any.hpp
./boost/proto/detail/any.hpp
./boost/type_erasure/any.hpp
./boost/hana/fwd/any.hpp
./boost/hana/any.hpp
./boost/any.hpp
./boost/xpressive/detail/utility/any.hpp
```
7. Выведите в консоль все файлы, где упоминается последовательность `boost::asio`.
```bash
$ grep -lr 'boost::asio' .
...
...
./doc/html/process/reference.html
```
8. Скомпилирутйе *boost*. Можно воспользоваться [инструкцией](https://www.boost.org/doc/libs/1_61_0/more/getting_started/unix-variants.html#or-build-custom-binaries) или [ссылкой](https://codeyarns.com/2017/01/24/how-to-build-boost-on-linux/).
```bash
$ ./bootstrap.sh --prefix=boost_output
$ ./b2 install
```
9. Перенесите все скомпилированные на предыдущем шаге статические библиотеки в директорию `~/boost-libs`.
```bash
$ cd ..
$ mv boost_1_69_0/boost_output boost-libs

```
10. Подсчитайте сколько занимает дискового пространства каждый файл в этой директории.
```bash
$ tree -h
```
11. Найдите *топ10* самых "тяжёлых".
```bash
$ find .  -type f -exec du -sh {} 2>/dev/null + | sort -rh | head -n 10
27M	./lib/libboost_wave.a
 21M	./lib/libboost_log_setup.a
 19M	./lib/libboost_log.a
 16M	./lib/libboost_test_exec_monitor.a
 15M	./lib/libboost_unit_test_framework.a
9,2M	./lib/libboost_locale.a
8,7M	./lib/libboost_regex.a
8,2M	./lib/libboost_math_tr1f.a
7,9M	./lib/libboost_math_tr1.a
7,8M	./lib/libboost_math_tr1l.a
```

```
Copyright (c) 2015-2019 The ISC Authors
```
