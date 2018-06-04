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

# DHCPV6_STATELESS_STATS structure


## -description


The <b>DHCPV6_STATELESS_STATS</b> structure defines an array of stateless IPv6 subnet statistics.


## -struct-fields




### -field NumScopes

Integer that specifies the number of subnet statistics in <i>ScopeStats</i>.


### -field ScopeStats

Pointer to a list of <a href="https://msdn.microsoft.com/edb099a6-18eb-49b1-8f97-7f0b32a2430a">DHCPV6_STATELESS_SCOPE_STATS</a> structures.


### -field ScopeStats.size_is

 


### -field ScopeStats.size_is.NumScopes

 




## -see-also




<a href="https://msdn.microsoft.com/edb099a6-18eb-49b1-8f97-7f0b32a2430a">DHCPV6_STATELESS_SCOPE_STATS</a>



<a href="https://msdn.microsoft.com/4f6ba79c-5ab5-4d89-907d-83bdddbd09a2">DhcpV6GetStatelessStatistics</a>
 

 

