# Ports Scanning                                                                                                                                                                           
Ports Scannig is a simple CLI tool, to check if specific ports are opened or closed.                                                                                                                  
## Installation                                                                                                                                                                          
To install/ build the binary, make sure that you have installed the go compiler.

```bash
  git clone https://github.com/sk10az/ports_scanning
  cd ports_scanning
```
```bash
  sudo make build
```
This will build the Ports Scanning binary in your /bin/ directory.
     
## Usage

It always follows this schema, where you first specify one of the two protocols (tcp, udp), after that you can insert your destination, which you want to check for open ports(localhost, any IP address). Last but not least, append the port that should be checked.
```sh
ports_scanning <protocol> <destination> <port>
```
For the port you can specify a port, or check all. For the all option, you can choose between different speed levels.
- -a     (normal speed)
- -af    (faster)
- -asf   (super fast)

Example:
```sh
ports_scanning tcp localhost 8080
```
To check if port 8080 on your machine is currently open, or closed.
```sh
ports_scanning tcp 132.203.220.211 443
```
To check if port 443 (https) on another machine is open.
```sh
ports_scanning tcp localhost -a
```
To check all ports on your local machine.
```sh
ports_scanning tcp localhost -af
```
To check all ports on your local machine, but faster than normal mode.