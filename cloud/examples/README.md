1. Compile RocksDB first by executing `USE_AWS=1 USE_RTTI=1 DISABLE_WARNING_AS_ERROR=1 make -j8 static_lib; sudo ldconfig` in parent dir
2. Create bucket `rockset.cloud.durable.example.user` in minio
3. Compile examples: 
```
cd examples/
export AWS_ACCESS_KEY_ID="minioadmin"
export AWS_SECRET_ACCESS_KEY="minioadmin"
export USER="user"
make cloud_durable_example
```
