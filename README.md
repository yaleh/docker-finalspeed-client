# finalspeed-client

## Example

### Configurations

Please create a configuration folder with following two files:

#### client_config.json

Following the guides at https://github.com/zqhong/finalspeed .

#### port_map.json

```
{
    "map_list": [
        {
            "dst_port": 23456, 
            "listen_port": 2200, 
            "name": "ssh"
        }
}
```

Notice the listen_port, which will be refered as DOCKER_LISTEN_PORT in the following shell command.

### Run the Docker Container
 
```bash
docker run -d -p EXTERNAL_LISTEN_PORT:DOCKER_LISTEN_PORT/tcp -v FINALESPEED_CONF_DIR:/conf --name finalspeed yaleh/finalspeed-client
```

