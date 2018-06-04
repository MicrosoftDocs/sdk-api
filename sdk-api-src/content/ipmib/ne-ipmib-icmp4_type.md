---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ICMP4_TYPE enumeration


## -description


The <b>ICMP4_TYPE</b> enumeration defines the set of Internet Control Message Protocol (ICMP) for IP version 4.0 (IPv4) message types.


## -enum-fields




### -field ICMP4_ECHO_REPLY

ICMP echo reply message.


### -field ICMP4_DST_UNREACH

The specified destination for the message is unreachable.


### -field ICMP4_SOURCE_QUENCH

ICMP source quench message.


### -field ICMP4_REDIRECT

ICMP redirection message.


### -field ICMP4_ECHO_REQUEST

ICMP echo redirection message.


### -field ICMP4_ROUTER_ADVERT

ICMP router advertisement message.


### -field ICMP4_ROUTER_SOLICIT

ICMP router solicitation message.


### -field ICMP4_TIME_EXCEEDED

The ICMPv6 message has timed out.


### -field ICMP4_PARAM_PROB

The IPv4 header is malformed or contains an incorrect value.


### -field ICMP4_TIMESTAMP_REQUEST

ICMP timestamp request message.


### -field ICMP4_TIMESTAMP_REPLY

ICMP timestamp reply message.


### -field ICMP4_MASK_REQUEST

ICMP mask request message.


### -field ICMP4_MASK_REPLY

ICMP mask reply message.


## -remarks



On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>ICMP4_TYPE</b> enumeration  is defined in the <i>Ipmib.h</i> header file not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i> which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.



