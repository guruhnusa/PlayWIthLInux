

<!-- /TOC -->
[Perintah Dasar Linux](#Perintah-Dasar-Linux)
[Tipe FIle System](#Tipe_File_System)

<!-- /TOC -->

## Perintah Dasar Linux 
**Pengertian**

Pada dasarnya, `Linux` merupakan sistem operasi yang berbasiskan pada text (Text Bases) dalam sistem kerjanya. Bila ingin melakukan sesuatu terhadap komputer user bisa mengetikkan perintah-perintah yang kemudian dieksekusi oleh komputer. Tapi sekarang ini tampilan `GUI` (Graphic User Interface) Linux sudah bagus dan memudahkan user. 

Perintah-perintah yang diketikkan itu biasa disebut `Command Line`. Untuk perintah-perintah dasar, biasa disebut Basic Command Line. Kita dapat menuliskan perintah dasar linux di terminal atau konsole.

### Mengenal User Interface Terminal
  
**Prompt**
    
    nusa@localhost:~$
Keterangan:

`nusa` ,merupakan User yang sedang aktif.

`localhost` ,nama komputer

`~` ,direktori/folder yang sedang aktif, tanda ~ menunjukkan bahwa anda sedang berada di direktori /home

`$` ,meruapakan user biasa , `#` merupakan user root

**Absolute Paths dan Relative Paths**
  
- **Absoulte Patch**
    Absolute path berarti sebuah jalur dimulai dari `root` (`/ `) dan direktori yang berada dibawahnya.
    
        /home/nusa/desktop
    Dibawah root ( / ) terdapat direktori yang bernama home, dibawahnya terdapat direktori nusa, dan dibawahnya terdapat direktori desktop demikian seterusnya hingga sampai pada direktori yang dituju.
     
- **Relative Patch**
    
    Relative path berarti, sebuah jalur tidak dimulai dari root, tetapi dari posisi direktori terakhir.
    Contoh :
    Susunan direktori adalah /home/nusa/dokumen. Jika saat ini Anda berada pada direktori dokumen, maka untuk berpindah ke direktori picture tidak perlu menyertakan tanda / (slash).
    
**Format Penulisan Perintah Dasar**

    $ ls -a /home/nusa

`$` (Prompt) = Menujukan user biasa, # menunjukan user root

`ls` (Perintah) = adalah perintah yang ingin anda jalankan

`-a` (Option) = adalah pilihan yang bisa anda gunakan untuk menghasilkan kondisi tertentu dari suatu perintah.

`/home/nusa` (path) = adalah sesuatu yang akan diproses oleh perintah, misalnya nama file atau nama direktori.

Option bisa digunakan lebih dari satu perintah, Contoh penulisan perintah bisa anda lihat pada contoh dibawah ini.

- Penulisan perintah tampa argument

        ❯ ls
        Applications  Desktop  Documents  Downloads  Music  peda  Pictures     Public  Templates  Videos

- Penulisan perintah dengan menggunakan argument berupa `option`

        ❯ ls -l
        total 40
        drwxr-xr-x 2 nusa nusa 4096 Mar 20 02:00 Applications
        drwxr-xr-x 3 nusa nusa 4096 Mar 19 05:27 Desktop
        drwxr-xr-x 2 nusa nusa 4096 Mar 18 19:39 Documents
        drwxr-xr-x 2 nusa nusa 4096 Mar 20 02:18 Downloads
        drwxr-xr-x 2 nusa nusa 4096 Mar 18 19:39 Music
        drwxr-xr-x 4 nusa nusa 4096 Mar 19 05:25 peda
        drwxr-xr-x 2 nusa nusa 4096 Mar 18 20:02 Pictures
        drwxr-xr-x 2 nusa nusa 4096 Mar 18 19:39 Public
        drwxr-xr-x 2 nusa nusa 4096 Mar 18 19:39 Templates
        drwxr-xr-x 2 nusa nusa 4096 Mar 18 19:39 Videos

- Penulisan perintah dengan menggunakan argument berupa `path`
  
        ❯ ls /home
        lost+found  nusa


- Penulisan perintah dengan menggunakan argument berupa `option` dan `path` 
  
        ❯ ls -l /home
        total 20 
        drwx------  2 root root 16384 Mar 18 19:26 lost+found
        drwxr-xr-x 22 nusa nusa  4096 Mar 20 03:43 nusa

Pada saat menuliskan perintah, ada beberapa aturan yang harus kita ikuti,
antara lain:

● Case Sensitive (penggunaan huruf besar dan huruf kecil) 

Dalam menuliskan perintah harus diperhatikan apakah perintah tersebut menggunakan huruf besar atau huruf kecil.

● Penggunaan tanda baca dan spasi

Penggunaan titik `.`, koma `,`, slash `/` atau backslash `\`. Begitu juga dengan spasi. Karena bila terjadi kesalahan dalam penggunaan tanda baca dan spasi, perintah juga tidak bisa dijalankan.

● Ejaan kata dari perintah yang digunakan

Pastikan perintah anda sudah benar ejaan katanya. Perintah-perintah yang ada menggunakan bahasa inggris.

**Membatalkan Perintah**

Bisa mengetikkan `Ctrl+c` atau `Ctrl+z`. Maka perintah yang sedang diproses oleh system akan terhenti.

## File System di Linux

**Pengertian**

Filesystem mempunyai 2 maksud, yaitu pertama, suatu cara pengorganisasian file atau direktori di dalam suatu media penyimpanan. Kedua, adalah jenis file atau yang seperti “file extension”.

**File system Hierarki Standard**

`FHS` adalah seperangkat petunjuk untuk penempatan file dan direktori dibawah sistem operasi yang mirip `UNIX`. Tujuannya agar dapat mendukung interopabilitas aplikasi, program administrasi sistem, program pengembangan, skrip dan dapat menyatukan dokumentasi dari sistem ini.

Berikut beberapa definisi direktori menurut standar FHS :
    
`/(Root Folder )`

Menduduki posisi puncak di dalam hirarki, direktori ini dilambangkan dengan tanda slash `/` atau biasa disebut garis miring. Direktori ini membawahi semua direktori penting lainnya.
            
`/bin`

Direktori ini berisi perintah dasar yang dibutuhkan oleh system maupun user.

`/boot`

Berisi program dan data yang dibutuhkan pada saat melakukan proses booting (menjalankan) system.

`/dev`

Direktori tempat file device.

`/etc`

Berisi file konfigurasi system.

`home`

Direktori tempat menyimpan data user.

`/lib`

berisi file-file library dari aplikasi yang ada di
system. 

`/media`

berisi media yang bisa dibongkar pasang di komputer anda.

`/mnt`

Direktori tempat pengaitan sistem sementara.

`/opt`

berisi paket aplikasi tambahan yang kita install ke
dalam system.

`/proc`

Filesystem untuk menjalankan proses.

`/root`

Direktori user root

`/sbin`

Berisi program biner untuk menjalankan dan memperbaiki system.

`/temp`

Menyimpan file temp.
    
`/usr`

Berisi program-program yang bisa di akses oleh user, program source code.

`/var`

Menyimpan informasi proses, seperti system `history`,` access logs`, dan `error logs`.

Agar lebih mudah memahami lihat gambar.

![Gambar Hierarki](https://github.com/guruhnusa/PlayWIthLInux/blob/main/linux-filesystem.png)

### Tipe FileSystem
Jenis- jenis filesystem di linux

- `ext2`
  
  Jenis filesystem yang cepat dan stabil. Jenis ini adalah yang paling populer digunakan di Linux.
- `ext3`
  
  ext3 menggunakan konsep journaling. Yaitu sebuah cara untuk merekam data yang sudah ditulis ke disk, sehingga proses recovery dapat dilakukan dengan mudah jika terjadi suatu kesalahan.

- `ext4`
  
  Adalah singkatan dari Fourth Extended Filesystem, yakni file system ekstensi keempat yang merupakan salah satu sistem file journaling untuk Linux dan dikembangkan sebagai penerus file system ext3.
- `reiserf`
  
  Jenis lain dari journaling sistem yang diklaim lebih cepat dan menawarkan fitur keamanan yang lebih baik.
- `xfs`
  
  64bit journaling sistem yang dibuat oleh Silicon Graphics, Inc (SGI) yang digunakan pada varian Unix yang dikembangkan oleh SGI.
- `jfs`
 
 journaling sistem yang dibuat oleh IBM.

### Aturan Pernamaan File

`Linux` mendukung penamaan file sebanyak 256 karakter. Nama file boleh menggunakan huruf besar atau kecil.Nama file diperbolehkan juga menggunakantitik `.`, dash `-` dan underscore `_`

contoh:

    ini.nama.file
    nama_file
    .nama_file (diawali titik file akan tersembunyi)

## Fitur - Fitur yang Bisa Diandalkan

**`Man`**

Salah satu perintah yang bisa memberikan informasi lengkap (manual) mengenai perintah dasar yang anda ingin ketahui. Bahkan perintah ini juga menyediakan informasi mengenai dirinya sendiri.

Coba ketik perintah **man man** di terminal !

    MAN(1)                                   Manual pager utils                                   MAN(1)

    NAME
       man - an interface to the system reference manuals

    SYNOPSIS
       man [man options] [[section] page ...] ...
       man -k [apropos options] regexp ...
       man -K [man options] [section] term ...
       man -f [whatis options] page ...
       man -l [man options] file ...
       man -w|-W [man options] page ...

    DESCRIPTION
       man  is the system's manual pager.  Each page argument given to man is normally the name of a
       program, utility or function.  The manual page associated with each  of  these  arguments  is
       then  found and displayed.  A section, if provided, will direct man to look only in that sec‐
       tion of the manual.  The default action is to search in all of the available sections follow‐
       ing  a  pre-defined order (see DEFAULTS), and to show only the first page found, even if page
       exists in several sections.

       The table below shows the section numbers of the manual followed by the types of  pages  they
       contain.

       1   Executable programs or shell commands
       2   System calls (functions provided by the kernel)
       3   Library calls (functions within program libraries)
       4   Special files (usually found in /dev)
       5   File formats and conventions, e.g. /etc/passwd
       6   Games
       7   Miscellaneous   (including  macro  packages  and  conventions),  e.g.  man(7),  groff(7),
           man-pages(7)
       8   System administration commands (usually only for root)
       9   Kernel routines [Non standard]

       A manual page consists of several sections.
   
Coba lagi perintah lain `man cat`


    User                            Commands                                  CAT(1)

    NAME
       cat - concatenate files and print on the standard output
       
    SYNOPSIS
       cat [OPTION]... [FILE]...

    DESCRIPTION
        Concatenate FILE(s) to standard output.

       With no FILE, or when FILE is -, read standard input.

       -A, --show-all
              equivalent to -vET

       -b, --number-nonblank
              number nonempty output lines, overrides -n

       -e     equivalent to -vE

       -E, --show-ends
              display $ at end of each line

       -n, --number
              number all output lines

       -s, --squeeze-blank
              suppress repeated empty output lines

       -t     equivalent to -vT

       -T, --show-tabs
              display TAB characters as ^I

       -u     (ignored)

       -v, --show-nonprinting
              use ^ and M- notation, except for LFD and TAB

       --help display this help and exit

       --version
              output version information and exit

    EXAMPLES
       cat f - g
              Output f's contents, then standard input, then g's contents.

       cat    Copy standard input to standard output.

    AUTHOR
       Written by Torbjorn Granlund and Richard M. Stallman.

    REPORTING BUGS
       GNU coreutils online help: <https://www.gnu.org/software/coreutils/>
       Report any translation bugs to <https://translationproject.org/team/>
    COPYRIGHT
       Copyright  ©  2020 Free Software Foundation, Inc.  License GPLv3+: GNU GPL version 3 or later
       <https://gnu.org/licenses/gpl.html>.
       This is free software: you are free to change and redistribute it.  There is NO WARRANTY,  to
       the extent permitted by law.

    SEE ALSO
       tac(1)

       Full documentation <https://www.gnu.org/software/coreutils/cat>
       or available locally via: info '(coreutils) cat invocation'


**`Info`**

Selain mencari bantuan dari `man`, perintah info juga bisa digunakan untuk membaca dokumentasi dari suatu perintah. Tetapi tidak semua distro Linux menyediakan fungsi info ini.

    Next: dir invocation,  Up: Directory listing

    10.1 ‘ls’: List directory contents
    ==================================

    The ‘ls’ program lists information about files (of any type, including
    directories).  Options and file arguments can be intermixed arbitrarily,
    as usual.

    For non-option command-line arguments that are directories, by
    default ‘ls’ lists the contents of directories, not recursively, and
    omitting files with names beginning with ‘.’.  For other non-option
    arguments, by default ‘ls’ lists just the file name.  If no non-option
    argument is specified, ‘ls’ operates on the current directory, acting as
    if it had been invoked with a single argument of ‘.’.

    By default, the output is sorted alphabetically, according to the
    locale settings in effect.(1)  If standard output is a terminal, the
    output is in columns (sorted vertically) and control characters are
    output as question marks; otherwise, the output is listed one per line
    and control characters are output as-is.

    Because ‘ls’ is such a fundamental program, it has accumulated many
    options over the years.  They are described in the subsections below;
    within each section, options are listed alphabetically (ignoring case).
    The division of options into the subsections is not absolute, since some
    options affect more than one aspect of ‘ls’’s operation.

    Exit status:

        0 success
        1 minor problems  (e.g., failure to access a file or directory not
        specified as a command line argument.  This happens when listing a
        directory in which entries are actively being removed or renamed.)
        2 serious trouble (e.g., memory exhausted, invalid option, failure
        to access a file or directory specified as a command line argument
        or a directory loop)

    Also see *note Common options::.

    * Menu:

    * Which files are listed::
    * What information is listed::
    * Sorting the output::
    * General output formatting::
    * Formatting file timestamps::
    * Formatting the file names::

**`Whatis`**

Menampilkan informasi singkat mengenai suatu perintah.

    $ whatis cat
    cat (1)              - concatenate files and print on the standard output

**`Apropos`**

Berfungsi untuk menampilkan informasi singkat perintah yang hanya anda ketahui sebagain atau anda ingin menampilkan perintah yang berhubungan dengan sesuatu

    $ apropos cd
    
    apt-cdrom (8)        - APT CD-ROM management utility
    dhcpcd (8)           - a DHCP client
    dhcpcd-run-hooks (8) - DHCP client configuration script
    dhcpcd.conf (5)      - dhcpcd configuration file
    hex2hcd (1)          - Broadcom Bluetooth firmware converter
    hipercdecode (1)     - Decode a HIPERC stream into human readable form.
    libOpenCL (7)        - OCL-ICD implementation of OpenCL ICD loader
    libOpenCL.so (7)     - OCL-ICD implementation of OpenCL ICD loader
    mcdiff (1)           - Visual shell for Unix-like systems.
    ncdu (1)             - NCurses Disk Usage
    pbmtomatrixorbital (1) - convert a PBM image to a Matrix Orbital LCD image
    pcdindex (1)         - renamed to pcdovtoppm
    pcdovtoppm (1)       - create index image for a photo CD
    rsyncd.conf (5)      - configuration file for rsync in daemon mode
    sbigtopgm (1)        - convert an SBIG CCDOPS file to PGM

**`--help`**

Bantuan yang satu ini berupa option yang bisa kita tambahkan ke perintah dasar yang kita inginkan.

    $ sudo --help
    sudo - execute a command as another user

    usage: sudo -h | -K | -k | -V
    usage: sudo -v [-ABknS] [-g group] [-h host] [-p prompt] [-u user]
    usage: sudo -l [-ABknS] [-g group] [-h host] [-p prompt] [-U user] [-u user] [command]
    usage: sudo [-ABbEHknPS] [-r role] [-t type] [-C num] [-D directory] [-g group] [-h host] [-p prompt]
                [-R directory] [-T timeout] [-u user] [VAR=value] [-i|-s] [<command>]
    usage: sudo -e [-ABknS] [-r role] [-t type] [-C num] [-D directory] [-g group] [-h host] [-p prompt]
                [-R directory] [-T timeout] [-u user] file ...

    Options:
    -A, --askpass                 use a helper program for password prompting
    -b, --background              run command in the background
    -B, --bell                    ring bell when prompting
    -C, --close-from=num          close all file descriptors >= num
    -D, --chdir=directory         change the working directory before running command
    -E, --preserve-env            preserve user environment when running command
        --preserve-env=list       preserve specific environment variables
    -e, --edit                    edit files instead of running a command
    -g, --group=group             run command as the specified group name or ID
    -H, --set-home                set HOME variable to target user's home dir
    -h, --help                    display help message and exit
    -h, --host=host               run command on host (if supported by plugin)
    -i, --login                   run login shell as the target user; a command may also be specified
    -K, --remove-timestamp        remove timestamp file completely
    -k, --reset-timestamp         invalidate timestamp file
    -l, --list                    list user's privileges or check a specific command; use twice for
                                    longer format

## Error

Pada saat mempelajari perintah dasar, mungkin anda akan mendapatkan error. Contoh- contoh error

**`Command Not Found`**

Mungkin terjadi kesalahan penulisan atau perintah yang anda ketikkan memang tidak ada. Karena bila mendapatkan error ini berarti perintah tidak dikenali sebagai perintah Linux.

    $ not
    zsh: command not found: not

**`Invalid Option`**

Error ini terjadi bila anda memberikan option yang salah atau tidak ada pada perintah yang anda ketikkan.

    $ ls -y
    ls: invalid option -- 'y'
    Try 'ls --help' for more information.

**`No Such File Or Dictionary  `**

Periksa kembali apakah file atau direktori yang anda maksud sudah benar. Karena bila file atau direktori tidak ada, maka akan tampil pesan error No such file or directory.

    $ ls
    Applications  Desktop  Documents  Downloads  Music  peda  Pictures  Public  Templates  Videos
    $ cd destop
    cd: no such file or directory: destop

**`Missing Operan`**

Ada perintah yang tidak bisa berdiri sendiri, perintah ini baru berjalan bila ada argumennya. Bila argumen tidak ada akan muncul error

    $ rmdir
    rmdir: missing operand
    Try 'rmdir --help' for more information.

## Play with Command Linux

### Perintah yang berhubungan dengan direktory

```ls```

Menampilkan isi dari suatu direktori. Perintah ini bisa berdiri sendiri ataupun dijalankan dengan argument.

|   Options     |        Fungsi                                                                          |
|   -----       |        -----                                                                           |
|-a             | menampilkan semua file dan folder, termasuk file dan folder yang tersembunyi           |
|-A             |sama dengan -a, tetapi tidak menampilkan direktori . dan ..                             |
|-C             |menampilkan direktori dengan output berbentuk kolom                                     |
|-d             |Hanya menampilkan directori saja|
|-f             |menampilkan isi direktori tanpa diurutkan                                               |
|-l             |menampilkan isi direktori secara lengkap, mulai dari hak akses, owner, group dan tanggal file atau direktori tersebut dibuat|
|-1             |menampilkan isi direktori dengan format satu direktori per baris                        |

```dir```

Memiliki fungsi yang sama dengan perintah ```ls```, yaitu menampilkan ```ls``` direktori. Anda bisa membuka manual dari perintah ```dir```. Pemberian option dan argument sama dengan perintah ```ls```.

    $ dir
    Applications  Desktop  Documents  Downloads  Music  peda  Pictures  Public  Templates  Videos

```pwd (print working directory)```

Menampilkan direktori yang sedang aktif (curent directory). Perintah ini tidak mempunyai option dan argumen.

    $ pwd
    /home/nusa

```mkdir```

Perintah untuk membuat direktori. Untuk mencoba perintah ini ikuti  latihan dibawah ini. 

    $ ls
    home
    $ mkdir home2
    $ ls
    home  home2

```cd```

Perintah untuk berpindah direktori aktif.

    $ ls
    Applications  Desktop  Documents  Downloads  Music  peda  Pictures  Public  Templates  Videos
    $ cd Documents
    ~/Documents $

### Perintah Dasar yang Berhubungan dengan Manajemen File

```touch```

Perintah untuk mengganti waktu pembuatan suatu file. Tetapi bila file yang anda ketikkan belum ada maka secara otomatis file tersebut akan dibuat.

```cat```

Perintah ```cat```, digunakan untuk menampilkan isi file. Biasanya file yang ditampilkan dengan perintah ini adalah file yang bertipe teks. Dan yang pasti bukan file kosong.

```more```

Perintah ini bisa digunakan untuk menampilkan isi file teks dengan tampilan perlayar. 

```less```

Memiliki fungsi yang sama dengan more, tetapi anda bisa menampilkan tampilan layar terdahulu dengan menggunakan tombol panah atas atau Page Up.

```cp```

Berfungsi untuk mengcopy atau menduplikat file dan direktori.\

     cp nama_file_asal nama_file_hasil

```mv```

Perintah untuk memindahkan file dan direktori. Perintah ini juga bisa digunakan untuk merename (mengganti) nama file atau direktori.

    mv nama_file nama_file_baru
    mv nama_file direktori_tujuan

```rm```

Untuk menghapus (remove) file atau direktori.

    rm nama_file

```find```

Mencari suatu file dalam direktori tertentu. Anda bisa melakukan pencarian berdasarkan nama, ukuran, waktu pembuatan file dsb. dengan memberikan option yang anda inginkan.

    find nama_file option

```which```

Menampilkan lokasi perintah dasar yang anda cari. Perintah ini juga bisa digunakan untuk mencari file program yang bisa dieksekusi.

    which nama_file

```whereis```

Hampir sama dengan ```which```, menampilkan lokasi perintah dasar, tetapi dengan whereis lokasi file binary, source dan manual juga ditampilkan

    whereis nama_file

```tar```

Untuk mengextract (memekarkan) file yang di kompres dengan menggunakan perintah teks di linux

    tar option nama_file

Dimana parameter ```x``` adalah untuk memekarkan file, ```z``` untuk menyaring file hasil compresian dari format gzip , ```v``` untuk menampilkan proses sehingga user dapat mengetahui proses yang terjadi, dan ```f``` adalah ada namafile yang harus diikuti 

```unzip```

Perintah ini digunakan untuk mengekstrak file yang di kompress yang berekstensi .zip

    unzip nama_file

### Perintah yang berhubungan dengan Pemrosesan String

String adalah serangkaian karakter. Linux menyediakan beberapa perintah yang dapat digunakan berkaitan dengan proses string, seperti mencari karakter, pengurutan dan lainnya.

```head```

Perintah ini digunakan untuk menampilkan beberapa baris awal dari isi file. Misalnya ingin menampilkan 8 baris pertama saja. Secara default yang ditampilkan adalah sepuluh (10) baris awal file.

    $ head nama_file

```tail```

Menampilkan isi akhir file. Untuk menampilkan beberapa baris terakhir dari isi file gunakan perintah ```tail```. Secara default yang ditampilkan adalah sepuluh baris akhir file.

    $ tail nama_file

```grep```

Mencari karakter atau kata yang diinginkan dari sebuah file yang terdiri dari banyak kalimat. Perintah yang digunakan adalah ```grep```. Dengan perintah ini pencarian lebih mudah dilakukan.

    $ grep nama_kata nama_file

```wc```

Perintah untuk menampilkan jumlah baris, jumlah kata dan ukuran dari sebuah file.

    $ wc nama_file

```sort```

Menampilkan isi file teks secara urut. Gunakan perintah ini.

    $ sort nama_file

### Perintah-perintah yang berhubungan dengan informasi system

```uname```

Printah ini akan menampilkan informasi system komputer anda antara lain tipe mesin komputer, hostname, nama dan versi sistem operasi dan tipe prosesor.

    $ uname option

|Option|Fungsi|
|------|------|
|-a, -all|menampilkan semua informasi|
|-m, -machine|menampilkan tipe mesin|
|-n, -nodename|menampilkan hostname|
|-r, -release|menampilkan rilis dari kernel sistem operasi|
|-s, -o|menampilkan nama sistem operasi|
|-p, -prosessor|menampilkan nama prosessor|
|-v|menampilkan versi sistem operasi

contoh:

    $ uname -a
    Linux nusa 5.16.12-051612-generic #202203021142 SMP PREEMPT Wed Mar 2 12:19:24 UTC 2022 x86_64 GNU/Linux

```date```

Perintah untuk menampilkan tanggal dan waktu system.

    $ date 
    Min 20 Mar 2022 06:42:16  WIB

```cal```

Untuk menampilkan kalender.

```df```

Perintah untuk menampilkan penggunaan space filesystem dari hardisk anda.

    $ df
    Filesystem     1K-blocks      Used Available Use% Mounted on
    udev             3895468         0   3895468   0% /dev
    tmpfs             791324      1512    789812   1% /run
    /dev/nvme0n1p4  34966168  10370780  22787004  32% /
    tmpfs               5120         4      5116   1% /run/lock
    tmpfs            1582640     19824   1562816   2% /dev/shm
    /dev/nvme0n1p7    510984      6100    504884   2% /boot/efi
    /dev/nvme0n1p5  42950324   1735556  39000816   5% /home
    cgroup           3956616         0   3956616   0% /sys/fs/cgroup
    tmpfs             791320        12    791308   1% /run/user/1000
    /dev/nvme0n1p2 157946876 110092460  47854416  70% /media/nusa/Acer
    /dev/nvme0n1p3 258153468 138431520 119721948  54% /media/nusa/New Volume

```du```

Perintah untuk menampilkan ukuran direktori atau file.

    $ du
    12      ./.oh-my-zsh/plugins/ros
    12      ./.oh-my-zsh/plugins/kops
    12      ./.oh-my-zsh/plugins/fancy-ctrl-z
    24      ./.oh-my-zsh/plugins/genpass
    12      ./.oh-my-zsh/plugins/cpanm
    12      ./.oh-my-zsh/plugins/octozen
    1092    ./.oh-my-zsh/plugins/emoji
    20      ./.oh-my-zsh/plugins/taskwarrior
    16      ./.oh-my-zsh/plugins/pylint
    12      ./.oh-my-zsh/plugins/sfffe
    24      ./.oh-my-zsh/plugins/juju
    12      ./.oh-my-zsh/plugins/vundle
    12      ./.oh-my-zsh/plugins/marked2
    12      ./.oh-my-zsh/plugins/codeclimate

```uptime```

Untuk mengetahui informasi tentang lama sistem berjalan setelah terakhir reboot atau mati. 

    $ uptime
    18:47:15 up 11:16,  1 user,  load average: 2,53, 1,61, 1,56

```hostname```

Perintah untuk menampilkan nama dari komputer (hostname).

```free```

Perintah untuk menampilkan penggunaan memori.

    $ free
    total        used        free      shared  buff/cache   available
    Mem:         7913232     3399984      278276     1135684     4234972     3048772
    Swap:        4108280         256     4108024

```ps```

Perintah ```ps``` merupakan akronim dari “process status”. Akan memberikan informasi status proses pada sistem kita. 

    $ ps
    PID TTY          TIME CMD
    19231 pts/0    00:00:00 zsh
    19237 pts/0    00:00:00 zsh
    19265 pts/0    00:00:00 zsh
    19266 pts/0    00:00:00 zsh
    19268 pts/0    00:00:00 gitstatusd-linu
    25704 pts/0    00:00:00 ps

`pstree`

Perintah ini fungsinya sama dengan perintah `ps`, tetapi ditampilkan dalam bentuk pohon. Sebenarnya di Linux tidak ada proses yang berdiri sendiri.

contoh:

    $ pstree
    init─┬─NetworkManager───2*[{NetworkManager}]
     ├─acpid
     ├─appimaged───{appimaged}
     ├─avahi-daemon───avahi-daemon
     ├─bluetoothd
     ├─cupsd
     ├─2*[dbus-daemon]
     ├─dbus-launch
     ├─dconf-service───2*[{dconf-service}]
     ├─dhcpcd
     ├─dnsmasq
     ├─dockerd─┬─containerd───18*[{containerd}]
     │         └─18*[{dockerd}]
     ├─elogind-daemon
     ├─gamemoded───{gamemoded}
     ├─gnome-keyring-d───3*[{gnome-keyring-d}]
     ├─haveged
     ├─irqbalance───{irqbalance}
     ├─kactivitymanage───5*[{kactivitymanage}]
     ├─kdeinit5───klauncher───2*[{klauncher}]
     ├─kglobalaccel5───2*[{kglobalaccel5}]
     ├─2*[kioslave5]
     ├─kscreen_backend───2*[{kscreen_backend}]
     ├─ksystemstats───{ksystemstats}
     ├─kwin_x11───31*[{kwin_x11}]
     ├─2*[mount.ntfs]
     ├─obexd
     ├─polkitd───2*[{polkitd}]
     ├─preload
     ├─pulseaudio─┬─gsettings-helpe───3*[{gsettings-helpe}]
     │            └─2*[{pulseaudio}]
     ├─rngd
     ├─sddm─┬─Xorg───22*[{Xorg}]
     │      ├─sddm-helper───startplasma-x11─┬─plasma_session─┬─autostart-latte─┬─latte-dock─┬─code─┬─code───code───17*[{co+
     │      │                               │                │                 │            │      ├─code───code───code───+
     │      │                               │                │                 │            │      ├─code───4*[{code}]
     │      │                               │                │                 │            │      ├─code───25*[{code}]
     │      │                               │                │                 │            │      ├─code───12*[{code}]
     │      │                               │                │                 │            │      ├─code─┬─code───11*[{co+
     │      │                               │                │                 │            │      │      ├─code───13*[{co+
     │      │                               │                │                 │            │      │      └─19*[{code}]
     │      │                               │                │                 │            │      └─33*[{code}]
     │      │                               │                │                 │            ├─firejail───firejail───firefo+
     │      │                               │                │                 │            ├─station─┬─zsh───pstree
     │      │                               │                │                 │            │         └─15*[{station}]
     │      │                               │                │                 │            └─30*[{latte-dock}]
     │      │                               │                │                 └─plasmashell───18*[{plasmashell}]
     │      │                               │                ├─gmenudbusmenupr───2*[{gmenudbusmenupr}]
     │      │                               │                ├─kaccess───2*[{kaccess}]
     │      │                               │                ├─kdeconnectd───3*[{kdeconnectd}]
     │      │                               │                ├─kded5───6*[{kded5}]
     │      │                               │                ├─ksmserver───2*[{ksmserver}]
     │      │                               │                ├─org_kde_powerde───4*[{org_kde_powerde}]
     │      │                               │                ├─plasma-hud───10*[{plasma-hud}]
     │      │                               │                ├─polkit-kde-auth───14*[{polkit-kde-auth}]
     │      │                               │                ├─sh───AppRun───{AppRun}
     │      │                               │                ├─xembedsniproxy───2*[{xembedsniproxy}]
     │      │                               │                └─{plasma_session}
     │      │                               ├─ssh-agent
     │      │                               └─{startplasma-x11}
     │      └─{sddm}
     ├─start_kdeinit
     ├─2*[supervise-daemo───agetty]
     ├─udevd
     ├─udisksd───4*[{udisksd}]
     ├─upowerd───2*[{upowerd}]
     ├─uuidd
     ├─wpa_supplicant
     ├─xsettingsd
     ├─zsh───gitstatusd-linu───24*[{gitstatusd-linu}]
     └─2*[zsh]

### Perintah dasar yang berhubungan dengan User

Di Linux ada dua tipe user yang penting untuk diketahui. Kedua user itu adalah user biasa dan user root.

- user root     : user yang memiliki hak sebagi administrator, biasa juga disebut “super user”. User root yang akan mengelola dan mengkonfigurasi komputer.

- user biasa    : user yang tidak memiliki hak akses sebagai administrator User ini digunakan untuk melakukan kegiatan sehari-hari itu misalnya mengetik, browsing internet dan kegiatan lain yang tidak membutuhkan hak root.

`who`

Perintah ini digunakan untuk menampilkan user yang sedang login saat ini. Informasi yang tampak adalah nama user, di terminal (pts) berapa user tersebut berada dan waktu loginnya.

`whoami`

Bila anda ingin menampilkan user yang sedang aktif anda bisa menggunakan perintah ini.

`id`

Gunakan perintah `id` untuk menampilkan identitas user. User yang ingin ditampilkan identitasnya adalah user yang sedang aktif (login).

`tty`

untuk menampilkan nama terminal dimana saat ini anda berada gunakan perintah `tty` ini.

`su`

Anda dapat berpindah dari user yang sedang aktif menjadi user lain tanpa harus melakukan logout. Gunakan perintah `su`.

`adduser`

Untuk membuat user baru digunakan perintah `adduser` atau `useradd`. Perintah ini harus dijalankan melalui user root. Login atau bergantilah dari user biasa ke user root.

`visudo atau sudo`

Untuk menggunakan hak root, digunakan perintah `sudo`. Tetapi sebelum menggunakan perintah `sudo`, user tersebut sudah harus masuk dalam daftar pengguna `sudo`

`passwd`

Setelah membuat user baru dengan perintah useradd, kita perlu membuatkan password. Gunakan perintah `passwd`.

`usedel`

User yang sudah dibuat juga dapat dihapus. Gunakan perintah userdel untuk menghapus user.

`groupadd`

Perintah ini digunakan untuk membuat group. Group yang dimaksud disini adalah sekelompok user yang saling bergabung dan mempunyai ketentuan tersendiri di kelompoknya.

`groupdel`

Group yang ada juga dapat dihapus. Gunakan perintah `groupdel`.

`Redirection`

Dengan mempelajari bagian Redirection ini, anda akan memahami perintah tersebut. Dalam UNIX/Linux, terdapat istilah standard input, standard output dan standard error.

- **Standar input**
  
  Masukan atau input standar dari suatu perintah atau program.
- **standar Output**
  
  Keluaran atau output standar dari suatu perintah atau program.
- **Standar Error**
  
  keluaran atau output standar jika pada perintah atau program terjadi kesalahan.

Simbol yang digunakan untuk pembelokkan ini adalah :

`>` , untuk output.

`<` , untuk input.

`>> `, penambahan output.


`pipe`

Pipe `|` atau pipeline atau pipa dalam bahasa Indonesia digunakan untuk komunikasi antar proses (perintah). Dengan `pipe` Anda dapat menghubungkan sebuah perintah yang menghasilkan sebuah output dengan perintah lain yang akan memproses output tersebut. 

`clear`

Untuk membersihkan layar terminal.

## Izin Akses FIle

Setiap file Linux memiliki status izin akses (file permission). Maksudnya setiap file memiliki informasi untuk mengatur siapa saja yang berhak untuk membaca, menjalankan atau mengubah file tersebut. Tujuannya adalah untuk menjaga privasi file, keamanan serta integritas sistem agar tidak terganggu

**Melihat izin akses file**

Untuk mengetahui izin akses suatu file dapat digunakan perintah `ls` dengan option `-l`

    $ ls -l
    total 40
    drwxr-xr-x 2 nusa nusa 4096 Mar 20 02:00 Applications
    drwxr-xr-x 4 nusa nusa 4096 Mar 20 08:13 Desktop
    drwxr-xr-x 2 nusa nusa 4096 Mar 18 19:39 Documents
    drwxr-xr-x 2 nusa nusa 4096 Mar 20 17:25 Downloads
    drwxr-xr-x 2 nusa nusa 4096 Mar 18 19:39 Music
    ----------------------------------------------------
    drwxr-xr-x  : Izin akses file
    2           : Link file
    nusa        : Pemilik file
    nusa        : Nama group pemilik file
    4096        : ukuran file
    Mar 20 02:00: bulan,tanggal,jam pembuatan file
    Desktop     : Nama file
    ----------------------------------------------------
    Izin akses file ada tiga, yaitu :
    r : read (membaca)
    w : write (menulis)
    x : execute (menjalankan)

**Mengubah izin akses file**

Untuk mengubahnya digunakan perintah `chmod`. Ada 2 macam mode mengubah Izin Akses File, yaitu Symbolic mode dan Octal mode.

**Kepemilikan file dan group**

Untuk keamanan dan privasi, setiap file di Linux memiliki indentitas kepemilikan (ownership). Dengan adanya identitas ini maka akan jelas siapa pemilik file tersebut, siapa yang berhak membaca, menulis atau menjalankannya.

**Mengubah kepemilikan file & direktori**

Pemilik sebuah fle atau direktori dapat diganti menjadi milik user yang lain. Untuk mengganti digunakan perintah `chown`

    $ chown option pemilik_baru nama_file/direktori

**Mengubah kepemilikan group**

Untuk mengubah pemilik group digunakan perintah `chgrp`. Perintah ini harus dilakukan melalui root dan group pengganti sudah harus ada dalam sistem

    $ chgrp option group_pengganti nama_file/direktori

## Konsep Kernel dan Shell

### Kernel

Kernel adalah jantung dari sebuah sistem operasi karena kernel lah yang mengatur semua proses seperti manajemen memori, proses input/output, termasuk mengatur bekerjanya device. Secara teknis Linux hanyalah sebuah kernel. Untuk mengikuti perkembangan kernel, dapat mengunjungi http://kernel.og

Untuk mengetahui versi kernel yang digunakan pada distro, ketikkan perintah `uname`

    $ uname -r
    5.16.12-051612-generic

### Shell

`Shell` adalah program penerjemah perintah yang menjembatani user dengan sistem operasi. Pada umumnya shell menyediakan prompt sebagai user interface, yaitu tempat dimana user mengetikkan perintah- perintah yang diinginkan.

**Jenis- jenis shell di linux**

- `ash`
  
  The Almquist shell. Shell ini merupakan versi ringan dari Berkeley UNIX shell. Shell ini tidak menyertakan banyak fitur. ash dibuat oleh Kenneth Almquist.
- `bash`
  
  Bash menyertakan fitur yang ada pada shell lain. bash juga merupakan default shell dari banyak distro
- `ksh`
  
  Korn Shell, dibuat oleh David Korn di AT&T Bell Labs.
- `tcsh`
  
  Merupakan pengembangan dari C shell (csh) dan menggunakan konsep open source. csh dibuat oleh Bill Joy.
- `zsh`
  
   Merupakan salah satu clone dari sh shell.

**Mengetahui shell yang tersedia di sistem**

Untuk mengetahui shell yang ada di sistem, digunakan perintah `chsh` dengan option `-l`

**Mengganti shell**

mengganti shell yang aktif dengan shell yang lain? Gunakan perintah `chsh` dengan option `-s`

## Bash Script

-- COMING SOON -- 
