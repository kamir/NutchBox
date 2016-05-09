# NutchBox

The project contains scripts and configuration files to bring up an Apache Nutch based crawler VM quickly.

Currently (Mai 2016) we use version 2.3.1 on CDH 5.5.0 in order to crawl data from the WWW into an Apache HBase system.
Apache Gora is used as abstraction layer and thus we can not build this sources against a newer CDH version. Solving this issue is a different sub project.

## Prerequisites
 - Java: 1.7.x
 - Maven: 3.x
 - Ant: 1.9.x

### Download the right QSVM:
 1) http://www.cloudera.com/downloads/quickstart_vms/5-5.html

We prepare a shared folder to export / import data from an to the VM. This way, our crawl VM should be stateless. 
Please be aware of the fact, that as soon as you have crawled a lot of pages, this data defines a state of the VM. This
is clearly an operational aspect and has nothing to do with application life cycle. We can crawl the pages again if we us a new VM but if you keep the crawl state, you have no stateless container any more. This is why the staging area - here a local HBase service - should be configured as a remote service as well. This way, Nutch is only crawling and all state information can be handled separately.

### Clone the NutchBox project from Github and share the folder QSVM5.5_NutchBox_v1.0 with your VM. 

If you prefere to go step by step, than you should download the source distribution of Apache Nutch from here: http://www.apache.org/dyn/closer.lua/nutch/2.3.1/apache-nutch-2.3.1-src.zip

### Configure it ...
 
### Build it ...

### Prepare SOLR home folder ...

### Prepare SOLR collection ...

### Check CDH status:
- Zookeeper
- HBase
- SOLR
- YARN

###Start Nutch Web-UI

### Define crawl seed.

### Start crawling

### Inspect crawl data

### Look into crawl results

### Export page graph to visualize Crawl graph.
