<p align="center">
<img src="https://i.imgur.com/ji8tw98.png" width="50%" height="50%"/>
</p>

<h1>Practicing with DNS</h1>

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>A-Record Exercise</h2>
<ol>
  <li>Connect/log into DC-1 as your domain admin account (mydomain.com\jane_admin)</li>
  <li>Connect/log into Client-1 as an admin (mydomain\jane_admin)</li>
  <li>From Client-1 try to ping “mainframe” notice that it fails</li>
  <li>Nslookup “mainframe” notice that it fails (no DNS record)</li>
  <li>Create a DNS A-record on DC-1 for “mainframe” and have it point to DC-1’s Private IP address</li>
  <li>Go back to Client-1 and try to ping it. Observe that it works</li>
</ol>

<h2>Local DNS Cache Exercise</h2>
<ol>
  <li>Go back to DC-1 and change mainframe’s record address to 8.8.8.8</li>
  <li>Go back to Client-1 and ping “mainframe” again. Observe that it still pings the old address</li>
  <li>Observe the local dns cache (ipconfig /displaydns)</li>
  <li>Flush the DNS cache (ipconfig /flushdns).</li>
  <li>Observe that the cache is empty (ipconfig /displaydns)</li>
  <li>Attempt to ping “mainframe” again. Observe the address of the new record is showing up</li>
</ol>
