# confix
Confix is a lightweight, Alpine-based configuration updating container designed to dynamically manage and inject configuration files into application containers at runtime. 
It ensures that the latest configuration files are seamlessly copied into specified volumes, making them accessible to running services without requiring full container rebuilds. 
Confix requires external volume management, which means we'd need to explicitly define an external named volume to use this contianer. The default volume it looks for is "config_volume" and the default config it looks for is "config.ini".

cd in into confix, add config file and run command : 

``` sudo docker compose run --rm confix ```

The contianer is automatically removed after copying the latest config file in named volume.
