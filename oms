#!/bin/bash
yum install wget -y
a=`[ -f /opt/microsoft/omsagent/bin/uninstall ] && echo "File exist" || echo "File does not exist"`
 echo $a
    if [ "$a" = "File exist" ]
then
    echo "File exist"
exit
else
    echo "File does not exist"
wget https://raw.githubusercontent.com/Microsoft/OMS-Agent-for-Linux/master/installer/scripts/onboard_agent.sh && sh onboard_agent.sh -w 0e178a58-2416-4d37-962b-a9b6f19ce0a8 -s gDRqzb6LFIu0jAfor+qMXphConpfn5OwXvtCMbzTJD8UUSmvVcJfQtQgzSwenoXF6HLEd2nlQmdwkyu3ERjdGA== -d opinsights.azure.com

proxyconf="https://13.89.50.211:8080"
sudo echo $proxyconf >> /etc/opt/microsoft/omsagent/proxy.conf
sudo chown omsagent:omiusers /etc/opt/microsoft/omsagent/proxy.conf
sudo chmod 600 /etc/opt/microsoft/omsagent/proxy.conf /etc/opt/microsoft/omsagent/proxy.conf  
sudo /opt/microsoft/omsagent/bin/service_control restart 0e178a58-2416-4d37-962b-a9b6f19ce0a8
fi
