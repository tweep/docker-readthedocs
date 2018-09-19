FROM elasticsearch:1.7-alpine
LABEL maintainer="Yevgeny Popovych <jmennius@gmail.com>"

# Add  debug messagese as i had problems with DNS 
# This helped me fixed the issue:
# https://development.robinwinslow.uk/2016/06/23/fix-docker-networking-dns/  
# Note: I updated /etc/docker/daemon.json and added the dns servers on my Ubuntu 18.04 cloud host machine
# cat     /etc/docker/daemon.json:
#
#    {
#        "dns": ["128.137.240.235", "128.137.241.235", "10.0.0.2", "8.8.8.8"]
#    }
RUN /usr/share/elasticsearch/bin/plugin -l -v -install elasticsearch/elasticsearch-analysis-icu/2.7.0
