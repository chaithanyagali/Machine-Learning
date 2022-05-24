# Machine-Learning
## About Instructor
Andrew Ng is an adjunct professor at Stanford University, Ng co-founded Coursera and deeplearning.ai
## Content             
solutions for code , Andrew Ng online course(cousera)
## Applications required
Matlab/octave are used for coding
## Languages Required
simple python programming,basic operations in matlab


## Submission
you should submit the code by using matlab/octave using e-mail id and token no

sqoop-import --connect jdbc:mysql://cdb22dw011.c0lf9xyp8cv9.ap-south-1.rds.amazonaws.com/cdb21dw011 --username cdb22dw011 -P --table StudentData --target-dir /StudentData1 -m 1\
sqoop-import --connect jdbc:mysql://cdb22dw011.c0lf9xyp8cv9.ap-south-1.rds.amazonaws.com/cdb21dw011 --username cdb22dw011 -P --table StudentData --where "gender='Female'" --target-dir /StudentDataFemale -m 1


cp /home/ubh01/apache-hive-2.3.2-bin/lib/hive-common-2.3.2.jar /home/ubh01/sqoop-1.4.7.bin__hadoop-2.6.0/lib/

create table karthick(
age int,
gender string,
name string,
course string,
roll int,
marks int,
email string)
row format delimited
fields terminated by ','
TBLPROPERTIES ("skip.header.line.count"="1");
=============================================================================
# Load the data from HDFS Location -> move the file from original location to hive architecture local
#if you drop the data original file is lost
load data inpath '/karthick/StudentData.csv' overwrite into table karthick;
=============================================================================
#Load from the Local File System
#Keep the original file from local file system
load data local inpath '/home/ubh01/Desktop/StudentData.csv' overwrite into table karthick;
============================
export PIG_HOME=/home/ubh01/pig/pig-0.17.0
export PATH=$PATH:/home/ubh01/pig/pig-0.17.0/bin
export PIG_CLASSPATH=$HADOOP_HOME/conf
 
#JAVA_HOME
export JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64
