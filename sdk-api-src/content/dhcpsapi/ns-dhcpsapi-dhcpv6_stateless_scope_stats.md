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

# DHCPV6_STATELESS_SCOPE_STATS structure


## -description


The <b>DHCPV6_STATELESS_SCOPE_STATS</b> structure defines the address counters for a specific IPv6 stateless subnet. The number of stateless IPv6 clients added and removed from the stateless client inventory are stored in this structure.




## -struct-fields




### -field SubnetAddress


<a href="https://msdn.microsoft.com/9623e866-81e5-4d5a-8801-33f0f8973ed3">DHCP_IPV6_ADDRESS</a> structure that specifies the IPv6 prefix of the DHCPv6 stateless scope.


### -field NumStatelessClientsAdded

Integer that specifies the number of IPv6 stateless clients that have been added to the DHCPv6 stateless client inventory for the prefix in <b>SubnetAddress</b>.


### -field NumStatelessClientsRemoved

Integer that specifies the number of IPv6 stateless clients that have been removed from the DHCPv6 stateless client inventory for the prefix in <b>SubnetAddress</b>.


## -see-also




<a href="https://msdn.microsoft.com/8C0E26F3-9496-497C-9E05-9995CC322189">DHCPV6_STATELESS_STATS</a>



<a href="https://msdn.microsoft.com/4f6ba79c-5ab5-4d89-907d-83bdddbd09a2">DhcpV6GetStatelessStatistics</a>
 

 

