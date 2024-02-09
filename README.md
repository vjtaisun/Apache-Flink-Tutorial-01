# Apache-Flink-Tutorial-01
Apache Flink

# Start the ZooKeeper service
$ bin/zookeeper-server-start.sh config/zookeeper.properties


# Start the Kafka broker service
$ bin/kafka-server-start.sh config/server.properties


# set flink path
$ export PATH=/home/vjtaisunubuntu/Downloads/flink-1.18.1/bin:$PATH


# run flink job
flink run -p 1 -py /home/vjtaisunubuntu/Desktop/DemoProject/flight-data-sink/create_source.py -pyfs /home/vjtaisunubuntu/Desktop/DemoProject/flight-data-sink/utils.py,/home/vjtaisunubuntu/Desktop/DemoProject/flight-data-sink/models.py -pyreq /home/vjtaisunubuntu/Desktop/DemoProject/flight-data-sink/requirements.txt -pyclientexec /home/vjtaisunubuntu/Desktop/DemoProject/flight-data-sink/env/bin/python -pyexec /home/vjtaisunubuntu/Desktop/DemoProject/flight-data-sink/env/bin/python
# flink run 
# -p 1 
# -py /home/vjtaisunubuntu/Desktop/DemoProject/flight-data-sink/create_source.py 
# -pyfs /home/vjtaisunubuntu/Desktop/DemoProject/flight-data-sink/utils.py,/home/vjtaisunubuntu/Desktop/DemoProject/flight-data-sink/models.py 
# -pyreq /home/vjtaisunubuntu/Desktop/DemoProject/flight-data-sink/requirements.txt 
# -pyclientexec /home/vjtaisunubuntu/Desktop/DemoProject/flight-data-sink/env/bin/python 
# -pyexec /home/vjtaisunubuntu/Desktop/DemoProject/flight-data-sink/env/bin/python

flink run -p 1 -py /home/vjtaisunubuntu/Desktop/DemoProject/flight-data-stats/flight_data_stats.py -pyfs /home/vjtaisunubuntu/Desktop/DemoProject/flight-data-stats/models.py, /home/vjtaisunubuntu/Desktop/DemoProject/flight-data-stats/utils.py -pyreq /home/vjtaisunubuntu/Desktop/DemoProject/flight-data-stats/requirements.txt -pyclientexec /home/vjtaisunubuntu/Desktop/DemoProject/flight-data-stats/env/bin/python -pyexec /home/vjtaisunubuntu/Desktop/DemoProject/flight-data-stats/env/bin/python

# Start Flink Cluster
$ ./bin/start-cluster.sh
$ ./bin/stop-cluster.sh


# Creating python virtual enviroment zip
# use script setup-pyflink-virtual-env.sh
$ setup-pyflink-virtual-env.sh 1.10.2