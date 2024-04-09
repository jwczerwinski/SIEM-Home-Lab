# SIEM-Home-Lab
<h2>Description</h2>
Implement Microsoft Sentinel (SIEM) and integrate it with a live virtual machine serving as a honeypot. Monitor real-time attacks, such as RDP Brute Force attempts, originating from global sources. Utilize a PowerShell script to retrieve geolocation data of attackers and visualize it on the Microsft Sentinel Map. <br />

<h2>Languages and Utilities Used</h2>
- <b>PowerShell</b> 

<h2>Environments Used </h2>
- <b>Micrsoft Sentinel</b> (22H2) <br />
- <b>Windows Server 2022 </b> (21H2)

<h2>Diagram </h2>
<img src="https://i.imgur.com/7qNlLBO.png" height="80%" width="80%" />

<h2>Walk-through:</h2>
<p align="center">
 
 [Azure Trial](https://azure.microsoft.com/en-us/free/)<br />
 [PowerShell Script](https://github.com/joshmadakor1/Sentinel-Lab/blob/main/Custom_Security_Log_Exporter.ps1)<br />
<br />
Start free trial Azure account: <br/>
<img src="https://i.imgur.com/SaKx6jR.png" height="80%" width="80%" />
<br />
<br />
Create a VM named "Honeypot", create resource group named "Honeypotlab", remove existing firewall rules, add a rule to allow all traffic in, then review and create VM: <br/>
<img src="https://i.imgur.com/txgXdec.png" height="80%" width="80%" />
<img src="https://i.imgur.com/mr41aRO.png" height="80%" width="80%" />
<img src="https://i.imgur.com/MA2yoZQ.png" height="80%" width="80%" />
<img src="https://i.imgur.com/YTzTl30.png" height="80%" width="80%" />
<img src="https://i.imgur.com/2V9gd1J.png" height="80%" width="80%" />
<img src="https://i.imgur.com/BpluC1u.png" height="80%" width="80%" />
<br />
<br />
Create Log Analytics workspace, add to Honeypotlab resource group, name "law-honeypot1", add to same region, then review and create Log Analytics: <br/>
<img src="https://i.imgur.com/qwD5cuv.png" height="80%" width="80%" />
<img src="https://i.imgur.com/pb5fi5N.png" height="80%" width="80%" />
<img src="https://i.imgur.com/1l31Qmz.png" height="80%" width="80%" />
<br />
<br />
From Microsoft Defender for Cloud, enable Log Analytics to gather VM logs: <br/>
<img src="https://i.imgur.com/zjo7GSC.png" height="80%" width="80%" />
<img src="https://i.imgur.com/dfqyiYk.png" height="80%" width="80%" />
<img src="https://i.imgur.com/X0gt5IH.png" height="80%" width="80%" />
<img src="https://i.imgur.com/1zjdUvM.png" height="80%" width="80%" />
<br />
<br />
Connect Log Analytics to VM: <br/>
<img src="https://i.imgur.com/9WGBfap.png" height="80%" width="80%" />
<img src="https://i.imgur.com/DovYnHD.png" height="80%" width="80%" />
<br />
<br />
Setup Microsoft Sentinel: <br/>
<img src="https://i.imgur.com/qthJlJN.png" height="80%" width="80%" />
<img src="https://i.imgur.com/qpjdktX.png" height="80%" width="80%" />
<br />
<br />
Log into VM with RDP: <br/>
<img src="https://i.imgur.com/II25P3u.png" height="80%" width="80%" />
<img src="https://i.imgur.com/D5rvf8r.png" height="80%" width="80%" />
<br />
<br />
Turn off Windows Firewall on VM: <br/>
<img src="https://i.imgur.com/2G00v1z.png" height="80%" width="80%" />
<img src="https://i.imgur.com/KghCre8.png" height="80%" width="80%" />
<img src="https://i.imgur.com/4uUINph.png" height="80%" width="80%" />
<br />
<br />

