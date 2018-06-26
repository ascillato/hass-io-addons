ARG BUILD_FROM
FROM $BUILD_FROM

ENV LANG C.UTF-8

RUN apk add --no-cache \
    py-pip \
	python \
	python-dev\
 && pip install -U pip

# Copy data for add-on
COPY ntpserver.py /ntpserver.py
COPY run.sh /
RUN chmod a+x /run.sh
RUN chmod a+x /ntpserver.py

CMD [ "/run.sh" ]