# PartitionReckoner.jl
A package to gather partitioned datasets for file readers such as CSV.jl, Parquet.jl, etc.

Focus first on CSV.jl

```
INPUT:
a file path to root of dataset {ideally a URI, including s3 location}

OUTPUT:
a vector of file paths to dataset files or an iterator to be used by CSV.jl

partitions are recognized by a pattern like:

../dataset_name/partition_name_1=partitionA/partition_name2=partition01/part-0001-xxx.csv
```

Additional features:

* detect data type of partition, a la CSV.jl
* support partition pruning, prob define additional kwargs for CSV.jl


