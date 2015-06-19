# Super Simple IPtables Config

## RedHat Family

    iptables -F
    iptables-restore < iptables.config
    service iptables save


## Ubuntu

This is probably out of date now, ymmv

    iptables -F
    iptables-restore < iptables.config
    iptables-save > /etc/iptables.rules
    echo "pre-up iptables-restore < /etc/iptables.rules" > /etc/network/interfaces
