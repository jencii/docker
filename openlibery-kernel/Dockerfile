FROM jenci/java

ENV VERSION 18.0.0.1
ENV RELEASE 2018-03-09_2209 
ENV INSTALL_DIR /opt/

ENV OPENLIBERTY_HOME ${INSTALL_DIR}/openliberty-${VERSION}
ENV DEPLOYMENT_DIR ${OPENLIBERTY_HOME}/standalone/deployments/
RUN curl -O https://public.dhe.ibm.com/ibmdl/export/pub/software/openliberty/runtime/release/${RELEASE}/openliberty-${VERSION}.zip \
  && unzip openliberty-${VERSION}.zip -d ${INSTALL_DIR} \
  && rm openliberty-${VERSION}.zip
ENV CONFIG /opt/wlp/usr/servers/defaultServer/
EXPOSE 9080 9443
ENTRYPOINT /opt/wlp/bin/server run defaultServer

