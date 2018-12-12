---
UID: NS:ipexport._IP_UNIDIRECTIONAL_ADAPTER_ADDRESS
title: IP_UNIDIRECTIONAL_ADAPTER_ADDRESS
author: windows-sdk-content
description: The IP_UNIDIRECTIONAL_ADAPTER_ADDRESS structure stores the IPv4 addresses associated with a unidirectional adapter.
old-location: iphlp\ip_unidirectional_adapter_address.htm
tech.root: IpHlp
ms.assetid: 225b93ae-e34f-4e5b-a699-1fdd342265c6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PIP_UNIDIRECTIONAL_ADAPTER_ADDRESS, IP_UNIDIRECTIONAL_ADAPTER_ADDRESS, IP_UNIDIRECTIONAL_ADAPTER_ADDRESS structure [IP Helper], PIP_UNIDIRECTIONAL_ADAPTER_ADDRESS, PIP_UNIDIRECTIONAL_ADAPTER_ADDRESS structure pointer [IP Helper], _iphlp_ip_unidirectional_adapter_address, ipexport/IP_UNIDIRECTIONAL_ADAPTER_ADDRESS, ipexport/PIP_UNIDIRECTIONAL_ADAPTER_ADDRESS, iphlp.ip_unidirectional_adapter_address"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IP_UNIDIRECTIONAL_ADAPTER_ADDRESS
product: Windows
targetos: Windows
req.typenames: IP_UNIDIRECTIONAL_ADAPTER_ADDRESS, *PIP_UNIDIRECTIONAL_ADAPTER_ADDRESS
req.redist: 
---

# IP_UNIDIRECTIONAL_ADAPTER_ADDRESS structure


## -description


The 
<b>IP_UNIDIRECTIONAL_ADAPTER_ADDRESS</b> structure stores the IPv4 addresses associated with a unidirectional adapter.


## -struct-fields




### -field NumAdapters

The number of IPv4 addresses pointed to by the <b>Address</b> member.


### -field Address

An array of variables of type <a href="https://msdn.microsoft.com/00d4823d-114d-4cc7-afdf-54c7fed3fe45">IPAddr</a>. Each element of the array specifies an IPv4 address associated with this unidirectional adapter.


## -remarks



The <b>IP_UNIDIRECTIONAL_ADAPTER_ADDRESS</b> structure is retrieved by the <a href="https://msdn.microsoft.com/32aa3a8e-ae74-4da9-bc8d-b28e270d9702">GetUnidirectionalAdapterInfo</a>function. A unidirectional adapter is an adapter that can receive
    IPv4 datagrams, but can't transmit them.





## -see-also




<a href="https://msdn.microsoft.com/32aa3a8e-ae74-4da9-bc8d-b28e270d9702">GetUnidirectionalAdapterInfo</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="https://msdn.microsoft.com/d53c3821-00a0-4eaa-9a06-69ec7aa98d84">IP Helper Structures</a>



<a href="https://msdn.microsoft.com/00d4823d-114d-4cc7-afdf-54c7fed3fe45">IPAddr</a>
 

 

