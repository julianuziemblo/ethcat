# `ethcat`
Send and receive raw Ethernet frames.

## Running
Install `requirements.txt` and run with `sudo`.

## Modes of operation
- `send`:
    - `-c`/`--count`: number of packets to send, 1 on default
    - `-d`/`--dst`: destination MAC
    - `-t`/`--ethtype`: Ethertype
- `recv`:
    - `-c`/`--count`: number of packets to receive, 1 on default
    - `-f`/`--filter`: receive only packets matching the filter, no filter on default
      
      syntax: Python conditional syntax, available objects:
        - `src`: source MAC, like `00:11:22:33:44:55`
        - `dst`: destination MAC, like `00:11:22:33:44:55`
        - `ethtype`: Ethertype, like `0x1234`
- `echo`:
    - `-c`/`--count`: number of packets to echo, infinite on default
    - `-f`/`--filter`: same as in `recv` mode

## TODO
- [x] basic send and receive
- [x] echo packets
- [x] basic recv filtering
- [x] send packets with specified payload 
- [x] send random payload
- [ ] improved recv filtering
- [ ] send payload(s) from file
