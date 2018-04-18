Clear Elastic search cache
curl -X DELETE 'http://localhost:9200/_all'

Filebeat
sudo rm data/registry
sudo ./filebeat -e -c filebeat.yml -d "publish"

Logstash
bin/logstash -f expertiza-logstash.conf --config.reload.automatic

Kibana
bin/kibana