1. Launch Cloudera Manager
   sudo /home/cloudera/cloudera-manager --express --force

2. Open Cloudera Manager in browser and start:
   - HDFS
   - YARN

3. Verify Hadoop services are running
   jps

4. Create input directory in HDFS
   hdfs dfs -mkdir /user/cloudera/mr_input

5. Create input file in local system
   nano file.txt

6. Enter sample data
   Ever tried
   Ever failed
   No matter
   Try again
   Fail again
   Fail better

7. Upload input file to HDFS
   hdfs dfs -put file.txt /user/cloudera/mr_input

8. Verify file upload
   hdfs dfs -ls /user/cloudera/

9. Run MapReduce WordCount program
   hadoop jar /usr/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar wordcount /user/cloudera/mr_input /user/cloudera/mr_output

10. View output
    hdfs dfs -cat /user/cloudera/mr_output/part-r-00000
