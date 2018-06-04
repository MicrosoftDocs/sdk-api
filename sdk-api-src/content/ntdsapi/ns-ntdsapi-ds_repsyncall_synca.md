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

# DS_REPSYNCALL_SYNCA structure


## -description


The <b>DS_REPSYNCALL_SYNC</b> structure identifies a single replication operation performed between a source, and destination, server by the 
<a href="https://msdn.microsoft.com/2608adde-4f18-4048-a96f-d736ff09cd4b">DsReplicaSyncAll</a> function.


## -struct-fields




### -field pszSrcId

Pointer to a null-terminated string that specifies the DNS GUID of the source server.


### -field pszDstId

Pointer to a null-terminated string that specifies the DNS GUID of the destination server.


### -field pszNC

 


### -field pguidSrc

 


### -field pguidDst

 




## -see-also




<a href="https://msdn.microsoft.com/3b0005cb-0fb6-492c-89e5-8a18a88f881b">DS_REPSYNCALL_UPDATE</a>



<a href="https://msdn.microsoft.com/42b20d3b-1799-4f5f-b74e-fe9284dd8ac3">Domain Controller and Replication Management Structures</a>



<a href="https://msdn.microsoft.com/2608adde-4f18-4048-a96f-d736ff09cd4b">DsReplicaSyncAll</a>
 

 

