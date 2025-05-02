# CoAP-Based-Communication-Frameworks-for-Latency-and-Reliability-Analysis-in-IoT-Networks

This repository contains a comprehensive implementation to analyze the performance of different IoT communication protocols under varying network conditions.

# Overview
The lab implements two distinct IoT communication environments to study the impact of different protocols and network qualities on message delivery performance:

# Environment 1: CoAP + HTTP

Device to Edge: CoAP protocol
Edge to Application: HTTP protocol


# Environment 2: CoAP + MQTT

Device to Edge: CoAP protocol
Edge to Application: MQTT protocol



# Features

- Complete setup scripts for all environments
- Performance measurement tools for latency analysis
- Network degradation simulation (packet loss: 0%, 3%, 5%, 10%)
- Comparison of reliability mechanisms:
  - Confirmable vs. Non-confirmable CoAP
  - MQTT QoS levels (0, 1, 2)



# Requirements

- Ubuntu/Debian Linux systems
- libcoap for CoAP server and client
- Node.js for HTTP server and CoAP-to-MQTT bridge
- Mosquitto MQTT broker and clients
- Wireshark for packet analysis


# Usage

- Set up the three VMs (Device, Edge, Application)
- Install required components (CoAP (libcoap), MQTT (Mosquitto/Paho), Wireshark, Node.js)
- Start services on each machine in the correct order
- Write measurement scripts to collect performance data
- Analyze results based on packet captures and latency observations
  
# Analysis Results
The project includes detailed analysis of:

- Protocol overhead comparison
- Latency measurements under different packet loss scenarios
- Impact of reliability mechanisms on performance
- Tradeoffs between different QoS levels

# Notes
The CoAP-to-MQTT bridge implements a 5-second polling interval to simulate realistic IoT sensor behavior, which significantly impacts the latency measurements. This design choice was made to reflect typical IoT deployment patterns rather than optimize for minimal latency.
