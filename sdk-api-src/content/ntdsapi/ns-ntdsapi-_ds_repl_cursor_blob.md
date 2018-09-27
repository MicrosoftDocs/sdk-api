---
UID: NS:ntdsapi._DS_REPL_CURSOR_BLOB
title: "_DS_REPL_CURSOR_BLOB"
author: windows-sdk-content
description: The DS_REPL_CURSOR_BLOB structure contains inbound replication state data with respect to all replicas of a given naming context.
old-location: ad\ds_repl_cursor_blob.htm
tech.root: ad
ms.assetid: c41e4737-5ef8-40ce-9af1-0afff7e11dc1
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: DS_REPL_CURSOR_BLOB, DS_REPL_CURSOR_BLOB structure [Active Directory], _DS_REPL_CURSOR_BLOB, ad.ds_repl_cursor_blob, ntdsapi/DS_REPL_CURSOR_BLOB
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntdsapi.h
api_name:
 - DS_REPL_CURSOR_BLOB
product: Windows
targetos: Windows
req.typenames: DS_REPL_CURSOR_BLOB
req.redist: 
---

# _DS_REPL_CURSOR_BLOB structure


## -description


The <b>DS_REPL_CURSOR_BLOB</b> structure contains inbound replication state data with respect to all replicas of a   given naming context. This structure is similar to the <a href="https://msdn.microsoft.com/0361a3e1-814c-4ef2-b574-2870a9289e52">DS_REPL_CURSOR_3</a> structure, but is obtained from the <a href="https://msdn.microsoft.com/32bc9909-e476-423c-bbb5-3978234457fd">Lightweight Directory Access Protocol API</a> functions when obtaining binary data for the <b>msDS-NCReplCursors</b> attribute.


## -struct-fields




### -field uuidSourceDsaInvocationID

Contains the invocation identifier of the originating server to which the <b>usnAttributeFilter</b> corresponds.


### -field usnAttributeFilter

Contains the maximum update sequence number to which the destination server can indicate that it has recorded all changes originated by the given server at update sequence numbers less than, or equal to, this update sequence number. This is used to filter changes at replication source servers that the destination server has already applied.


### -field ftimeLastSyncSuccess

Contains a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the date and time of the last successful synchronization operation.


### -field oszSourceDsaDN

Contains the offset, in bytes, from the address of this structure  to  a null-terminated Unicode string that contains the distinguished name of the directory service agent that corresponds to the source server to which this replication state data applies.


## -see-also




<a href="https://msdn.microsoft.com/0361a3e1-814c-4ef2-b574-2870a9289e52">DS_REPL_CURSOR_3</a>



<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>



<a href="https://msdn.microsoft.com/32bc9909-e476-423c-bbb5-3978234457fd">Lightweight Directory Access Protocol API</a>
 

 

