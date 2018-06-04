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

# _DHCPV4_FAILOVER_CLIENT_INFO_ARRAY structure


## -description


The <b>DHCPV4_FAILOVER_CLIENT_INFO_ARRAY</b> structure defines an array of DHCP server scope statistics that are part of a failover relationship.


## -struct-fields




### -field NumElements

Integer that specifies the number of DHCP server scope statistics in <b>Clients</b>.


### -field Clients

Pointer to an array of <a href="https://msdn.microsoft.com/46e4fb62-5b8e-44f8-b3a0-92535ca690f0">DHCPV4_FAILOVER_CLIENT_INFO</a>  structures.


### -field Clients.size_is

 


### -field Clients.size_is.NumElements

 



