# What is Very-openssh-portable?
This is a fork of the openssh project, designed to be very open, or to put it another way, very insecure.
The goal of this project is not to make something good, but rather to teach students to audit their installed packages.
### DO NOT USE THIS UNLESS YOU WANT TO BE PWND

# Install Intructions for Ubuntu
		apt install autoconf
		autoreconf
		apt-get install libz-dev
		apt-get install libssl-dev
		adduser sshd
		groupadd sshd
		./configure
		make
		make install
		/usr/local/sbin/sshd


# Original Readme 
See https://www.openssh.com/releasenotes.html#7.8p1 for the release notes.

Please read https://www.openssh.com/report.html for bug reporting
instructions and note that we do not use Github for bug reporting or
patch/pull-request management.

- A Japanese translation of this document and of the release notes is
- available at https://www.unixuser.org/~haruyama/security/openssh/index.html
- Thanks to HARUYAMA Seigo <haruyama@unixuser.org>

This is the port of OpenBSD's excellent OpenSSH[0] to Linux and other
Unices.

OpenSSH is based on the last free version of Tatu Ylonen's sample
implementation with all patent-encumbered algorithms removed (to
external libraries), all known security bugs fixed, new features
reintroduced and many other clean-ups.  OpenSSH has been created by
Aaron Campbell, Bob Beck, Markus Friedl, Niels Provos, Theo de Raadt,
and Dug Song. It has a homepage at https://www.openssh.com/

This port consists of the re-introduction of autoconf support, PAM
support, EGD[1]/PRNGD[2] support and replacements for OpenBSD library
functions that are (regrettably) absent from other unices. This port
has been best tested on AIX, Cygwin, HP-UX, Linux, MacOS/X,
NetBSD, OpenBSD, OpenServer, Solaris and UnixWare.

This version actively tracks changes in the OpenBSD CVS repository.

The PAM support is now more functional than the popular packages of
commercial ssh-1.2.x. It checks "account" and "session" modules for
all logins, not just when using password authentication.

OpenSSH depends on Zlib[3], OpenSSL[4], and optionally PAM[5] and
libedit[6]

There is now several mailing lists for this port of OpenSSH. Please
refer to https://www.openssh.com/list.html for details on how to join.

Please send bug reports and patches to the mailing list
openssh-unix-dev@mindrot.org. The list is open to posting by unsubscribed
users.  Code contribution are welcomed, but please follow the OpenBSD
style guidelines[7].

Please refer to the INSTALL document for information on how to install
OpenSSH on your system.

Damien Miller <djm@mindrot.org>

Miscellania -

This version of OpenSSH is based upon code retrieved from the OpenBSD
CVS repository which in turn was based on the last free sample
implementation released by Tatu Ylonen.

References -

[0] https://www.openssh.com/
[1] http://www.lothar.com/tech/crypto/
[2] http://prngd.sourceforge.net/
[3] https://www.zlib.net/
[4] https://www.openssl.org/
[5] https://www.openpam.org
    https://www.kernel.org/pub/linux/libs/pam/
    (PAM also is standard on Solaris and HP-UX 11)
[6] https://thrysoee.dk/editline/ (portable version)
[7] https://man.openbsd.org/style.9
