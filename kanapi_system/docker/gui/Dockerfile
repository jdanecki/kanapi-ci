FROM kanapi/kanapi-x11
MAINTAINER Jacek Danecki <jacek.m.danecki@gmail.com>
RUN mkdir /kanapi_build/kanapi
COPY kanapi /kanapi_build/kanapi
RUN /kanapi_build/kanapi/kanapi_system/docker/configure; cd /kanapi_build/kanapi/kanapi_system/x86_64 && ./install gui verbose  && \
	/kanapi_build/kanapi/kanapi_system/docker/strip_binaries && \
	 rm -rf ${HOME}/src && mkdir ${HOME}/src && rm -rf ${HOME}/.ccache && rm -rf /kanapi_build/kanapi
CMD ["/bin/bash"]
