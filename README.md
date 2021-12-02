# TICK-Stack
Download docker image for the following directories:
1. Chronograf
2. InfluxDB
3. Kapacitor
4. Telegraf

Once they are installed , go to Docker hub and run all the images.

The basic flow is that data is sent to telegraph and stored in InfluxDB database. With the help of Chronograf query can be placed via web interface and Kapacitor will process 
the monitor and raise the alerts based on data.

Tick.yml file is created with all the foru components for which image is downloaded. It defines the way they communicate to each other.

Through Docker config object , telegraf's configuration is provided.
The configuration defines the agen which gathers host CPU metrics and it defines an additional input method to receive data over HTTP.
Using swarm network for communication will be created between application and the containers.

Only telegraf and cronograf are exposed to the outer world. Telegraf used to store data through port and chronograph visualize the data.
