# Network Experiments based on Locating Arrays

This repository contains for the network experiments based on Locating Arrays.
The idea is to generate different combinations of factors and analyze its effect on the Network.

Location Arrays has been used to generate these combinations 
because it provides an efficient way to generate these factors
than combinatorial arrays.

More details about LA is covered in the following paper:
https://www.researchgate.net/publication/276315580_Locating_Arrays

## Fabric Platform
Fabric is a research infrastructure platform where researchers can
develop experimental testbeds to bring the novel ideas into fruition.
The experiments could be related to Distributed Cloud Computing, NDN, P4
etc. There is hardly any limit on the nature of experiment which can be developed on Fabric.
More details about Fabric can be found in the below paper:

https://ieeexplore.ieee.org/iel7/4236/8970628/08972790.pdf

## Network Experiments
We are using Fabric platform to develop our experiments i.e. how different factors
influence the network. This requires setting up the code of LA on Fabric.
Fabric provides to flexibility to develop experiments with the help of 
Jupyter Notebook. Hence, three notebooks have been generated so far.

### Proof Of Concept (POC)
We first developed a POC experiment based on the native API provided by the Fabric.
We considered three factors (Core, RAM, Disk) to generate their different combinations
with the help of LA array.

The individual factor value can be found in the tsv file.
Different slices (with nodes) were generated based on the values of these factors
and ping tests were executed between the nodes as a Proof of Concept.

This motivated us to develop complex experiments on the Fabric Platform.

### POC using FabAPI
Fabric platform is still involving with addition of several APIs and 
experiments. Hence, it's very important for us as well to make our experiments compatible
with these evolving APIs.

Hence, the POC experiment was developed using FabAPI as well.

### Complex Experiment
Factors such as Cores, RAM and Disk wouldn't impact the network layer 
to a large extent. Hence, we moved to other factors such as 
TCP version, Number of Parallel Connections, Buffer Length etc.
The information about these factors can be found in the TSV files.

A complex experiment is under development where the nodes communicate with each
other using iperf3 utilizing different values of these factors.
In addition, R scripts will be used to analyze the results of these experiments.

However, using tools like iperf3 and R requires installation 
of several packages. Hence, Jupyter notebook has been developed
to take care of installing these dependencies on the nodes. The
automation of installing these packages will reduce the manual effort 
on the researcher's side.