---
UID: NS:ntdsapi._DS_REPL_CURSORS_3W
title: DS_REPL_CURSORS_3W
author: windows-sdk-content
description: The DS_REPL_CURSORS_3 structure is used with the DsReplicaGetInfo2 function to provide replication state data with respect to all replicas of a given naming context.
old-location: ad\ds_repl_cursors_3.htm
tech.root: ad
ms.assetid: 7b8e0015-dd8f-4cba-8ea2-683cb107f294
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DS_REPL_CURSORS_3, DS_REPL_CURSORS_3 structure [Active Directory], DS_REPL_CURSORS_3W, ad.ds_repl_cursors_3, ntdsapi/DS_REPL_CURSORS_3
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
 - DS_REPL_CURSORS_3
product: Windows
targetos: Windows
req.typenames: DS_REPL_CURSORS_3W
req.redist: 
---

# DS_REPL_CURSORS_3W structure


## -description


The <b>DS_REPL_CURSORS_3</b> structure is used with the <a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a> function to provide replication state data with respect to all replicas of a given naming context.


## -struct-fields




### -field cNumCursors

Contains  the number of elements in the <b>rgCursor</b> array.


### -field dwEnumerationContext

Contains the zero-based index of the next entry to retrieve if more entries are available. This value is passed for the <i>dwEnumerationContext</i> parameter in the next call to <a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a> to retrieve the next block of entries. If no more entries are available, this member contains -1.


### -field rgCursor.size_is

 


### -field rgCursor.size_is.cNumCursors

 


### -field rgCursor

Contains an array of <a href="https://msdn.microsoft.com/0361a3e1-814c-4ef2-b574-2870a9289e52">DS_REPL_CURSOR_3</a> structures that contain the requested replication data. The <b>cNumCursors</b> member contains the number of elements in this array.


## -see-also




<a href="https://msdn.microsoft.com/0361a3e1-814c-4ef2-b574-2870a9289e52">DS_REPL_CURSOR_3</a>



<a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a>
 

 

