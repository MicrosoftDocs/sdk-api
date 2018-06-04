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

# _DHCP_FAILOVER_RELATIONSHIP_ARRAY structure


## -description


The <b>DHCP_FAILOVER_RELATIONSHIP_ARRAY</b> structure defines an array of DHCPv4 failover relationships between partner servers.


## -struct-fields




### -field NumElements

 


### -field pRelationships

Pointer to an array of <a href="https://msdn.microsoft.com/b409b0ff-2fdc-416c-a7ce-2cba9cf75122">DHCP_FAILOVER_RELATIONSHIP</a>  structures.


### -field pRelationships.size_is

 


### -field pRelationships.size_is.NumElements

 




#### - numElements

Integer that specifies the number of DHCPv4 failover relationships in <b>pRelationships.</b>


## -see-also




<a href="https://msdn.microsoft.com/81ef2af8-c1a9-44e7-857c-1591947609ed">DhcpV4FailoverEnumRelationship</a>
 

 

