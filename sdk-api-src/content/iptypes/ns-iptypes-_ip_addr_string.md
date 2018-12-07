---
UID: NS:iptypes._IP_ADDR_STRING
title: "_IP_ADDR_STRING"
author: windows-sdk-content
description: Represents a node in a linked-list of IPv4 addresses.
old-location: iphlp\ip_addr_string.htm
tech.root: IpHlp
ms.assetid: 783c383d-7fd3-45bc-90f6-2e8ce01db3c3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PIP_ADDR_STRING, IP_ADDR_STRING, IP_ADDR_STRING structure [IP Helper], PIP_ADDR_STRING, PIP_ADDR_STRING structure pointer [IP Helper], _IP_ADDR_STRING, _iphlp_ip_addr_string, iphlp.ip_addr_string, iptypes/IP_ADDR_STRING, iptypes/PIP_ADDR_STRING"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: iptypes.h
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
 - Iptypes.h
api_name:
 - IP_ADDR_STRING
product: Windows
targetos: Windows
req.typenames: IP_ADDR_STRING, *PIP_ADDR_STRING
req.redist: 
---

# _IP_ADDR_STRING structure


## -description


The 
<b>IP_ADDR_STRING</b> structure represents a node in a linked-list of IPv4 addresses.


## -struct-fields




### -field Next

A pointer to the next 
<b>IP_ADDR_STRING</b> structure in the list.


### -field IpAddress

A value that specifies a structure type with a single member, <b>String</b>. The <b>String</b> member is a <b>char</b> array of size 16. This array holds an IPv4 address in dotted decimal notation.


### -field IpMask

A value that specifies a structure type with a single member, <b>String</b>. The <b>String</b> member is a <b>char</b> array of size 16. This array holds the IPv4 subnet mask in dotted decimal notation.


### -field Context

A network table entry (NTE). This value corresponds to the <i>NTEContext</i> parameters in the 
<a href="https://msdn.microsoft.com/669264cd-a43c-4681-9416-2704d4232685">AddIPAddress</a> and 
<a href="https://msdn.microsoft.com/d7ed986d-d62e-4723-ab74-85c3edfdf4ff">DeleteIPAddress</a> functions.


## -see-also




<a href="https://msdn.microsoft.com/669264cd-a43c-4681-9416-2704d4232685">AddIPAddress</a>



<a href="https://msdn.microsoft.com/d7ed986d-d62e-4723-ab74-85c3edfdf4ff">DeleteIPAddress</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="https://msdn.microsoft.com/d53c3821-00a0-4eaa-9a06-69ec7aa98d84">IP Helper Structures</a>



<a href="https://msdn.microsoft.com/f8035801-ca0c-4d86-bfc5-8e2d746af1b4">IP_ADAPTER_INFO</a>



<b>IP_ADDRESS_STRING</b>
 

 

