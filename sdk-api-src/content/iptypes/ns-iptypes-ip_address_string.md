---
UID: NS:iptypes.__unnamed_struct_0
title: IP_ADDRESS_STRING (iptypes.h)
author: windows-sdk-content
description: Stores an IPv4 address in dotted decimal notation.
old-location: iphlp\ip_address_string.htm
tech.root: IpHlp
ms.assetid: f426b22f-66e4-43e4-8852-357359df6f88
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PIP_ADDRESS_STRING, *PIP_ADDRESS_STRING,IP_MASK_STRING,*PIP_MASK_STRING, *PIP_ADDRESS_STRING,IP_MASK_STRING,*PIP_MASK_STRING structure [IP Helper], *PIP_MASK_STRING, IP_ADDRESS_STRING, IP_ADDRESS_STRING structure [IP Helper], IP_MASK_STRING, iphlp.ip_address_string, iptypes/*PIP_ADDRESS_STRING,IP_MASK_STRING,*PIP_MASK_STRING, iptypes/IP_ADDRESS_STRING"
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
 - IP_ADDRESS_STRING
product: Windows
targetos: Windows
req.typenames: IP_ADDRESS_STRING, *PIP_ADDRESS_STRING, IP_MASK_STRING, *PIP_MASK_STRING
req.redist: 
ms.custom: 19H1
---

# IP_ADDRESS_STRING structure


## -description


The <b>IP_ADDRESS_STRING</b> structure stores an IPv4 address in dotted decimal notation. The <b>IP_ADDRESS_STRING</b> structure definition is also the type definition for the <b>IP_MASK_STRING</b> structure.


## -struct-fields




### -field String

A character string that represents an IPv4 address or an IPv4 subnet mask in dotted decimal notation.


## -remarks



The <b>IP_ADDRESS_STRING</b> structure is used as  a parameter in  the  <a href="https://docs.microsoft.com/windows/desktop/api/iptypes/ns-iptypes-_ip_addr_string">IP_ADDR_STRING</a> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="https://docs.microsoft.com/windows/desktop/IpHlp/ip-helper-structures">IP Helper Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iptypes/ns-iptypes-_ip_addr_string">IP_ADDR_STRING</a>
 

 

