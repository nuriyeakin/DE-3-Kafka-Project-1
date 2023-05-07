# QUESTIONS

- Truncate topic1.
- Produce iris.csv using data-generator to topic1.
- Build a python consumer;
	- Comsume from topic1. 
	- Write the message content, topic name, partition number of each flower type in a separate file with its own name (`/tmp/kafka_out/<species_name_out.txt`>).
	- Write messages that do not belong to any of the three flower types in the `/tmp/kafka_out/other_out.txt` file.

Example result file tree: 
```
tree /tmp/kafka_out/
/tmp/kafka_out/
├── other_out.txt
├── setosa_out.txt
├── versicolor_out.txt
└── virginica_out.txt
```

Example file content
```
 head /tmp/kafka_out/setosa_out.txt
topic1|2|0|0|5.1,3.5,1.4,0.2,Iris-setosa
topic1|2|1|2|4.7,3.2,1.3,0.2,Iris-setosa
topic1|2|2|3|4.6,3.1,1.5,0.2,Iris-setosa
topic1|2|3|9|4.9,3.1,1.5,0.1,Iris-setosa
topic1|2|4|16|5.4,3.9,1.3,0.4,Iris-setosa
topic1|2|5|29|4.7,3.2,1.6,0.2,Iris-setosa
topic1|2|6|32|5.2,4.1,1.5,0.1,Iris-setosa
topic1|2|7|36|5.5,3.5,1.3,0.2,Iris-setosa
topic1|2|8|40|5.0,3.5,1.3,0.3,Iris-setosa
topic1|2|9|41|4.5,2.3,1.3,0.3,Iris-setosa
```
