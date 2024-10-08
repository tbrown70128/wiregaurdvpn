<h1>WireGuard VPN in Home Assistant</h1>

 
<h2>Description</h2>
Project consists of setting up a WireGuard VPN in Home Assistant is a great way to securely access your home network remotely. WireGuard is a lightweight and efficient VPN protocol that’s gaining popularity for its simplicity and performance. Let’s walk through the steps to get it up and running:
<br />


<h2>Languages and Utilities Used</h2>

- <b>Home Assistant</b> 
- <b>YAML</b>

<h2>Environments Used </h2>

- <b>Windows </b> 

<h2>Program walk-through:</h2>


<b>Prerequisites:</b>
-  You’ll need Home Assistant installed and running.
-  Access to your router (to configure port forwarding).
-  At least one client device (Windows, macOS, iOS, or Android) that you want to connect to the VPN.: <br/>

<b>Install the WireGuard Add-On:</b>
-  Open Home Assistant.
-  Go to Supervisor > Add-On Store.
-  Search for “WireGuard” and install it. <br/>
<img src="https://i.imgur.com/aul6yPh.png"/>

<b>Configure WireGuard:</b>
-  In the WireGuard add-on settings, set the following
- Host: Your external address (e.g., your DuckDNS subdomain).
- Peers: Define the devices you want to connect. For example: <br/>
<img src="https://i.imgur.com/e7i4AD1.png"/> </b>
- Replace YOUR_NAME.duckdns.org with your actual address or dynamic DNS.
- Feel free to add more peers if needed. <br/>

<b>AdGuard Integration (Optional):</b>
-  If you want to block ads while using the VPN, you can add AdGuard.
-  Set the DNS server to the IP address of your AdGuard instance:
<img src="https://i.imgur.com/PwtyLnY.png"/> <br/>

<b>Save Configuration:</b>
-  Click the “SAVE” button in the add-on settings.<br/>

<b>Missing WireGuard Kernel Module:</b>
-  If you encounter this error, you might need to install the WireGuard kernel module on your host system. Check the add-on logs for details.<br/>

<b>Port Forwarding:</b>
-  In your router settings, forward UDP port 51820 to your Home Assistant instance.<br/>

<b>Connect Clients:</b>
-  Install the WireGuard app on your client devices.
-  Import the configuration (you can scan a QR code generated by Home Assistant).
-  Turn on the VPN and test the connection.<br/>

And that’s it! You should now have a functional WireGuard VPN running through Home Assistant. Remember to keep your keys secure and regularly update them for added security. If you have any questions along the way, feel free to ask! 😊🔒
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
