To compile the package skip the tests 
mvn clean package -Dmaven.test.skip=true

Testing setup




Configuration of Kafka Sink
----------

    agent_log.sinks.kafka.type = com.vipshop.flume.sink.kafka.KafkaSink
    agent_log.sinks.kafka.channel = all_channel
    agent_log.sinks.kafka.zk.connect = 127.0.0.1:2181
    agent_log.sinks.kafka.topic = all
    agent_log.sinks.kafka.batchsize = 200
    agent_log.sinks.kafka.producer.type = async
    agent_log.sinks.kafka.serializer.class = kafka.serializer.StringEncoder
    agent_log.sinks.kafka.metadata.broker.list=127.0.0.1:9092
    


Configuration of Kafka Source
----------

    agent_log.sources.kafka0.type = com.vipshop.flume.source.kafka.KafkaSource
    agent_log.sources.kafka0.zk.connect = 127.0.0.1:2181
    agent_log.sources.kafka0.topic = all
    agent_log.sources.kafka0.groupid = es
    agent_log.sources.kafka0.channels = channel0

