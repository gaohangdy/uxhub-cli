# uxhubcli - cli tool for UXHub experience platform

### about UXHub experience platform

UXHub is an API first headless experience management system

For more information about this project go to https://www.uxhub-platform.com/

### about percli

`uxhubcli` is a command line tool to accomplish general tasks that arise when 
working

### prerequisits

the following tools need to be installed and accessible for uxhubcli to be able to work

- Java 11
- NodeJS 14.16.0 (LTS)

### install uxhubcli
```
npm install uxhubcli -g
```

### install UXHub experience platform
```
uxhubcli server install
```

### start an already installed UXHub experience platform instance

```
uxhubcli server start
```

### stop a running UXHub experience platform instance

```
uxhubcli server stop
```

### check if a UXHub experience platform instance is running

```
uxhubcli server status
```

### list installed instances

```
uxhubcli server list
```

### running multiple instances

multiple uxhub instances can be installed, started and stopped using the `--name` and `--port` parameters. 

**note:** by default, an instance named `sling` will run on port `8080`.

to install an instance called `myinstance`, run:

```
uxhubcli server install --name myinstance --port 8081
```

to stop, start and check status of the instance, run:

```
percli server stop --name myinstance
percli server start --name myinstance
percli server status --name myinstance
```

### advanced install

you can define additional run modes during the server install. for example, if you want a classic author/publish
deployment, run:

```
percli server install --name author --port 8081 --runmodes author,notshared
percli server install --name publish --port 8082 --runmodes publish,notshared
```

the runmodes are saved in the server configuration file (`~/.perclirc`) and do not need to be specified after the initial install.

```
percli server start --name author 
percli server start --name publish
```
