# SOLR-CLOUD
Open Search-Engine thing , which has feature of distributed Sharding/Replication and clustering ,which further helps in load-balancing , and query on large set of data

Here collections are at top level of hierache and then inside come multiple shards ,which distributes/partitoning the data amongs shards ,and then for load balancing /failure of one node  there is multiple-replica of node inside the shards ,in which one of them is a leader and gets firstly updated when new data comes and then it will asyncronously updates the other replicas , so high-availabily of data ,more the replica more scalable 

We can query on perticular shards also but then we have to insert the data in acc to some catogorization field like product etc thing.

And also there is route_name things available which is given at the time of collection making to shards , not sure but it would have to happen like that ,
and then smame like query on perticular shard ,we can give the route field at the time of quering and it gets data from that shards whose route_name is this.


Replica are of diffrent types they are core like nrt,etc and some of can leader , maintain transaction etc.

Shards are just an logical upper layer on the top of pysical core/replica layers.

And if we can't filter the shards on the query time , it will make just an distributed search over the whole shards , no latency and efficency gain on quering .
