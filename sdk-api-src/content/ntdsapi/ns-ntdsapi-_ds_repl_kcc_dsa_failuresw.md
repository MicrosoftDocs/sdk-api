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

# _DS_REPL_KCC_DSA_FAILURESW structure


## -description


The <b>DS_REPL_KCC_DSA_FAILURES</b> structure contains an array of <a href="https://msdn.microsoft.com/7a7131ce-a647-4b3d-a9f3-091b6dcebff7">DS_REPL_KCC_DSA_FAILURE</a> structures, which in turn contain replication state data with respect to inbound replication partners, as returned by the 
<a href="https://msdn.microsoft.com/b7ab22fe-ed92-4213-9b66-2dd5526286fa">DsReplicaGetInfo</a> and <a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a> functions.


## -struct-fields




### -field cNumEntries

Contains the number of elements in the <b>rgMetaData</b> array.


### -field dwReserved

Reserved for future use.


### -field rgDsaFailure.size_is

 


### -field rgDsaFailure.size_is.cNumEntries

 


### -field rgDsaFailure

Contains an array of <a href="https://msdn.microsoft.com/7a7131ce-a647-4b3d-a9f3-091b6dcebff7">DS_REPL_KCC_DSA_FAILURE</a> structures that contain the requested replication data. The <b>cNumEntries</b> member contains the number of elements in this array.


## -see-also




<a href="https://msdn.microsoft.com/7a7131ce-a647-4b3d-a9f3-091b6dcebff7">DS_REPL_KCC_DSA_FAILURE</a>



<a href="https://msdn.microsoft.com/b7ab22fe-ed92-4213-9b66-2dd5526286fa">DsReplicaGetInfo</a>



<a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a>
 

 

