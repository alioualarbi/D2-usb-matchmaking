# D2-matcmaking
First credits to @BasRaayman and @inchenzo

## ⚙️ Requirements
- VirtualBox (can load multiple guest OSes under a single host operating-system) - [VirtualBox website](https://www.virtualbox.org/)
- Ubuntu 21.04 server image - [Download image](https://ubuntu.com/download/desktop/thank-you/?version=21.04&architecture=amd64)

## 📁 Virtual Server Creation
1. Create a Virtual Machine by clicking the **New** button
1. Name the machine Ubuntu and set its Memory size to **2048MB**
1. Do not change the VDI settings and click **Create**
1. Go to the Network tab in the machine settings (yellow **Settings** button), and change the **NAT** option to **Bridged Adaptator** (select the interface that is connected to internet )
1. In the same menu enable the seconde interface, and change the **NAT** option to **Bridged Adaptator** and choose your seconde interface (where the console connected)
1. Start the machine and select the Ubuntu server image (I'm using ubuntu 21.04)

## 🔌 Give yourself permissions
```bash
sudo su
```

## 🤖 Install the script
```bash
rm *
wget -q https://raw.githubusercontent.com/alioualarbi/D2-matcmaking/main/d2 -O ./d2
chmod +x ./d2

## Usage
#### Setup: initial setup
``` sudo bash d2 -a setup ```
#### Add: add a sniffed id to your firewall
``` sudo bash d2 -a add ```
#### Remove: remove ids from the end of the list
``` sudo bash d2 -a remove ```
#### Sniff: Auto sniffer. (You must add your 2 host consoles prior to running this)
``` sudo bash d2 -a sniff ```
#### Open: Enables public matchmaking 
``` sudo bash d2 -a open ```
#### Close: Disables public matchmaking
``` sudo bash d2 -a close ```
#### List: List the current accounts
``` sudo bash d2 -a list ```
#### Update: Update the script to the newest version.
``` sudo bash d2 -a update ```
#### Load: Load the saved rules after a reboot
``` sudo bash d2 -a load ```
#### Reset: Reset iptables to default
``` sudo bash d2 -a reset ```
