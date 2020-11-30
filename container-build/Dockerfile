# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent

EXPOSE 8080

LABEL 	io.openshift.expose-services="8080:http" \
	io.k8s.display-name="Appache HTML Server" \
	io.k8s.description="Appache HTML Server with custom data" \
	io.openshift.tags="apache, httpd"


RUN 	chgrp -R 0 /var/run/httpd /var/log/httpd && \
	chmod -R g=u /var/run/httpd /var/log/httpd && \
	sed -i "s/Listen 80/Listen 8080/g" /etc/httpd/conf/httpd.conf

USER 1001
