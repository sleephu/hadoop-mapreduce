## hadoop-mapreduce
* Hadoop MapReduce example.
  * Using the access.log file stored in HDFS, implement MapReduce to find the number of times each IP accessed the website.

##### Prerequisites:
* Hadoop Installed.
* Copy access.log file into hdfs. 
* Suppose it's under hdfs:///logs

##### Usage:
* Import the project into Eclipse.
* Export the project as a jar file (accessMR.jar).
* Execute the command to do mapreduce in hadoop.

 ```
 hadoop jar /Users/hello/Desktop/accessMR.jar accessMR.AccessMR /logs/access.log /user/output
 ```
* Check the output.

  ```
  hadoop fs -cat /user/output/part-00000
  ```
###### Shortcut to run hadoop command:
Edit ~/.profile and setup hadoop home path.

  ```
  vim ~/.profile
  export HADOOP_HOME=/usr/local/bin/hadoop-2.7.1;
  export PATH=$PATH:$HADOOP_HOME/bin;
  ```
If ~/.bash_profile exists, add the following code to ~/.bash_profile so that you don't need to source the file everytime you reopen the terminal:
 ```
 source ~/.profile
 ```
 Reason: Interactive shell will check ~/.bash_profile, ~/.bash_login and ~/.profile in order.
