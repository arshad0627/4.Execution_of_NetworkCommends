# 4.Execution_of_NetworkCommands
## AIM :Use of Network commands in Real Time environment
## Software : Command Prompt And Network Protocol Analyzer
## Procedure: To do this EXPERIMENT- follows these steps:
<BR>
In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer 
<BR>
All commands related to Network configuration which includes how to switch to privilege mode
<BR>
and normal mode and how to configure router interface and how to save this configuration to
<BR>
flash memory or permanent memory.
<BR>
This commands includes
<BR>
• Configuring the Router commands
<BR>
• General Commands to configure network
<BR>
• Privileged Mode commands of a router 
<BR>
• Router Processes & Statistics
<BR>
• IP Commands
<BR>
• Other IP Commands e.g. show ip route etc.
<BR>

## PROGRAM 
## PING
```
import time
from ping3 import ping

def ping_simulation(host, count=4) -> None:
    print(f"Pinging {host} with {count} packets:")
    for i in range(count):
        delay = ping(host, timeout=1)
        if delay is None:
            print(f"Request timed out.")
        else:
            print(f"Reply from {host}: time={round(delay * 1000, 2)} ms")
        time.sleep(1)
ping_simulation('google.com')


```
## TRACEROUTE
```
import subprocess
import platform

def traceroute_simulation(host):
    system = platform.system()

    if system == "Windows":
        cmd = ["tracert", host]
    else:
        cmd = ["traceroute", host]

    try:
        result = subprocess.run(cmd, stdout=subprocess.PIPE, stderr=subprocess.PIPE, text=True)
        print(result.stdout)
    except Exception as e:
        print(f"Error: {e}")

# Run the function
traceroute_simulation('google.com')
```
## Output

![image](https://github.com/user-attachments/assets/74b71e52-e39d-44da-b7b2-52cf64264f0b)

![image](https://github.com/user-attachments/assets/59e25ede-b3a0-4519-a476-bf28a01c8e38)

## Result
Thus Execution of Network commands Performed 
