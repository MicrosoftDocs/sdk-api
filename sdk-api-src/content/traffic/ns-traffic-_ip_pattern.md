---
UID: NS:traffic._IP_PATTERN
title: "_IP_PATTERN"
author: windows-sdk-content
description: The IP_PATTERN structure applies a specific pattern or corresponding mask for the IP protocol. The IP_PATTERN structure designation is used by the traffic control interface in the application of packet filters.
old-location: qos\ip_pattern.htm
tech.root: QOS
ms.assetid: c8c3bd92-8120-4a3b-af8b-0a2c0a9bee0f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PIP_PATTERN, IP_PATTERN, IP_PATTERN structure [QOS], PIP_PATTERN, PIP_PATTERN structure pointer [QOS], _IP_PATTERN, _gqos_ip_pattern, qos.ip_pattern, traffic/IP_PATTERN, traffic/PIP_PATTERN"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: traffic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Traffic.h
api_name:
 - IP_PATTERN
product: Windows
targetos: Windows
req.typenames: IP_PATTERN, *PIP_PATTERN
req.redist: 
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
 

 

