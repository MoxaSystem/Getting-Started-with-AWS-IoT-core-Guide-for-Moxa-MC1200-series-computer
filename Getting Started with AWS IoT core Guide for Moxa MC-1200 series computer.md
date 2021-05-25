# Getting Started with AWS IoT core Guide for Moxa MC-1200 series computer

# Document Information

## Revision History (Version, Date, Description of change)

| Version | Date        | Description of change |
| ------- | ----------- | --------------------- |
| 1       | 2021/05/29 | First release         |
|         |             |                       |

# Overview

The MC-1200 Series computers are built around a 7th Gen Intel®Celeron® or Intel® Core™ i3, i5, or i7 CPU and come with 1 HDMI display port, 3 USB 3.0 ports, 2 gigabit LAN ports, and 2 3-in-1 RS-232/422/485 serial ports. The MC-1200 is equipped with a 2.5” HDD/SSD slot and a built-in TPM 2.0 module. Additional value and convenience is provided through a modular design with three independent slots for flexible system integration and expansion. Users have the option to add a variety of different communications modules, including Wi-Fi, 3G, LTE, GPS, and mSATA expansion modules. The MC-1200 is designed to operate reliably in extreme conditions, such as continuous exposure to low or high temperatures, humidity, high vibration, and power surges, making them perfect for heavy industry, solar grid, water/wastewater, oil and gas, and transportation applications.

# Hardware Description


## DataSheet

[MC-1200 series](https://www.moxa.com/getmedia/d6169672-a7b1-4394-883b-c194e695d6c8/moxa-mc-1200-series-datasheet-v1.1.pdf)

## Standard Kit Contents

The standard shipping Moxa MC-1200 series computer package contains the following items:

- 1 x MC-1200 embedded computer
- 1 x Terminal block to power jack converter
- 1 x DIN-rail mounting kit
- 1 x Quick installation guide (printed)
- 1 x Warranty card

## User Provided items

To setup and operate Moxa MC-1200 series computer, users have to prepare the following items by themselves.

- 10/100/1000M Ethernet cables
- Power adapter: input voltage 90 to 264 VAC, output voltage 24 V with 2.5 A DC load (can be purchased separately from Moxa)
- Power Cord: Power cord with AU/CN/EU/UK/US plug, 2.5A/250V, 1.83 m (can be purchased separately from Moxa)

Based on user’s application requirement, the following items are optional

- WiFi or Cellular module (can be purchased separately from Moxa)
- Antennas (can be purchased separately from Moxa)

## 3rd Party purchasable items
N/A

# Set up your Hardware Environment
- **Connecting a Display**

    Moxa MC-1200 series computer comes with HDMI interfaces on the front panel. Connect a display monitor to the HDMI interfaces.

- **Connecting a Keyboard and Mouse**

    Connectors for a keyboard and mouse are located on the front panel of the computer. Both connectors are USB interfaces; you can directly connect a keyboard and a mouse using these connectors.

- **Powering on Moxa MC-1200 series computer :**

    To power on the MC-1200, connect the “terminal block to power jack converter” to the MC-1200’s DC terminal block (located on the side panel),and then connect the 9 to 36 VDC power adapter. The computer will be automatically turned on once the power adapter is plugged in. If it does not, press the Power Button to turn on the computer. Note that the Shielded Ground wire should be connected to the top pin of the terminal block. It takes about 30 seconds for the system to boot up. Once the system is ready, the Power LED will light up.
- **Accessing Moxa MC-1200 series computer Using a Linux/Windows PC or Mac**

    You can use a PC to access Moxa MC-1200 series 
    ****computer by using SSH over the network. Refer to the following IP addresses and login information:

    ![images/image2.png](images/image2.png)

Login: moxa

Password: moxa

Root account login is disabled until you manually create a password for the account. The user moxa is in the sudo group so you can operate system level commands with this user using the sudo command.

**ATTENTION: For security reasons, we recommend that you disable the default user account and create your own user accounts or** 

**Refer to Account Management of [Moxa MC-1200 series computer-linux-user-manual](https://www.moxa.com/getmedia/58efc9c5-5865-4aa9-9eb1-12734d28f3cb/moxa-mc-1200-series-linux-manual-v1.0.pdf) for the detail steps.**

- **Change the network settings of Moxa MC-1200 series computer based on your network environment**

    Refer to the Changing the interfaces Configuration File of [Moxa MC-1200 series computer-linux-user-manual](https://www.moxa.com/getmedia/58efc9c5-5865-4aa9-9eb1-12734d28f3cb/moxa-mc-1200-series-linux-manual-v1.0.pdf) for the detail steps.

# Set up your Development Environment

## Tools Installation (IDEs, Toolchains, SDKs)

The operation system of Moxa MC-1200 series is a native 64-bits X86 Linux operating system. There is no need to install toolchains. You can install development tools in Moxa MC-1200 series computer directly.

Follow these steps to update the package menu:

1. Make sure a network connection is available.

2. Use apt-get update to update the Debian package list.

```bash
moxa@Moxa:~$ sudo apt-get update
```

3. Install the native compiler and necessary packages.

```bash
moxa@Moxa:~$ sudo apt-get install gcc build-essential flex bison automake
```

# Setup your AWS account and Permissions

Refer to the instructions at [Set up your AWS Account](https://docs.aws.amazon.com/iot/latest/developerguide/setting-up.html). Follow the steps outlined in these sections to create your account and a user and get started:

- Sign up for an AWS account and
- Create a user and grant permissions.
- Open the AWS IoT console

Pay special attention to the Notes.

# Create Resources in AWS IoT

Refer to the instructions at [Create AWS IoT Resources](https://docs.aws.amazon.com/iot/latest/developerguide/create-iot-resources.html). Follow the steps outlined in these sections to provision resources for your Moxa MC-1200 series computer:

- Create an AWS IoT Policy
- Create a thing object

Pay special attention to the Notes.

> **Important**
Before you continue to the next step, your Moxa computer must be configured, and running. The Moxa computer must be connected to the Internet and you will need to be able to access the computer by using its command line interface. Command line access can be through SSH terminal remote interface.

# Build the demo

Follow above section, **Accessing Moxa MC-1200 series** **computer Using a Linux/Windows PC or Mac,** using PuTTY to open a remote terminal to Moxa computer on **Linux/Windows PC or Mac** and perform the following instructions in that window. 

Refer to the instruction at [Install the required tools and libraries for the AWS IoT Device SDK](https://docs.aws.amazon.com/iot/latest/developerguide/connecting-to-existing-device.html#gs-device-sdk-tools) and [Install AWS IoT Device SDK](https://docs.aws.amazon.com/iot/latest/developerguide/connecting-to-existing-device.html#gs-device-install-sdk) for Python on Moxa MC-1200 series computer directly. Follow the steps outlined in these sections to install AWS IoT Device SDK for your Moxa computer:

- Update the operating system and install required libraries
- Install git
- Install the AWS IoT Device SDK for Python.

Note: Due to using Python, there is no need to compile/build any programs. And we perform all steps in Moxa computer, there is no need to load/upload any programs to it.

# Run the demo

Continue previous section, perform the instructions, [Install and run the sample app](https://docs.aws.amazon.com/iot/latest/developerguide/connecting-to-existing-device.html#gs-device-node-app-run), in that terminal window. 

To view the MQTT messages published by the sample app in the AWS IoT console, perform the instructions,[View messages from the sample app in the AWS IoT console](https://docs.aws.amazon.com/iot/latest/developerguide/connecting-to-existing-device.html#gs-device-view-msg).

# Debugging

1. Not able to login Moxa MC-1200 series computer's through SSH terminal.

    Connect a display monitor to the Moxa MC-1200 series computer, and then power it up. Once the system is ready, a login screen will appear on your monitor. Refer to Starting from a HDMI Console of [**Moxa MC-1200 series computer-linux-user-manual](https://www.moxa.com/getmedia/58efc9c5-5865-4aa9-9eb1-12734d28f3cb/moxa-mc-1200-series-linux-manual-v1.0.pdf)** for the detail steps. After login Moxa computer check following items:

    a. Check if IP address of LAN1/LAN2 is in the same subnet of your PC.

    b. Check if you are able to operate OS normally. If not, gather all error message when you operate OS and then [CONTACT US](https://www.moxa.com/en/support/technical-support)

2. Moxa computer is not able to access internet.

    a. Check if IP address, mask and gateway of LAN1/LAN2 are configured in /etc/network/interfaces properly.

    b. Check if routing is correct.

    c. Check if nameserver is configured in /etc/resolv.conf

# Troubleshooting

Still need assistance with your Moxa product? [CONTACT US](https://www.moxa.com/en/support/technical-support)
