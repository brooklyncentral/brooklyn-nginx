# NGINX

NGINX is a free, open-source, high-performance HTTP server and reverse proxy. These are [Apache Brooklyn](http://brooklyn.apache.org) YAML blueprints for the deployment and in-life management of NGINX.

## Basic Config

This blueprint is mainly designed for use as a load balancer, the [example three tier blueprint](tests/nginx/yamlNginxThreeTier.bom) shows it in use. It is a minimal drop-in
replacement for the Apache Brooklyn [java NGINX blueprint](https://brooklyn.apache.org/learnmore/catalog/catalog-item.html#!entities/org.apache.brooklyn.entity.proxy.nginx.NginxController). 
Additionally it has a config key `sensor.inpool` which allows the specification of the sensor which determines if an item in a load balanced cluster should be in the load balancer
pool or not. This defaults to `service.isUp` which was the hard coded sensor monitored by the Java implementation.

## Future development

The blueprint is currently functional for basic usage but the following items probably require further input: 

* SSL configuration 
* Weighting / load balancing rules
* Additional configuration
