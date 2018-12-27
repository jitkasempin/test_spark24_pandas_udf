# In progress
In order to learn how to setup and config hive-site.xml and develop spark application in scala that support ingesting to Hive.

Example command:
../spark-2.3.1-bin-hadoop2.7/bin/spark-submit --jars "core/target/spark-hive-streaming-sink_2.11-assembly-0.1.0-SNAPSHOT.jar,/home/ubuntu/apache-hive-3.1.1-bin/conf/hive-site.xml" --files /home/ubuntu/apache-hive-3.1.1-bin/conf/hive-site.xml --conf "spark.driver.extraClassPath=core/target/spark-hive-streaming-sink_2.11-assembly-0.1.0-SNAPSHOT.jar:/home/ubuntu/apache-hive-3.1.1-bin/conf/hive-site.xml" --conf "spark.executor.extraClassPath=./" --class "com.hortonworks.spark.hive.example.HiveStreamingExample" --master local[*] example/target/spark-hive-streaming-sink-example_2.11-0.1.0-SNAPSHOT.jar localhost 9999 "thrift://localhost:9083" 
