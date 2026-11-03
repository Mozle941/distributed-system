![](https://nextwork.ai/mos-dev/uploads/56330f0f-e0c6-474e-bda9-d625ff412ba0_ris7uz4u)

## Project Overview: Exploring the CAP Theorem

### Goals and motivation

In this project, I'm building a distributrd key value store so that I can learn how distributed systems work.

## Building the Distributed Node and Cluster

### Setting up the project

In this step, I'm setting up a node as a flask application.

![Building the Distributed Node and Cluster](https://nextwork.ai/mos-dev/uploads/56330f0f-e0c6-474e-bda9-d625ff412ba0_4yjkejh9)

### Project files and their roles

I created the app.py file, requirements.txt file, Dockerfile and docker-compose.yaml which is responsible for the core logic, the dependency list for the program, the container blueprint and lastly the docker config.

## Launching the Cluster and Verifying Replication

### Normal operation goals

In this step, I'm launching all three nodes so that I can confirm that data written in one node automatically replicates to the others.

![Launching the Cluster and Verifying Replication](https://nextwork.ai/mos-dev/uploads/56330f0f-e0c6-474e-bda9-d625ff412ba0_9897rzta)

### Consistency before any partition

In CP mode, writes to node1 are also written in node 2 and 3. The CAP theorem doesn't force a trade-off yet because all three prerequisites of the CAP theorem have been satisfied.

## Simulating a Network Partition in CP Mode

### Partition simulation approach

In this step, I'm simulating a partition so that I can observe CP mode rejecting a write to protect consistency.

![Simulating a Network Partition in CP Mode](https://nextwork.ai/mos-dev/uploads/56330f0f-e0c6-474e-bda9-d625ff412ba0_tl0ju0r5)

### Why CP mode rejects writes

Node1 rejected the write because in CP mode the write is rejected until all the node are acessible.

## Observing Split-Brain in AP Mode

### Switching to AP mode

In this step, I'm switching to AP mode so that I can observe how it handles partitioning compared to CP mode.

### CP vs AP trade-offs explained

In CP mode the system trades off availability in order to protect consistency while in AP mode the system trades off consistency in order to ensure data is available.

## Implementing Conflict Resolution with Last-Write-Wins

![Implementing Conflict Resolution with Last-Write-Wins](https://nextwork.ai/mos-dev/uploads/56330f0f-e0c6-474e-bda9-d625ff412ba0_pfapdzbj)

### Trade-offs of eventual consistency

In this project extension, I observed that last-write-wins resolves conflicts by merging diverged data once the partition heals.

## Reflections and Key Takeaways

### Tools and concepts mastered

The key tools I used include python, Flask and Docker.Key concepts I learnt include simulating network partitions using Docker and I also learnt how CP mode and AP mode work.

### Time and challenges

This project took me approximately 2 hours. The most challenging part was simulating network partitions using curl commands.

### Looking ahead

I did this project today to learn how to build a distributed system and learn how it works. Another skill I want to learn is AWS.
