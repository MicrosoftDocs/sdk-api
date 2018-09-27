---
UID: NS:ntdsapi._DS_REPL_CURSOR
title: "_DS_REPL_CURSOR"
author: windows-sdk-content
description: The DS_REPL_CURSOR structure contains inbound replication state data with respect to all replicas of a given naming context, as returned by the DsReplicaGetInfo and DsReplicaGetInfo2 functions.
old-location: ad\ds_repl_cursor.htm
tech.root: ad
ms.assetid: ab4ee8d8-5ccd-4f3f-a1c0-de78c65a10d3
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: DS_REPL_CURSOR, DS_REPL_CURSOR structure [Active Directory], _DS_REPL_CURSOR, _glines_ds_repl_cursor, ad.ds__repl__cursor, ad.ds_repl_cursor, ntdsapi/DS_REPL_CURSOR
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
 - DS_REPL_CURSOR
product: Windows
targetos: Windows
req.typenames: DS_REPL_CURSOR
req.redist: 
---

# _DS_REPL_CURSOR structure


## -description


The <b>DS_REPL_CURSOR</b> structure contains inbound replication state data with respect to all replicas of a given naming context, as returned by the 
<a href="https://msdn.microsoft.com/b7ab22fe-ed92-4213-9b66-2dd5526286fa">DsReplicaGetInfo</a> and <a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a> functions.


## -struct-fields




### -field uuidSourceDsaInvocationID

Contains the invocation identifier of the originating server to which the <b>usnAttributeFilter</b> corresponds.


### -field usnAttributeFilter

Contains the maximum update sequence number to which the destination server can indicate that it has recorded all changes originated by the given server at update sequence numbers less than, or equal to, this update sequence number. This is used to filter changes at replication source servers that the destination server has already applied.


## -see-also




<a href="https://msdn.microsoft.com/0fe5ad72-d3f3-42a8-a36f-ca1fc9c55c50">DS_REPL_CURSORS</a>



<a href="https://msdn.microsoft.com/b7ab22fe-ed92-4213-9b66-2dd5526286fa">DsReplicaGetInfo</a>



<a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a>
 

 

