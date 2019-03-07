FROM debian:testing

ENV DEBIAN_FRONTEND noninteractive

RUN echo "Base Build: $(date)" > /etc/build_date
ONBUILD RUN echo "Child Build: $(date) " >> /etc/build_date

RUN apt-get -y update && apt-get -y install \
  procps \
  net-tools \
  vim \
  && apt-get clean && rm -rf /var/lib/apt/lists
