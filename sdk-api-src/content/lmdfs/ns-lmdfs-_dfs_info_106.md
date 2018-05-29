---
UID: NS:lmdfs._DFS_INFO_106
title: "_DFS_INFO_106"
author: windows-sdk-content
description: Contains the storage state and priority for a DFS root target or link target. This structure is only for use with the NetDfsSetInfo function.
old-location: dfs\dfs_info_106.htm
old-project: Dfs
ms.assetid: 12c114e4-f978-4423-85a8-ec0cf9c9e8c5
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: "*LPDFS_INFO_106, *PDFS_INFO_106, DFS_INFO_106, DFS_INFO_106 structure [Distributed File System], DFS_STORAGE_STATES, DFS_STORAGE_STATE_OFFLINE, DFS_STORAGE_STATE_ONLINE, LPDFS_INFO_106, LPDFS_INFO_106 structure pointer [Distributed File System], PDFS_INFO_106, PDFS_INFO_106 structure pointer [Distributed File System], _DFS_INFO_106, dfs.dfs_info_106, fs.dfs_info_106, lmdfs/DFS_INFO_106, lmdfs/LPDFS_INFO_106, lmdfs/PDFS_INFO_106, netmgmt.dfs_info_106"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: lmdfs.h
req.include-header: LmDfs.h, Lm.h
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
req.typenames: DFS_INFO_106, *PDFS_INFO_106, *LPDFS_INFO_106
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	LmDfs.h
api_name:
-	DFS_INFO_106
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _DFS_INFO_106 structure


## -description


Contains the storage state and priority for a DFS root target or link target. This structure is only for use with the <a href="https://msdn.microsoft.com/5526afa7-82bc-47c7-99d6-44e41ef772b1">NetDfsSetInfo</a> function.


## -struct-fields




### -field State

State of the target as one of the following values.



#### DFS_STORAGE_STATE_OFFLINE (0x00000001)

The DFS storage is offline.



#### DFS_STORAGE_STATE_ONLINE (0x00000002)

The DFS storage is online.



#### DFS_STORAGE_STATES (0x0000000F)

Mask value that indicates which storage flags are set.


### -field TargetPriority


<a href="https://msdn.microsoft.com/b8f645ab-e3b4-4e0f-809a-57e27ab1e641">DFS_TARGET_PRIORITY</a> structure that contains the specific priority class and rank of a DFS target.


## -see-also




<a href="https://msdn.microsoft.com/a29cde3e-483a-4658-94d4-27398f66abfb">Distributed File System (DFS) Functions</a>



<a href="https://msdn.microsoft.com/5526afa7-82bc-47c7-99d6-44e41ef772b1">NetDfsSetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>
 

 

