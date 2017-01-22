---
layout: post
title:  "Introduction to USB"
date:   2017-01-22 11:00:00 +0530
categories: usb
---
### What is USB?

  - Achronym for Universal Serial Bus
  - Is an industry standard
  - Created in 1996
  - Defines cables, connectors, and communication protocols used in bus
    which is used for connections, commincation, and power supply between
    computer systems.

### USB Connectors

In general, there are 3 kinds of USB connectors:

  - Standard (normal USB flash drives)
  - Mini (now, deperecated)
  - Micro (used in mobile phones)

### USB Data transfer

There are 5 data transfer modes as of date:

Mode        | Version      | Speed     | Notes
:---------- | :----------- | :-------- | :-----
Low Speed   | 1.0          | 1.5 mbps  | Used in joysticks
Full Speed  | 1.1          | 12 mbps   | Used in disk drives, etc
High Speed  | 2.0          | 480 mbps  |
SuperSpeed  | 3.0          | 5 gbps    | Full-duplex communication, earlier it used to half-duplex
SuperSpeed+ | 3.1          | 10gbps    |


### USB Specifications

Here is USB specification timeline:

Version | When Released? | Supported Transfer Mode
:------ | :------------- | :----------------------
1.0     | January 1996   | Low Speed
1.1     | September 1998 | Full Speed
2.0     | April 2000     | High Speed
3.0     | November 2008  | SuperSpeed
3.1     | July 2013      | SuperSpeed+

### USB Architecture:

Following is basic architecture diagram for USB:

![USB Architure Diagram]({{site.url}}/assets/usb_architecture.svg)

### USB Devices

There are two extra types of peripheral devices, besides normal
USB devices:

  - Composite device
    - Consists of logical sub-devices (also called device functions)
    - Provides several functions
    - e.g., USB headset with built-in microphone

  - Compound device
    - Each logical device is assigned a separate address space
    - All the logical device connects to hub

#### Communications in Devices

  - Is based on pipes (endpoints)
  - Pipe is a connection from HC to a logical entity
  - USB device can have upto 32 endpoints (16 IN, 16 OUT)
  - Two types of pipes
    - Message
      - Used for control transfer
      - Are bi-directional
    - Stream
      - Used for data transfer
      - Are unidirectinal
      - 3 kinds of transfers
        - Isochronous
          - Guaranteed data rate, with possible data loss
        - Interrrupt
          - Bounded latency, pointing devices
        - Bulk
          - Large transfers, no guarantee for bandwidth or latency
