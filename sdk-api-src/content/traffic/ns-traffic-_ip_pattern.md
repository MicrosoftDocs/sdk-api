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

# _IP_PATTERN structure


## -description


The 
<b>IP_PATTERN</b> structure applies a specific pattern or corresponding mask for the IP protocol. The 
<b>IP_PATTERN</b> structure designation is used by the traffic control interface in the application of packet filters.


## -struct-fields




### -field Reserved1

Reserved for future use.


### -field Reserved2

Reserved for future use.


### -field SrcAddr

Source address.


### -field DstAddr

Destination address.


### -field S_un


### -field S_un.S_un_ports



##### S_un_ports.s_srcport,s_dstport

Source port and destination port.


### -field S_un.S_un_ports.s_srcport

 


### -field S_un.S_un_ports.s_dstport

 


### -field S_un.S_un_icmp



##### S_un_icmp.s_type,s_code

ICMP message type and ICMP message code.


### -field S_un.S_un_icmp.s_type

 


### -field S_un.S_un_icmp.s_code

 


### -field S_un.S_un_icmp.filler

 


### -field S_un.S_Spi

Service provider interface.


### -field ProtocolId

Protocol identifier.


### -field Reserved3

Reserved for future use.


## -remarks



The following macros are defined in Traffic.h to make it easier to reference the members of the union: 

<pre class="syntax" xml:space="preserve"><code>#define tcSrcPort S_un.S_un_ports.s_srcport
#define tcDstPort S_un.S_un_ports.s_dstport
#define tcIcmpType        S_un.S_un_icmp.s_type
#define tcIcmpCode        S_un.S_un_icmp.s_code
#define tcSpi             S_un.S_Spi</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a>
 

 

