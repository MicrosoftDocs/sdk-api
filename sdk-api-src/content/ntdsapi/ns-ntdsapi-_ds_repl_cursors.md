---
UID: NS:ntdsapi._DS_REPL_CURSORS
title: "_DS_REPL_CURSORS"
author: windows-sdk-content
description: The DS_REPL_CURSORS structure is used with the DsReplicaGetInfo and DsReplicaGetInfo2 function to provide replication state data with respect to all replicas of a given naming context.
old-location: ad\ds_repl_cursors.htm
old-project: ad
ms.assetid: 0fe5ad72-d3f3-42a8-a36f-ca1fc9c55c50
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: DS_REPL_CURSORS, DS_REPL_CURSORS structure [Active Directory], _DS_REPL_CURSORS, _glines_ds_repl_cursors, ad.ds__repl__cursors, ad.ds_repl_cursors, ntdsapi/DS_REPL_CURSORS
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
tech.root: 
req.typenames: DS_REPL_CURSORS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntdsapi.h
api_name:
 - DS_REPL_CURSORS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _DS_REPL_CURSORS structure


## -description


The <b>DS_REPL_CURSORS</b> structure is used with the <a href="https://msdn.microsoft.com/b7ab22fe-ed92-4213-9b66-2dd5526286fa">DsReplicaGetInfo</a> and <a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a> function to provide replication state data with respect to all replicas of a given naming context.


## -struct-fields




### -field cNumCursors

Contains  the number of elements in the <b>rgCursor</b> array.


### -field dwReserved

Reserved for future use.


### -field rgCursor.size_is

 


### -field rgCursor.size_is.cNumCursors

 


### -field rgCursor

Contains an array of <a href="https://msdn.microsoft.com/ab4ee8d8-5ccd-4f3f-a1c0-de78c65a10d3">DS_REPL_CURSOR</a> structures that contain the requested replication data. The <b>cNumCursors</b> member contains the number of elements in this array.


## -see-also




<a href="https://msdn.microsoft.com/ab4ee8d8-5ccd-4f3f-a1c0-de78c65a10d3">DS_REPL_CURSOR</a>



<a href="https://msdn.microsoft.com/b7ab22fe-ed92-4213-9b66-2dd5526286fa">DsReplicaGetInfo</a>



<a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a>
 

 

