Netlink
=======

## Compiling

Get dependencies

```sh
rebar get-deps
```

And compile

```sh
rebar compile
```

## Testing

Start erlang with netlink application

```sh
erl -pa ebin -s netlink
```

And list all network interfaces

```sh
netlink:i().
```

Which should print something comparable to

```sh
link {
    addr { address fe80::216:3eff:fe07:64cc; flags [permanent]; scope 253; 8 <<128,0,0,0>>; index 10; family inet6; prefixlen 64;}
    addr { address fdf9:8bf1:beb1:1:216:3eff:fe07:64cc; flags []; scope 0; 8 <<0,1,0,0>>; index 10; family inet6; prefixlen 64;}
    addr { address 172.31.0.112; flags [permanent]; broadcast 172.31.0.255; scope 0; 8 <<128,0,0,0>>; index 10; family inet; label "eth0"; local 172.31.0.112; prefixlen 24;}
    32 <<1,0,0,0>>;
    group 0;
    35 <<2,0,0,0>>;
    address 00:16:3e:07:64:cc;
    qdisc "noqueue";
    41 <<0,0,1,0>>;
    flags [up,broadcast,running,multicast,lower_up];
    broadcast ff:ff:ff:ff:ff:ff;
    31 <<1,0,0,0>>;
    mtu 1500;
    linkmode default;
    operstate up;
    ifname "eth0";
    37 <<0,0,0,0>>;
    40 <<255,255,0,0>>;
    index 10;
    promiscuity 0;
    14 <<0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0>>;
    33 <<1>>;
    link 11;
    39 <<0>>;
    txqlen 1000;
    linkinfo [{kind,"veth"}];}
link {
    addr { address ::1; flags [permanent]; scope 254; 8 <<128,0,0,0>>; index 1; family inet6; prefixlen 128;}
    addr { address 127.0.0.1; flags [permanent]; scope 254; 8 <<128,0,0,0>>; index 1; family inet; label "lo"; local 127.0.0.1; prefixlen 8;}
    32 <<1,0,0,0>>;
    group 0;
    35 <<0,0,0,0>>;
    address 00:00:00:00:00:00;
    qdisc "noqueue";
    41 <<0,0,1,0>>;
    flags [up,loopback,running,lower_up];
    broadcast 00:00:00:00:00:00;
    31 <<1,0,0,0>>;
    mtu 65536;
    linkmode default;
    operstate unknown;
    ifname "lo";
    40 <<255,255,0,0>>;
    index 1;
    promiscuity 0;
    14 <<0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0>>;
    33 <<1>>;
    39 <<0>>;
    txqlen 1;}
ok
```
