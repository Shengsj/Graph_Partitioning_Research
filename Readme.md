                                 SOCIAL GRAPH PARTITIONING ALGORITHMS RESEARCH

	           Student: Zishi Deng    Professor: Torsten Suel  Institution: New York University
      
**Research Abstract**

Graph partitioning is a well-known NP-hard problem that has no known efficient algorithm. Given its practical importance, many heuristic algorithms have been proposed. One example is METIS, a k-way multilevel partitioning algorithm, which can deliver good practical results. With the rise of social media, we see huge growth in social networks such as Facebook, Google+ and Twitter. The large amounts of user data make these social graphs impossible to be stored on a single machine. Thus, companies have built large distributed systems to store these graphs, and to run queries on them. However, due to bandwidth constraints and communication overheads, querying nodes across machines takes significantly more time than querying nodes locally. Hence, to minimize communication costs, data needs to be partitioned such that the total number of edges cutting across partitions is minimized while also satisfying constraints on the maximum amount of data that can be stored on each node.

In this research project, we study several methods proposed in recent papers, in particular, Balanced Label Propagation, LEOPARD, and a Bayesian Sharding approach. We implement these algorithms and run them on several large social graphs including LiveJournal, Orkut, and Pokec, each with millions of nodes and tens of millions of edges. We then compare and contrast the advantages and drawbacks for each algorithm. Finally, we further optimize the algorithms to improve partition quality.



**Repository Description**

	This git repository consists of three folders, and one poster briefly describes the purpose of the project,

	Balanced_Label_Propagation
	Disruptive_BLP_AutoConverge
	LEOPARD
	References
	Poster_ZISHI_DENG_pdf

	Balanced_Label_Propagation consists of two parts,
	1.Randomly initialized Balanced Label Propagation
	2.METIS + BLP (Balanced Label Propagation run on top of METIS)

	Disruptive_BLP_AutoConverge is the major improvements from Balanced_Label_Propagation
	1.Improved mapping algorithm allow it to run faster on larger graph and partitions
	2.It will run disruptive rounds when it is close to convergence (When improvement in locality between two rounds < 0.5%)
	3.It will automatically stop the BLP process and return the highest locality achieved when no improvement can be achieved (Convergence arises and it is lower than the previous convergence point)

	LEOPARD stands for Lightweight Edge-Oriented Partitioning and Replication for Dynamic Graphs
	It is still at the beginning stage

	References contains all the relevant papers referred during this research 
	

**Use Instruction**

	Please go into the respective sub-folders to read the instructions from there
