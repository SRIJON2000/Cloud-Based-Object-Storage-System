# Cloud-Based-Object-Storage-System

### Q2. In this problem, cloud based object storage system is to be implemented.

- Data (set of objects) is partitioned and stored using consistent hashing on a ring topology of
  2
  64 id space. Number of nodes (Containers/VMs) should be at least 3 and each representing
  500 virtual nodes.
- Each object is replicated in N nodes (N is configurable). Consistency among replicas is
  achieved by using vector clocks, read-write quorums, and rea-repair and anti-entropy process.
  Dynamo paper
- Every t seconds (t is configurable), system should check for hotspots and migrate
  VM/container using volume-to-size ratio. Reference
- REST API for user to be able to create/delete objects.
- The API should return the following in a JSON object: Success or failure, Vector clocks of
  all replicas, Node number where the write took place (in case of write)
