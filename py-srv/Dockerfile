FROM praqma/native-buck

WORKDIR /app

COPY bin .

RUN apt update

RUN pip install -r requirements.txt

ENV WAIT_VERSION 2.7.2

ADD https://github.com/ufoscout/docker-compose-wait/releases/download/$WAIT_VERSION/wait /wait

RUN chmod +x /wait

CMD ["buck", "run", "alias_to_python"]