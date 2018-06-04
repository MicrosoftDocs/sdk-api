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

# _DS_REPL_KCC_DSA_FAILUREW_BLOB structure


## -description


The <b>DS_REPL_KCC_DSA_FAILUREW_BLOB</b> structure contains replication state data with respect to a specific inbound replication partner. This state data is compiled and used by the Knowledge Consistency Checker (KCC) to decide when alternate replication routes must be added to account for  unreachable servers.
  This structure is similar to the <a href="https://msdn.microsoft.com/7a7131ce-a647-4b3d-a9f3-091b6dcebff7">DS_REPL_KCC_DSA_FAILURE</a> structure, but is obtained from the <a href="https://msdn.microsoft.com/32bc9909-e476-423c-bbb5-3978234457fd">Lightweight Directory Access Protocol API</a> functions when obtaining binary data for the <b>msDS-ReplConnectionFailures</b> or <b>msDS-ReplLinkFailures</b> attribute.


## -struct-fields




### -field oszDsaDN

Contains the offset, in bytes, from the address of this structure  to  a null-terminated string that contains the  distinguished name of the directory system agent object in the directory that corresponds to the source server.


### -field uuidDsaObjGuid

Contains the <b>objectGuid</b> of the directory system agent object represented by the <b>oszDsaDN</b> member.


### -field ftimeFirstFailure

Contains a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure which the contents of depends on the requested binary replication data.



#### msDS-ReplConnectionFailures

Contains the date and time that the first failure occurred when replicating from the source server.



#### msDS-ReplLinkFailures

Contains the date and time of the last successful replication.


### -field cNumFailures

Contains the number of consecutive failures since the last successful replication.


### -field dwLastResult

Contains the error code associated with the most recent failure, or <b>ERROR_SUCCESS</b> if the specific error is unavailable.


## -see-also




<a href="https://msdn.microsoft.com/7a7131ce-a647-4b3d-a9f3-091b6dcebff7">DS_REPL_KCC_DSA_FAILURE</a>



<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>



<a href="https://msdn.microsoft.com/32bc9909-e476-423c-bbb5-3978234457fd">Lightweight Directory Access Protocol API</a>
 

 

