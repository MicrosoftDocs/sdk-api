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

# _IP_ADAPTER_INDEX_MAP structure


## -description



			The 
<b>IP_ADAPTER_INDEX_MAP</b> structure stores the interface index associated with a network adapter with IPv4 enabled together with the name of the network adapter.


## -struct-fields




### -field Index

The interface index associated with the network adapter.


### -field Name

A pointer to a Unicode string that contains the name of the adapter.


## -remarks



The 
<b>IP_ADAPTER_INDEX_MAP</b> structure is specific to network adapters with IPv4 enabled. 

An adapter index  may change when the adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.

On Windows Vista and later, the <b>Name</b> member of the <b>IP_ADAPTER_INDEX_MAP</b> structure may be a Unicode string of the GUID for the network interface (the string begins with the '{' character). 

This structure is defined in the <i>Ipexport.h</i> header file which is automatically included in the <i>Iphlpapi.h</i> header file. The <i>Ipexport.h</i> header file should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/d53c3821-00a0-4eaa-9a06-69ec7aa98d84">IP Helper
  Structures</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start
  Page</a>



<a href="https://msdn.microsoft.com/287a4574-0a0f-4f20-932b-22bb6f40401d">IP_INTERFACE_INFO</a>



<a href="https://msdn.microsoft.com/d937ea44-1ca3-49e0-913d-fb77888d05fc">IpReleaseAddress</a>



<a href="https://msdn.microsoft.com/25b1bf9f-3ae1-453c-baae-5f70ae46cd24">IpRenewAddress</a>
 

 

