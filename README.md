# Amazon Linux 2023 Personnal repository

## To Use binary packages from this repo:

### Configure Repo
edit file /etc/yum.repo/amazonlinux-nagios.repo

```
[amazonlinux-nagios]
name=Nagios for Amazon Linux 2023
baseurl=https://raw.githubusercontent.com/csabattier/amazonlinux/main/packages
enabled=1
repo_gpgcheck=0
type=rpm
gpgcheck=0
```

### Install Package

```
dnf install -y nrpe
```



## To build NRPE for Amazon Linux 2023 from source: 

### Run container of Amazon Linux 2023 if you dont have access to an ec2 instance:
```
docker run -it public.ecr.aws/amazonlinux/amazonlinux:2023 /bin/bash
```
### Install Dependencies:

```
dnf install -y adobe-mappings-cmap adobe-mappings-cmap-deprecated adobe-mappings-pdf alternatives amazon-linux-repo-cdn amazon-rpm-config annobin-docs annobin-plugin-gcc audit-libs autoconf automake avahi-libs basesystem bash bind-libs bind-license bind-utils binutils brotli brotli-devel bzip2 bzip2-devel bzip2-libs ca-certificates cairo cairo-gobject checkpolicy cmake-filesystem coreutils-single cpio cpp cracklib crypto-policies cryptsetup-libs cups-libs curl-minimal cyrus-sasl cyrus-sasl-devel cyrus-sasl-lib dbus dbus-broker dbus-common dbus-libs device-mapper device-mapper-libs diffutils dnf dnf-data dnf-plugins-core dnf-utils doxygen dwz ed efi-srpm-macros elfutils elfutils-debuginfod-client elfutils-debuginfod-client-devel elfutils-default-yama-scope elfutils-devel elfutils-libelf elfutils-libelf-devel elfutils-libs emacs-filesystem expat file file-libs filesystem findutils fontconfig fontconfig-devel fonts-filesystem fonts-srpm-macros fping freetype freetype-devel fribidi fstrm gawk gc gcc gcc-c++ gd gdb-minimal gdbm-libs gd-devel gdk-pixbuf2 gettext gettext-libs ghc-srpm-macros glib2 glib2-devel glibc glibc-common glibc-devel glibc-gconv-extra glibc-headers-x86 glibc-minimal-langpack gmp gnupg2-minimal gnutls google-droid-sans-fonts google-noto-fonts-common google-noto-sans-vf-fonts go-srpm-macros gperf gpgme gpm-libs graphite2 graphite2-devel graphviz grep groff-base guile22 gzip harfbuzz harfbuzz-devel harfbuzz-icu hostname info iputils jansson jbig2dec-libs jbigkit-libs json-c kernel-headers kernel-srpm-macros keyutils-libs kmod-libs krb5-libs langpacks-core-font-en lcms2 less libacl libarchive libargon2 libassuan libattr libblkid libblkid-devel libbrotli libcap libcap-ng libcbor libcom_err libcomps libcurl-minimal libdatrie libdb libdbi libdbi-devel libdnf libeconf libedit libevent libfdisk libffi libffi-devel libfido2 libfontenc libgcc libgcrypt libgomp libgpg-error libgs libICE libicu libicu-devel libidn2 libijs libjpeg-turbo libjpeg-turbo-devel libldb libmaxminddb libmodulemd libmount libmount-devel libmpc libnghttp2 libpaper libpkgconf libpng libpng-devel libpq libpq-devel libpwquality librepo libreport-filesystem librsvg2 libseccomp libselinux libselinux-devel libselinux-utils libsemanage libsepol libsepol-devel libsigsegv libSM libsmartcols libsmbclient libsolv libstdc++ libstdc++-devel libtalloc libtasn1 libtdb libtevent libtextstyle libthai libtiff libtiff-devel libtirpc libtool libtool-ltdl libunistring libutempter libuuid libuv libverto libwbclient libwebp libwebp-devel libX11 libX11-common libX11-devel libX11-xcb libXau libXau-devel libXaw libxcb libxcb-devel libxcrypt libxcrypt-devel libXext libXft libxkbcommon libxml2 libxml2-devel libXmu libXpm libXpm-devel libXrender libXt libyaml libzstd libzstd-devel lmdb-libs lm_sensors-devel lm_sensors-libs logrotate lua-libs lua-srpm-macros lz4-libs m4 mailcap make mariadb-connector-c mariadb-connector-c-config mariadb-connector-c-devel mkfontscale mpfr ncurses ncurses-base ncurses-libs net-snmp-agent-libs net-snmp-devel net-snmp-libs net-snmp-perl net-snmp-utils nettle npth ocaml-srpm-macros openblas-srpm-macros openjpeg2 openldap openldap-devel openssh openssh-clients openssl openssl-devel openssl-libs p11-kit p11-kit-trust package-notes-srpm-macros pam pango patch pcre2 pcre2-devel pcre2-syntax pcre2-utf16 pcre2-utf32 perl perl-Algorithm-Diff perl-Archive-Tar perl-Archive-Zip perl-Attribute-Handlers perl-autodie perl-AutoLoader perl-AutoSplit perl-autouse perl-B perl-base perl-Benchmark perl-bignum perl-blib perl-Carp perl-Class-Struct perl-Clone perl-Compress-Bzip2 perl-Compress-Raw-Bzip2 perl-Compress-Raw-Lzma perl-Compress-Raw-Zlib perl-Config-Extensions perl-Config-Perl-V perl-constant perl-CPAN perl-CPAN-DistnameInfo perl-CPAN-Meta perl-CPAN-Meta-Requirements perl-CPAN-Meta-YAML perl-Crypt-RC4 perl-Data-Dumper perl-Data-OptList perl-Data-Section perl-Date-Simple perl-DB_File perl-DBM_Filter perl-debugger perl-deprecate perl-devel perl-Devel-Peek perl-Devel-PPPort perl-Devel-SelfStubber perl-Devel-Size perl-diagnostics perl-Digest perl-Digest-MD5 perl-Digest-SHA perl-Digest-SHA1 perl-DirHandle perl-doc perl-Dumpvalue perl-DynaLoader perl-Encode perl-Encode-devel perl-Encode-Locale perl-encoding perl-encoding-warnings perl-English perl-Env perl-Errno perl-experimental perl-Exporter perl-ExtUtils-CBuilder perl-ExtUtils-Command perl-ExtUtils-Constant perl-ExtUtils-Embed perl-ExtUtils-Install perl-ExtUtils-MakeMaker perl-ExtUtils-Manifest perl-ExtUtils-Miniperl perl-ExtUtils-MM-Utils perl-ExtUtils-ParseXS perl-Fcntl perl-Fedora-VSP perl-fields perl-File-Basename perl-FileCache perl-File-Compare perl-File-Copy perl-File-DosGlob perl-File-Fetch perl-File-Find perl-FileHandle perl-File-HomeDir perl-File-Path perl-File-stat perl-File-Temp perl-filetest perl-File-Which perl-Filter perl-Filter-Simple perl-FindBin perl-GDBM_File perl-generators perl-Getopt-Long perl-Getopt-Std perl-Hash-Util perl-Hash-Util-FieldHash perl-HTML-Parser perl-HTML-Tagset perl-HTTP-Date perl-HTTP-Message perl-HTTP-Tiny perl-I18N-Collate perl-I18N-Langinfo perl-I18N-LangTags perl-if perl-Importer perl-inc-latest perl-interpreter perl-IO perl-IO-Compress perl-IO-Compress-Lzma perl-IO-HTML perl-IO-Socket-IP perl-IO-Socket-SSL perl-IO-Zlib perl-IPC-Cmd perl-IPC-Open3 perl-IPC-System-Simple perl-IPC-SysV perl-JSON perl-JSON-PP perl-less perl-lib perl-libnet perl-libnetcfg perl-libs perl-locale perl-Locale-Maketext perl-Locale-Maketext-Simple perl-local-lib perl-LWP-MediaTypes perl-macros perl-Mail-Sender perl-Math-BigInt perl-Math-BigInt-FastCalc perl-Math-BigRat perl-Math-Complex perl-Memoize perl-meta-notation perl-MIME-Base64 perl-MIME-Charset perl-Module-Build perl-Module-CoreList perl-Module-CoreList-tools perl-Module-Load perl-Module-Load-Conditional perl-Module-Loaded perl-Module-Metadata perl-Module-Signature perl-Mozilla-CA perl-mro perl-MRO-Compat perl-NDBM_File perl-Net perl-Net-Ping perl-Net-SSLeay perl-NEXT perl-Object-HashBase perl-ODBM_File perl-Opcode perl-open perl-overload perl-overloading perl-Package-Generator perl-Params-Check perl-Params-Util perl-parent perl-PathTools perl-perlfaq perl-PerlIO-via-QuotedPrint perl-Perl-OSType perl-ph perl-Pod-Checker perl-Pod-Escapes perl-Pod-Functions perl-Pod-Html perl-podlators perl-Pod-Perldoc perl-Pod-Simple perl-Pod-Usage perl-POSIX perl-Safe perl-Scalar-List-Utils perl-Search-Dict perl-SelectSaver perl-SelfLoader perl-sigtrap perl-Socket perl-Software-License perl-sort perl-srpm-macros perl-Storable perl-Sub-Exporter perl-Sub-Install perl-subs perl-Symbol perl-Sys-Hostname perl-Sys-Syslog perl-Term-ANSIColor perl-Term-Cap perl-Term-Complete perl-TermReadKey perl-Term-ReadLine perl-Term-Size-Any perl-Term-Size-Perl perl-Term-Table perl-Test perl-Test-Harness perl-Test-Simple perl-Text-Abbrev perl-Text-Balanced perl-Text-Diff perl-Text-Glob perl-Text-ParseWords perl-Text-Tabs+Wrap perl-Text-Template perl-Thread perl-Thread-Queue perl-threads perl-Thread-Semaphore perl-threads-shared perl-Tie perl-Tie-File perl-Tie-Memoize perl-Tie-RefHash perl-Time perl-TimeDate perl-Time-HiRes perl-Time-Local perl-Time-Piece perl-Unicode-Collate perl-Unicode-LineBreak perl-Unicode-Normalize perl-Unicode-UCD perl-URI perl-User-pwent perl-utils perl-vars perl-version perl-vmsish pixman pkgconf pkgconf-m4 pkgconf-pkg-config policycoreutils policycoreutils-devel policycoreutils-python-utils popt popt-devel postfix procps-ng protobuf-c python3 python3-audit python3-dateutil python3-dbus python3-distro python3-dnf python3-dnf-plugins-core python3-gpg python3-hawkey python3-libcomps python3-libdnf python3-libs python3-libselinux python3-libsemanage python3-pip-wheel python3-policycoreutils python3-pyparsing python3-rpm python3-setools python3-setuptools python3-setuptools-wheel python3-six python-srpm-macros qrencode-libs readline rpm rpm-build rpm-build-libs rpm-devel rpm-libs rpm-plugin-selinux rpm-sign-libs rust-srpm-macros samba-client samba-client-libs samba-common samba-common-libs sed selinux-policy selinux-policy-devel selinux-policy-targeted setup shadow-utils shared-mime-info sombok sqlite-libs sysprof-capture-devel systemd systemd-libs systemd-networkd systemd-pam systemd-resolved systemd-rpm-macros system-release systemtap-sdt-devel tar tzdata unzip urw-base35-bookman-fonts urw-base35-c059-fonts urw-base35-d050000l-fonts urw-base35-fonts urw-base35-fonts-common urw-base35-gothic-fonts urw-base35-nimbus-mono-ps-fonts urw-base35-nimbus-roman-fonts urw-base35-nimbus-sans-fonts urw-base35-p052-fonts urw-base35-standard-symbols-ps-fonts urw-base35-z003-fonts util-linux util-linux-core vim-common vim-data vim-enhanced vim-filesystem vim-minimal which xkeyboard-config xml-common xorg-x11-proto-devel xxd xxhash-libs xz xz-devel xz-libs yum zip zlib zlib-devel zstd 
```
### Install sources packages
```
rpm -ivh https://github.com/csabattier/amazonlinux/raw/main/packages/SRPMS/nagios-4.4.14-1.amzn2023.src.rpm
rpm -ivh https://github.com/csabattier/amazonlinux/raw/main/packages/SRPMS/nagios-plugins-2.4.6-2.amzn2023.src.rpm
rpm -ivh https://github.com/csabattier/amazonlinux/raw/main/packages/SRPMS/nrpe-4.1.0-2.amzn2023.src.rpm
```
### Build Package
```
cd /root/rpmbuild
```
```
rpmbuild -ba SPECS/nagios.spec
```
```
rpmbuild -ba SPECS/nagios-plugins.spec
```
```
rpmbuild -ba SPECS/nrpe.spec
```
