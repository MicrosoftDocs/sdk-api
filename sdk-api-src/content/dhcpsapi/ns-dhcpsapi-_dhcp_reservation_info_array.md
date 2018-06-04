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

# _DHCP_RESERVATION_INFO_ARRAY structure


## -description


The <b>DHCP_RESERVATION_INFO_ARRAY</b> structure defines an array of IPv4 reservations for DHCPv4 clients.


## -struct-fields




### -field NumElements

Integer that specifies the number of IPv4 client reservations in <b>Elements</b>.


### -field Elements

Pointer to an array of <a href="https://msdn.microsoft.com/4f0110b5-3770-4aae-8df7-d2481eac3417">DHCP_IP_RESERVATION_INFO</a> structures that contain IPv4 client reservations.


### -field Elements.size_is

 


### -field Elements.size_is.NumElements

 




## -see-also




<a href="https://msdn.microsoft.com/6eebc858-7ffe-4bf3-b318-3a5ad16c9827">DhcpV4EnumSubnetReservations</a>
 

 

