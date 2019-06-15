---
UID: NS:ipexport.arp_send_reply
title: ARP_SEND_REPLY (ipexport.h)
author: windows-sdk-content
description: The ARP_SEND_REPLY structure stores information about an Address Resolution Protocol (ARP) reply messages.
old-location: iphlp\arp_send_reply.htm
tech.root: IpHlp
ms.assetid: 6495d289-b9b8-42cb-b00b-cde53d3dc91c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PARP_SEND_REPLY, *PARP_SEND_REPLY structure [IP Helper], ARP_SEND_REPLY, ARP_SEND_REPLY structure [IP Helper], ipexport/*PARP_SEND_REPLY, ipexport/ARP_SEND_REPLY, iphlp.arp_send_reply"
ms.topic: struct
req.header: ipexport.h
req.include-header: Iphlpapi.h
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
 - Ipexport.h
api_name:
 - ARP_SEND_REPLY
product: Windows
targetos: Windows
req.typenames: ARP_SEND_REPLY, *PARP_SEND_REPLY
req.redist: 
ms.custom: 19H1
---

# ARP_SEND_REPLY structure


## -description


The <b>ARP_SEND_REPLY</b> structure stores information about an Address Resolution Protocol (ARP) reply messages.


## -struct-fields




### -field DestAddress

 The destination  IPv4 address to which the ARP message is sent, in the form of an <a href="https://docs.microsoft.com/windows/desktop/api/inaddr/ns-inaddr-in_addr">IPAddr</a> structure.


### -field SrcAddress

The source IPv4 address from which the ARP message is being transmitted, in the form of an <a href="https://docs.microsoft.com/windows/desktop/api/inaddr/ns-inaddr-in_addr">IPAddr</a> structure.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="https://docs.microsoft.com/windows/desktop/IpHlp/ip-helper-structures">IP Helper Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/inaddr/ns-inaddr-in_addr">IPAddr</a>
 

 

