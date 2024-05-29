# Decrypting Virtual Private Network Traffic

<h2> Description </h2>
This project demostrates a critical vulnerability in Virtual Private Networks (VPN's) that can be exploited on a local network. It was conducted within an isolated virtual network that was meant to replicate a real-world attack. The exploit that was used on this virtual machine was CVE-2024-3661 aka TunnelVision which can redirect or manipulate VPN traffic and expose sensitive data and information to unauthorized users.
  


<h2> Testing Environment Used </h2>
  
- <b>Ubuntu Server 22.04</b>
- <b>Windows 10 Pro</b>
- <b>Pop OS 22.04</b>

# Setup Internal Network & Network Adapter in VM Settings

<h2> DHCP Ubuntu Server <h2>
<img width="694" alt="DHCP Adp 1" src="https://github.com/a1xbit/DecloakingVPN/assets/119477838/6ea889c3-a730-4b42-bf11-f05a8d7f4d89">
<img width="694" alt="DHCP Adp 2" src="https://github.com/a1xbit/DecloakingVPN/assets/119477838/aae5b59a-7aac-4165-a4b1-4e1472be62e3">

<h2> Windows 10 Pro <h2>
<img width="695" alt="Win10 Adp 1" src="https://github.com/a1xbit/DecloakingVPN/assets/119477838/f6055e23-8991-4332-86c4-00f11386440d">
<img width="696" alt="Win10 Adp 2" src="https://github.com/a1xbit/DecloakingVPN/assets/119477838/a0aea21f-b31c-4338-8174-f030d5a3200c">

<h2> Pop OS <h2>
<img width="695" alt="PopOS Adp 1" src="https://github.com/a1xbit/DecloakingVPN/assets/119477838/e5143e5a-f5a8-43ea-8cae-71cb698edd5a">
<img width="695" alt="PopOS Adp 2" src="https://github.com/a1xbit/DecloakingVPN/assets/119477838/311cbdc6-13de-492b-a231-7bbb436a48e4">

# Configure Server

<h2> Server IP Address </h2>

![VirtualBox_DHCP Ubuntu Server 22 04_16_05_2024_05_01_26](https://github.com/a1xbit/DecloakingVPN/assets/119477838/b2098f10-1e80-454e-90b7-7558286e1b97)

<h2> Login to Server through SSH via Powershell </h2>

![VirtualBox_Windows 10 Pro_16_05_2024_20_22_43](https://github.com/a1xbit/DecloakingVPN/assets/119477838/2e1dcd20-ba8b-4742-92ab-3f5ca9feb604)

<h2> Download Tunnelvsion Respository </h2>

![VirtualBox_Windows 10 Pro_16_05_2024_20_23_14](https://github.com/a1xbit/DecloakingVPN/assets/119477838/f326ce66-53e7-4c49-890c-31ad0f767db5)

<h2> Change Directory </h2>

![VirtualBox_Windows 10 Pro_16_05_2024_20_27_51](https://github.com/a1xbit/DecloakingVPN/assets/119477838/a9b280d3-4680-4a45-8824-6dfdbe4dca44)

![VirtualBox_Windows 10 Pro_16_05_2024_20_23_40](https://github.com/a1xbit/DecloakingVPN/assets/119477838/68e2bb3a-0099-4300-a6a7-b0b63035c67f)

<h2> Execute Command </h2>

![VirtualBox_Windows 10 Pro_16_05_2024_20_24_26](https://github.com/a1xbit/DecloakingVPN/assets/119477838/60e64e59-545d-4607-973d-e7dda68f02a5)

![VirtualBox_Windows 10 Pro_16_05_2024_20_25_16](https://github.com/a1xbit/DecloakingVPN/assets/119477838/55e59780-f086-484c-9d35-2d548312971c)

![VirtualBox_Windows 10 Pro_16_05_2024_20_25_34](https://github.com/a1xbit/DecloakingVPN/assets/119477838/20f40d3b-73f2-48e3-a56d-efb631b34f1c)

![VirtualBox_Windows 10 Pro_16_05_2024_20_25_45](https://github.com/a1xbit/DecloakingVPN/assets/119477838/1368733f-ebd8-4bc9-a008-d7c67192e209)

![VirtualBox_Windows 10 Pro_16_05_2024_20_26_27](https://github.com/a1xbit/DecloakingVPN/assets/119477838/2159a651-5bb2-48ff-863a-d88ea6fede14)

<h2> Reboot Server </h2>

![VirtualBox_Windows 10 Pro_16_05_2024_20_27_51](https://github.com/a1xbit/DecloakingVPN/assets/119477838/13ca2ae9-01c4-4959-a5ae-c7037ab85eee)

# Rogue Admin Lab

<h2> Connect to VPN </h2>

<img width="311" alt="Screenshot 2024-05-28 at 8 43 28 PM" src="https://github.com/a1xbit/DecloakingVPN/assets/119477838/55e5441c-72a3-41e1-b57e-f2f3b6544ad1">

<h2> Push DHCP Route 121 </h2>

![VirtualBox_Windows 10 Pro_16_05_2024_20_32_37](https://github.com/a1xbit/DecloakingVPN/assets/119477838/dd0e9a92-a008-4b73-b77a-912388b44eb1)

<h2> Display Route Table </h2>

![VirtualBox_Pop OS_16_05_2024_20_33_41](https://github.com/a1xbit/DecloakingVPN/assets/119477838/956373c6-1055-4eb7-9c47-ad6ced7bef12)

<h2> Ping 8.8.8.8 </h2>

![VirtualBox_Pop OS_16_05_2024_20_41_16](https://github.com/a1xbit/DecloakingVPN/assets/119477838/08482692-8b87-4cb1-8e60-961193c50a83)

<h2> Observe Network Traffic through Wireshark </h2>

![VirtualBox_Pop OS_16_05_2024_20_37_39](https://github.com/a1xbit/DecloakingVPN/assets/119477838/fe84bbaf-c782-4304-b20e-e2c858f8601b)

<h2> Observe Unencrypted Network Traffic </h2>

![VirtualBox_Windows 10 Pro_16_05_2024_20_39_33](https://github.com/a1xbit/DecloakingVPN/assets/119477838/e0e1b9c3-9f20-454a-b152-9d96122ebfce)

![VirtualBox_Windows 10 Pro_16_05_2024_20_40_09](https://github.com/a1xbit/DecloakingVPN/assets/119477838/c420954a-86bf-43b4-9d49-f8a00723c2ac)


