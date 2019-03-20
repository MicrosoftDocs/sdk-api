---
UID: NS:lmdfs._DFS_STORAGE_INFO_1
title: DFS_STORAGE_INFO_1 (lmdfs.h)
author: windows-sdk-content
description: Contains information about a DFS target, including the DFS target server name and share name as well as the target's state and priority.
old-location: dfs\dfs_storage_info_1.htm
tech.root: Dfs
ms.assetid: 777b9688-9e34-48dd-bc8c-df17bef396d0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPDFS_STORAGE_INFO_1, *PDFS_STORAGE_INFO_1, DFS_STORAGE_INFO_1, DFS_STORAGE_INFO_1 structure [Distributed File System], DFS_STORAGE_STATES, DFS_STORAGE_STATE_OFFLINE, DFS_STORAGE_STATE_ONLINE, LPDFS_STORAGE_INFO_1, LPDFS_STORAGE_INFO_1 structure pointer [Distributed File System], PDFS_STORAGE_INFO_1, PDFS_STORAGE_INFO_1 structure pointer [Distributed File System], dfs.dfs_storage_info_1, fs.dfs_storage_info_1, lmdfs/DFS_STORAGE_INFO_1, lmdfs/LPDFS_STORAGE_INFO_1, lmdfs/PDFS_STORAGE_INFO_1, netmgmt.dfs_storage_info_1"
ms.topic: struct
req.header: lmdfs.h
req.include-header: LmDfs.h, Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008, Windows Server 2008
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
 - LmDfs.h
api_name:
 - DFS_STORAGE_INFO_1
product: Windows
targetos: Windows
req.typenames: DFS_STORAGE_INFO_1, *PDFS_STORAGE_INFO_1, *LPDFS_STORAGE_INFO_1
req.redist: 
---

# DFS_STORAGE_INFO_1 structure


## -description


Contains information about a DFS target, including the DFS target server name and share name as well as the target's state and priority.


## -struct-fields




### -field State

State of the target. This member can be one of the following values.



#### DFS_STORAGE_STATE_OFFLINE (0x00000001)

The DFS storage is offline.



#### DFS_STORAGE_STATE_ONLINE (0x00000002)

The DFS storage is online.



#### DFS_STORAGE_STATES (0x0000000F)

Mask value that indicates which storage flags are set.


### -field ServerName

Pointer to a null-terminated Unicode string that specifies the DFS root target or link target server name.


### -field ShareName

Pointer to a null-terminated Unicode string that specifies the DFS root target or link target share name.


### -field TargetPriority


<a href="https://msdn.microsoft.com/b8f645ab-e3b4-4e0f-809a-57e27ab1e641">DFS_TARGET_PRIORITY</a> structure that contains a DFS target's priority class and rank.


## -remarks



This structure is used as the <b>Storage</b> member of the <a href="https://msdn.microsoft.com/96a9c5eb-f79f-4577-b320-ebacff84fcc4">DFS_INFO_6</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/96a9c5eb-f79f-4577-b320-ebacff84fcc4">DFS_INFO_6</a>
 

 

