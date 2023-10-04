FROM ocsinventory/ocsinventory-docker-image:2.12

ENV OCS_VERSION 2.12.0

LABEL maintainer="adrianrp1988@gmail.com" \
      version="${OCS_VERSION}" \
      description="OCS Inventory docker image with hardware change logs"

WORKDIR /usr/local/share/perl/5.34.0/Apache/

COPY ./Ocsinventory .

EXPOSE 80

# https://docs.docker.com/develop/develop-images/dockerfile_best-practices/#entrypoint
ENTRYPOINT ["/docker-entrypoint.sh"]
CMD ["/usr/sbin/apache2", "-DFOREGROUND"]
