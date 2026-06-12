# Nmap Cheat Sheet

## Basic Scans
nmap 192.168.1.1              # scan one target
nmap 192.168.1.1-254          # scan whole network
nmap -p 80 192.168.1.1        # scan one port
nmap -p- 192.168.1.1          # scan ALL 65535 ports

## Detection
nmap -sV 192.168.1.1          # detect service versions
nmap -O 192.168.1.1           # detect OS
nmap -A 192.168.1.1           # detect everything

## Stealth
nmap -sS 192.168.1.1          # SYN scan (quiet)
nmap -T1 192.168.1.1          # slowest (bypass firewall)
nmap -T5 192.168.1.1          # fastest

## Save Output
nmap -oN result.txt 192.168.1.1    # save as text
nmap -oX result.xml 192.168.1.1    # save as XML

## Best All-in-One Command
nmap -A -T4 -p- 192.168.1.1

## LEGAL REMINDER
Only scan targets you OWN or have written permission to scan.
