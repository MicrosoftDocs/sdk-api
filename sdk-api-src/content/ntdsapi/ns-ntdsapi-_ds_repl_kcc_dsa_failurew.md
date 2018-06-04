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

# _DS_REPL_KCC_DSA_FAILUREW structure


## -description


The <b>DS_REPL_KCC_DSA_FAILURE</b> structure contains replication state data about a specific inbound replication partner, as returned by the 
<a href="https://msdn.microsoft.com/b7ab22fe-ed92-4213-9b66-2dd5526286fa">DsReplicaGetInfo</a> and <a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a> function. This state data is compiled and used by the Knowledge Consistency Checker (KCC) to decide when alternate replication routes must be added to account for unreachable servers.


## -struct-fields




### -field pszDsaDN

Pointer to a null-terminated string that contains the  distinguished name of the directory system agent object in the directory that corresponds to the source server.


### -field uuidDsaObjGuid

Contains the <b>objectGuid</b> of the directory system agent object represented by the <b>pszDsaDN</b> member.


### -field ftimeFirstFailure

Contains a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure which the contents of depends on the value passed for the <i>InfoType</i> parameter when <a href="https://msdn.microsoft.com/b7ab22fe-ed92-4213-9b66-2dd5526286fa">DsReplicaGetInfo</a> or <a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a> function was called.



#### DS_REPL_INFO_KCC_DSA_CONNECT_FAILURES

Contains the date and time that the first failure occurred when replicating from the source server.



#### DS_REPL_INFO_KCC_DSA_LINK_FAILURES

Contains the date and time of the last successful replication.


### -field cNumFailures

Contains the number of consecutive failures since the last successful replication.


### -field dwLastResult

Contains the error code associated with the most recent failure, or <b>ERROR_SUCCESS</b> if the specific error is unavailable.


## -see-also




<a href="https://msdn.microsoft.com/bb011502-38ae-43b7-a6ad-de16b499f61b">DS_REPL_KCC_DSA_FAILURES</a>



<a href="https://msdn.microsoft.com/b7ab22fe-ed92-4213-9b66-2dd5526286fa">DsReplicaGetInfo</a>



<a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a>



<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>
 

 

