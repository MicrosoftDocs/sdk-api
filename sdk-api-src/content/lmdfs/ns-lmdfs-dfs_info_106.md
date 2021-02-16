---
UID: NS:lmdfs._DFS_INFO_106
title: DFS_INFO_106 (lmdfs.h)
description: Contains the storage state and priority for a DFS root target or link target. This structure is only for use with the NetDfsSetInfo function.
helpviewer_keywords: ["*LPDFS_INFO_106","*PDFS_INFO_106","DFS_INFO_106","DFS_INFO_106 structure [Distributed File System]","DFS_STORAGE_STATES","DFS_STORAGE_STATE_OFFLINE","DFS_STORAGE_STATE_ONLINE","LPDFS_INFO_106","LPDFS_INFO_106 structure pointer [Distributed File System]","PDFS_INFO_106","PDFS_INFO_106 structure pointer [Distributed File System]","dfs.dfs_info_106","fs.dfs_info_106","lmdfs/DFS_INFO_106","lmdfs/LPDFS_INFO_106","lmdfs/PDFS_INFO_106","netmgmt.dfs_info_106"]
old-location: dfs\dfs_info_106.htm
tech.root: Dfs
ms.assetid: 12c114e4-f978-4423-85a8-ec0cf9c9e8c5
ms.date: 12/05/2018
ms.keywords: '*LPDFS_INFO_106, *PDFS_INFO_106, DFS_INFO_106, DFS_INFO_106 structure [Distributed File System], DFS_STORAGE_STATES, DFS_STORAGE_STATE_OFFLINE, DFS_STORAGE_STATE_ONLINE, LPDFS_INFO_106, LPDFS_INFO_106 structure pointer [Distributed File System], PDFS_INFO_106, PDFS_INFO_106 structure pointer [Distributed File System], dfs.dfs_info_106, fs.dfs_info_106, lmdfs/DFS_INFO_106, lmdfs/LPDFS_INFO_106, lmdfs/PDFS_INFO_106, netmgmt.dfs_info_106'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DFS_INFO_106, *PDFS_INFO_106, *LPDFS_INFO_106
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DFS_INFO_106
 - lmdfs/_DFS_INFO_106
 - PDFS_INFO_106
 - lmdfs/PDFS_INFO_106
 - DFS_INFO_106
 - lmdfs/DFS_INFO_106
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - LmDfs.h
api_name:
 - DFS_INFO_106
---

# DFS_INFO_106 structure


## -description

Contains the storage state and priority for a DFS root target or link target. This structure is only for use with the <a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetinfo">NetDfsSetInfo</a> function.

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

<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_target_priority">DFS_TARGET_PRIORITY</a> structure that contains the specific priority class and rank of a DFS target.

## -see-also

<a href="/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions">Distributed File System (DFS) Functions</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetinfo">NetDfsSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>