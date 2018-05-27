
FROM redis:4

COPY redis-master.conf /redis-master/redis.conf
COPY redis-slave.conf /redis-slave/redis.conf

RUN mkdir -p /redis-sentinel && \ 
    chmod -R 777 /redis-sentinel /redis-slave /redis-master

COPY run.sh /run.sh

RUN chmod 755 /run.sh

EXPOSE 26379
CMD [ "/run.sh" ]
ENTRYPOINT [ "bash", "-c" ]
