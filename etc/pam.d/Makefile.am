# This is a dummy Makefile.am to get automake work flawlessly,
# and also cooperate to make a distribution for `make dist'

pamd_files = \
	chfn \
	chsh \
	groupmems \
	login \
	passwd

pamd_acct_tools_files = \
	chage \
	chgpasswd \
	chpasswd \
	groupadd \
	groupdel \
	groupmod \
	newusers \
	useradd \
	userdel \
	usermod

if USE_PAM
pamddir = $(sysconfdir)/pam.d
pamd_DATA = $(pamd_files)
if ACCT_TOOLS_SETUID
pamd_DATA += $(pamd_acct_tools_files)
endif
endif

if WITH_SU
pamd_files += su
endif

EXTRA_DIST = $(pamd_files) $(pamd_acct_tools_files)
