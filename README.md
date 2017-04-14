# hadoop_bigram_unigram_generator
it is a bigram generator and counting program developed to run in hadoop distributed cluster.
it is case insensitive and regexp been used for tokenizing.
I am trying to figure out how to use the OpenNLP in hadoop environment. then the process will be further fragmented into sentence detection
then tokenization.

in order to run use the following command,
first compile using javac command
javac -cp path_to_hadoop/hadoop/*:path_to_hadoop/hadoop-mapreduce/* BigramCounter.java -d build Xlint

then create the jar file
jar -cvf BigramCounter.jar -C /build

finally submit the job 
hadoop jar BigramCounter.jar org.myorg.BigramCount /user/cloudera/wordcount/input /user/cloudera/wordcount/output 
-skip /user/cloudera/wordcount/stop_words.text
