---
UID: NS:iptypes._IP_ADDR_STRING
title: IP_ADDR_STRING (iptypes.h)
author: windows-sdk-content
description: Represents a node in a linked-list of IPv4 addresses.
old-location: iphlp\ip_addr_string.htm
tech.root: IpHlp
ms.assetid: 783c383d-7fd3-45bc-90f6-2e8ce01db3c3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PIP_ADDR_STRING, IP_ADDR_STRING, IP_ADDR_STRING structure [IP Helper], PIP_ADDR_STRING, PIP_ADDR_STRING structure pointer [IP Helper], _iphlp_ip_addr_string, iphlp.ip_addr_string, iptypes/IP_ADDR_STRING, iptypes/PIP_ADDR_STRING"
ms.topic: struct
f1_keywords: 
 - "iptypes/IP_ADDR_STRING"
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
ms.custom: 19H1
---

# IP_ADDR_STRING structure


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
<a href="https://docs.microsoft.com/windows/desktop/api/iphlpapi/nf-iphlpapi-addipaddress">AddIPAddress</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/iphlpapi/nf-iphlpapi-deleteipaddress">DeleteIPAddress</a> functions.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/iphlpapi/nf-iphlpapi-addipaddress">AddIPAddress</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iphlpapi/nf-iphlpapi-deleteipaddress">DeleteIPAddress</a>



<a href="https://docs.microsoft.com/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="https://docs.microsoft.com/windows/desktop/IpHlp/ip-helper-structures">IP Helper Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iptypes/ns-iptypes-_ip_adapter_info">IP_ADAPTER_INFO</a>



<b>IP_ADDRESS_STRING</b>
 

 

