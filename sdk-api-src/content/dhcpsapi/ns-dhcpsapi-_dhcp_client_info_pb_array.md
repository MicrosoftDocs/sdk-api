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

# _DHCP_CLIENT_INFO_PB_ARRAY structure


## -description


The <b>DHCP_CLIENT_INFO_PB_ARRAY</b> structure defines an array of DHCPv4 client information elements.


## -struct-fields




### -field NumElements

Integer that contains the number of DHCPv4 clients in <b>Clients</b>.


### -field Clients

Pointer to an array of <a href="https://msdn.microsoft.com/3ee224fb-650f-4468-848b-960424202ac3">DHCP_CLIENT_INFO_PB</a> structures that contain DHCPv4 client information.


### -field Clients.size_is

 


### -field Clients.size_is.NumElements

 




## -see-also




<a href="https://msdn.microsoft.com/f6c6113b-fabd-4094-a160-8da7a139bdc4">DhcpV4EnumSubnetClients</a>
 

 

