# Log4Shell Python

## Requirements

- \>=python3.6
- docker
- some python modules (see `exploit.py`)

## Preparation

Edit `exploit.py`

- Change `host` variable to external ip of the current host. This is used by the reverse shell to cnnect
- Change docker tag depending on the target java version (e.g. jdk8 might not be compatible with jdk11 appliation)
- Add current user to the docker group or change docker_cmd (e.g. add `sudo`)

## Exploitation

- Run `python exploit.py`
- Insert jdni string to victim server
- Wait for reverse shell to connect

## Credits

[kozmer/log4j-shell-poc](https://github.com/kozmer/log4j-shell-poc) for the Java exploit template
