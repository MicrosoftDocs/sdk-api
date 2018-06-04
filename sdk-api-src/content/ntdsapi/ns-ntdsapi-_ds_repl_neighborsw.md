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

# _DS_REPL_NEIGHBORSW structure


## -description


The <b>DS_REPL_NEIGHBORS</b> structure is used with the <a href="https://msdn.microsoft.com/b7ab22fe-ed92-4213-9b66-2dd5526286fa">DsReplicaGetInfo</a> and <a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a> functions to provide inbound replication state data for naming context and source server pairs.


## -struct-fields




### -field cNumNeighbors

Contains  the number of elements in the <b>rgNeighbor</b> array.


### -field dwReserved

Reserved for future use.


### -field rgNeighbor.size_is

 


### -field rgNeighbor.size_is.cNumNeighbors

 


### -field rgNeighbor

Contains an array of <a href="https://msdn.microsoft.com/acab74f4-5739-4310-895b-081062c0360b">DS_REPL_NEIGHBOR</a> structures that contain the requested replication data. The <b>cNumNeighbors</b> member contains the number of elements in this array.


## -see-also




<a href="https://msdn.microsoft.com/acab74f4-5739-4310-895b-081062c0360b">DS_REPL_NEIGHBOR</a>



<a href="https://msdn.microsoft.com/b7ab22fe-ed92-4213-9b66-2dd5526286fa">DsReplicaGetInfo</a>



<a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a>
 

 

