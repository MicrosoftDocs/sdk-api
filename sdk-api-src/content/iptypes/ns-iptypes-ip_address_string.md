---
UID: NS:iptypes.IP_ADDRESS_STRING
title: IP_ADDRESS_STRING
author: windows-sdk-content
description: Stores an IPv4 address in dotted decimal notation.
old-location: iphlp\ip_address_string.htm
tech.root: IpHlp
ms.assetid: f426b22f-66e4-43e4-8852-357359df6f88
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PIP_ADDRESS_STRING, *PIP_ADDRESS_STRING,IP_MASK_STRING,*PIP_MASK_STRING, *PIP_ADDRESS_STRING,IP_MASK_STRING,*PIP_MASK_STRING structure [IP Helper], *PIP_MASK_STRING, IP_ADDRESS_STRING, IP_ADDRESS_STRING structure [IP Helper], IP_MASK_STRING, iphlp.ip_address_string, iptypes/*PIP_ADDRESS_STRING,IP_MASK_STRING,*PIP_MASK_STRING, iptypes/IP_ADDRESS_STRING"
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
 - IP_ADDRESS_STRING
product: Windows
targetos: Windows
req.typenames: IP_ADDRESS_STRING, *PIP_ADDRESS_STRING, IP_MASK_STRING, *PIP_MASK_STRING
req.redist: 
---

# IP_ADDRESS_STRING structure


## -description


The <b>IP_ADDRESS_STRING</b> structure stores an IPv4 address in dotted decimal notation. The <b>IP_ADDRESS_STRING</b> structure definition is also the type definition for the <b>IP_MASK_STRING</b> structure.


## -struct-fields




### -field String

A character string that represents an IPv4 address or an IPv4 subnet mask in dotted decimal notation.


## -remarks



The <b>IP_ADDRESS_STRING</b> structure is used as  a parameter in  the  <a href="https://msdn.microsoft.com/783c383d-7fd3-45bc-90f6-2e8ce01db3c3">IP_ADDR_STRING</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="https://msdn.microsoft.com/d53c3821-00a0-4eaa-9a06-69ec7aa98d84">IP Helper Structures</a>



<a href="https://msdn.microsoft.com/783c383d-7fd3-45bc-90f6-2e8ce01db3c3">IP_ADDR_STRING</a>
 

 

