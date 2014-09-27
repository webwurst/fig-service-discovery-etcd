Service Discovery Using etcd and HAProxy
========================================

Based on Jason Wilders blog post [Docker Service Discovery Using Etcd and Haproxy}(http://jasonwilder.com/blog/2014/07/15/docker-service-discovery/).

    $ git clone https://github.com/webwurst/fig-service-discovery-etcd.git
    $ cd fig-service-discovery-etcd

    $ export HOST_IP=$(hostname --all-ip-addresses | awk '{print $1}')
    $ export ETCD_HOST=$HOST_IP:4001
    $ fig up

    $ xdg-open http://localhost:8000/
    $ xdg-open http://localhost:1936/

    $ fig scale whoami=3

Now reload http://localhost:8000/ several times while bypassing browser cache (ctrl+shift+r).
