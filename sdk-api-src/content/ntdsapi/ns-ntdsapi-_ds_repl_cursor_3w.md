---
UID: NS:ntdsapi._DS_REPL_CURSOR_3W
title: "_DS_REPL_CURSOR_3W"
author: windows-sdk-content
description: The DS_REPL_CURSOR_3 structure contains inbound replication state data with respect to all replicas of a given naming context, as returned by the DsReplicaGetInfo2 function.
old-location: ad\ds_repl_cursor_3.htm
old-project: AD
ms.assetid: 0361a3e1-814c-4ef2-b574-2870a9289e52
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: DS_REPL_CURSOR_3, DS_REPL_CURSOR_3 structure [Active Directory], DS_REPL_CURSOR_3W, _DS_REPL_CURSOR_3W, ad.ds_repl_cursor_3, ntdsapi/DS_REPL_CURSOR_3
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DS_REPL_CURSOR_3W
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntdsapi.h
api_name:
-	DS_REPL_CURSOR_3
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _DS_REPL_CURSOR_3W structure


## -description


The <b>DS_REPL_CURSOR_3</b> structure contains inbound replication state data with respect to all replicas of a given naming context, as returned by the 
<a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a> function. This structure is an enhanced version of the <a href="https://msdn.microsoft.com/ab4ee8d8-5ccd-4f3f-a1c0-de78c65a10d3">DS_REPL_CURSOR</a> and <a href="https://msdn.microsoft.com/ff839372-41f0-499a-9582-59ace02f1485">DS_REPL_CURSOR_2</a> structures.


## -struct-fields




### -field uuidSourceDsaInvocationID

Contains the invocation identifier of the originating server to which the <b>usnAttributeFilter</b> corresponds.


### -field usnAttributeFilter

Contains the maximum update sequence number to which the destination server can indicate that it has recorded all changes originated by the given server at update sequence numbers less than, or equal to, this update sequence number. This is used to filter changes at replication source servers that the destination server has already applied.


### -field ftimeLastSyncSuccess

Contains a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the date and time of the last successful synchronization operation.


### -field pszSourceDsaDN

Pointer to  a null-terminated string that contains the distinguished name of the directory service agent that corresponds to the source server to which this replication state data applies.


## -see-also




<a href="https://msdn.microsoft.com/ab4ee8d8-5ccd-4f3f-a1c0-de78c65a10d3">DS_REPL_CURSOR</a>



<a href="https://msdn.microsoft.com/ff839372-41f0-499a-9582-59ace02f1485">DS_REPL_CURSOR_2</a>



<a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a>



<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>
 

 

