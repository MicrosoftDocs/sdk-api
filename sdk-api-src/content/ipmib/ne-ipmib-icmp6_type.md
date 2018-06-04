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

# ICMP6_TYPE enumeration


## -description


The <b>ICMP6_TYPE</b> enumeration defines the set of Internet Control Message Protocol for IP version 6.0 (ICMPv6)  message types.


## -enum-fields




### -field ICMP6_DST_UNREACH

The specified destination for the message is unreachable.


### -field ICMP6_PACKET_TOO_BIG

The ICMPv6 packet is too large.


### -field ICMP6_TIME_EXCEEDED

The ICMPv6 message has timed out.


### -field ICMP6_PARAM_PROB

The IPv6 header is malformed or contains an incorrect value.


### -field ICMP6_ECHO_REQUEST

ICMPv6 echo request message.


### -field ICMP6_ECHO_REPLY

ICMPv6 echo reply message.


### -field ICMP6_MEMBERSHIP_QUERY

ICMPv6 group membership query message.


### -field ICMP6_MEMBERSHIP_REPORT

ICMPv6 group membership report message.


### -field ICMP6_MEMBERSHIP_REDUCTION

ICMPv6 group membership reduction message.


### -field ND_ROUTER_SOLICIT

ICMPv6 router solicitation message.


### -field ND_ROUTER_ADVERT

ICMPv6 router advertisement message.


### -field ND_NEIGHBOR_SOLICIT

ICMPv6 network neighbor solicitation message.


### -field ND_NEIGHBOR_ADVERT

ICMPv6 network neighbor advertisement message.


### -field ND_REDIRECT

ICMPv6 packet redirection message.


### -field ICMP6_V2_MEMBERSHIP_REPORT




## -remarks



On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>ICMP6_TYPE</b> enumeration  is defined in the <i>Ipmib.h</i> header file not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i> which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.



