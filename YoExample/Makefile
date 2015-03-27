USE_PKGBUILD=1
include /usr/local/share/luggage/luggage.make
PACKAGE_VERSION=1.0
TITLE=YoDocumentationExample
REVERSE_DOMAIN=com.github.erikng
USE_PKGBUILD=1
PAYLOAD= \
		pack-usr-local-outset-login-once-yo.sh \
		pack-Library-Documentation-yo.pdf \
		pack-utilities-yo.app
		
l_usr_local_outset_login_once: l_usr_local
	@sudo mkdir -p ${WORK_D}/usr/local/outset/login-once
	@sudo chown -R root:wheel ${WORK_D}/usr/local/outset/login-once
	@sudo chmod -R 755 ${WORK_D}/usr/local/outset/login-once

pack-usr-local-outset-login-once-%: % l_usr_local_outset_login_once
	@sudo ${INSTALL} -m 755 -g wheel -o root "${<}" ${WORK_D}/usr/local/outset/login-once
	
l_Library_Documentation: l_Library
	@sudo mkdir -p ${WORK_D}/Library/Documentation
	@sudo chown root:admin ${WORK_D}/Library/Documentation
	@sudo chmod 775 ${WORK_D}/Library/Documentation
	
pack-Library-Documentation-%: % l_Library_Documentation
	@sudo ${INSTALL} -m 664 -g admin -o root "${<}" ${WORK_D}/Library/Documentation