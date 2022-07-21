FROM alpine:3.6

ENV PGHOST='postgresql-redmine-4-local-deployment.default.svc.cluster.local
:5432'
ENV PGDATABASE='public'
ENV PGUSER='root'
ENV PGPASSWORD='gyz.redmine'

RUN apk update
RUN apk add postgresql

COPY dumpDatabase.sh .

ENTRYPOINT [ "/bin/sh" ]
CMD [ "./dumpDatabase.sh" ]