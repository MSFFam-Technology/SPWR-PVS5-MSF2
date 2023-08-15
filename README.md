# SPWR-PVS5-MSF2

Sunpower PVS5 Home Monitoring 

all credit goes to : https://github.com/ginoledesma/sunpower-pvs-exporter

I have just bundled the entire SunPower PVS solution with connectivity to Prometheus Server and Grafana Client UI.

All other programs and configurations are bundled but you will have to install python3 and pip prior to running things.

--
User will Require this Software bundle:
https://www.dropbox.com/s/ib95q7w997kdknp/MSF_SunPower_Monitor_Bundle-v2_PWP.zip?dl=0

User will Require this Hardware:

- Computer that has 2 Network interface Cards
   NIC 1 : onboard Ethernet will connect to --> Sunpower PVS5 BLACK port
   NIC 2 : USB Ethernet Adapter / Wi-fi Network --> connect to your local home network which has internet access

  User will install:
- python and pip sofware
- sunpower-pvs-bundle (from ginoledesma)


  Steps:

1) Install Python3 and pip on windows 10 based machine
   
   python install (Web Browser):
      Download https://www.python.org/downloads/
   
   pip install (using Powershell):
      python.exe ../Python/python-3.11.3/get-pip.py

   NOTE: When installing python, select the options:
        * Add python.exe to PATH
        * Select "Customize Installation" --> select and include 'pip'

   
2) Open Powershell , install ginoledesma sunpower-pvs-exporter
       pip install sunpower_pvs_exporter
         or
       pip install git@github.com:ginoledesma/sunpower-pvs-exporter.git
   

3) Download SPWR-PVS5-MSF2 software bundle and unzip . Copy to Desktop.

4) Quickly read included instructions to start services using the Powershell

5) Open Powershell, cd to software bundle directory 
   
6) Open Powershell , and enter included commands to start sunpower-pvs-exporter
7) Open Powershell , and enter included commands to start the pre-configured monitor software(1)
8) Open Powershell , and enter included commands to start the pre-configured gui software(2)
    
9) Using the same computer, Connect to gui web ui with web browser. Password is included.
       * Please note that you can connect to the gui from a remote machine on your LAN if you enter the address:
         http://<IP Address of machine running sunpower-pvs-exporter>:3000
   
11) From within gui, navigate to create 'New' Dashboard.
    Import the dashboards created by ginoledesma:
    https://github.com/ginoledesma/sunpower-pvs-exporter/blob/master/docs/inverter_panel_config.json
    https://github.com/ginoledesma/sunpower-pvs-exporter/blob/master/docs/pvs_supervisor_panel_config.json
    https://github.com/ginoledesma/sunpower-pvs-exporter/blob/master/docs/summary_panel_config.json

12) At this time you should see a graphical viewing of EACH of your Inverters with the gui software.
