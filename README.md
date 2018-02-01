# Parides [![Build Status](https://travis-ci.org/goettl79/parides.svg?branch=master)](https://travis-ci.org/goettl79/parides)

Parides is a simple python module to convert Prometheus metrics data to a pandas dataframe or a comma-separated file.
For a jumpstart / converting to csv at the console use the docker command below. The csv files will be in your /tmp
folder prefixed with an "all".

    docker run \
        -v /tmp:/usr/src/app/timeseries \
        -i goettl/parides \
            http://192.168.2.110:9090 {__name__=~\".+\"} \
            --dsid=all \
            --delta=20 


Further examples are currently under construction in the [documentation](https://goettl79.github.io/parides/) section.