FROM swift:3.1.0

RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        wget curl vim

####### Install Exercism CLI #######
COPY exercism /usr/bin/
RUN chmod o+r /usr/bin/exercism

RUN mkdir /exercism \
    && chmod 777 /exercism

RUN exercism --version

RUN exercism configure --key=YOUR_API_KEY_HERE

RUN exercism configure --dir=/exercism
