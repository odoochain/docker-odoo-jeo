FROM jobiols/odoo-jeo:11.0
LABEL maintainer="Jorge Obiols <jorge.obiols@gmail.com>"

USER root

# scripts to extract sources to host
COPY ./extract_dist-packages.sh /
COPY ./extract_dist-local-packages.sh /

# requerimiento para odoo-uml
RUN apt-get -qq update && apt-get install -yqq --no-install-recommends \
    default-jdk \
    && rm -rf /var/lib/apt/lists/*

RUN pip3 install \
    wdb \
    erppeek

USER odoo
