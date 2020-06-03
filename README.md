## Green Data

Anonymized data from the RISE Luleå data center in the time period March 18 -
June 2 2020. The data consists of three main folders,

- [Node data](#node-data)
- [Container data](#container-data)
- [Weather data](#weather-data)

### Node data

Data from the nodes in the Kubernetes cluster.

- `node_total_cpu_seconds` is the metric for the node CPU usage in `seconds`.
  Each node has 24 cores, and `node_total_cpu_seconds = 1` signifies that the
  node is seeing CPU utilization equivalent to one of its cores operating at
  100%.
- `node_total_memory_bytes` is the metric for the node RAM memory usage in
  `Bytes`.
- `node_total_read_bytes` is the metric for the node file system reads in
  `Bytes`.
- `node_total_write_bytes` is the metric for the node file system reads in
  `Bytes`.
- `node_total_receive_bytes` is the metric for the node network receive in
  `Bytes`.
- `node_total_transmit_bytes` is the metric for the node network transmit in
  `Bytes`.
- `node_power` is the node energy consumption in `Wh`
- `timestamp` is the UNIX timestamp of the data point
- `node` is an anonymized index of the node

### Container data

Data from the individual containers running in the Kubernetes cluster.

- `container_cpu_seconds` is the metric for the container CPU usage in
  `seconds`. Each node has 24 cores, and `container_cpu_seconds = 1` signifies
  that the container is seeing CPU utilization equivalent to one of the cores
  of its nodes operating at 100%.
- `container_memory_bytes` is the metric for the container RAM memory usage in
  `Bytes`.
- `container_read_bytes` is the metric for the container file system reads in
  `Bytes`.
- `container_write_bytes` is the metric for the container file system reads in
  `Bytes`.
- `node_power` is the node energy consumption in `Wh`
- `container` is an anonymized index of the container
- `timestamp` is the UNIX timestamp of the data point
- `node` is an anonymized index of the node

### Weather Data

Weather data from the weather station at Luleå Airport.

- `temperature` is the metric for the air temperature in `Celsius`
- `timestamp` is the UNIX timestamp of when the data was gathered (every 30
  min)
- `wind_speed` is the metric for the wind speed in `km/h`
- `desciption` is a text string describing the conditions (i.e. `Sunny`,
  `Cloudy` etc.)
- `pressure` is the metric for air pressure in `hPA`
- `humidity` is the metric for air humidity in `percent`
