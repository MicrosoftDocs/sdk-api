---
UID: NS:lmdfs._DFS_INFO_104
title: DFS_INFO_104 (lmdfs.h)
description: Contains the priority of a DFS root target or link target.
helpviewer_keywords: ["*LPDFS_INFO_104","*PDFS_INFO_104","DFS_INFO_104","DFS_INFO_104 structure [Distributed File System]","LPDFS_INFO_104","LPDFS_INFO_104 structure pointer [Distributed File System]","PDFS_INFO_104","PDFS_INFO_104 structure pointer [Distributed File System]","dfs.dfs_info_104","fs.dfs_info_104","lmdfs/DFS_INFO_104","lmdfs/LPDFS_INFO_104","lmdfs/PDFS_INFO_104","netmgmt.dfs_info_104"]
old-location: dfs\dfs_info_104.htm
tech.root: Dfs
ms.assetid: 95b2cd36-4933-440d-889d-ebf36d7b9cc7
ms.date: 12/05/2018
ms.keywords: '*LPDFS_INFO_104, *PDFS_INFO_104, DFS_INFO_104, DFS_INFO_104 structure [Distributed File System], LPDFS_INFO_104, LPDFS_INFO_104 structure pointer [Distributed File System], PDFS_INFO_104, PDFS_INFO_104 structure pointer [Distributed File System], dfs.dfs_info_104, fs.dfs_info_104, lmdfs/DFS_INFO_104, lmdfs/LPDFS_INFO_104, lmdfs/PDFS_INFO_104, netmgmt.dfs_info_104'
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
targetos: Windows
req.typenames: DFS_INFO_104, *PDFS_INFO_104, *LPDFS_INFO_104
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DFS_INFO_104
 - lmdfs/_DFS_INFO_104
 - PDFS_INFO_104
 - lmdfs/PDFS_INFO_104
 - DFS_INFO_104
 - lmdfs/DFS_INFO_104
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
 - DFS_INFO_104
---

# DFS_INFO_104 structure


## -description

Contains the priority of a DFS root target or link target. This structure is only for use with the <a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetinfo">NetDfsSetInfo</a> function.

## -struct-fields

### -field TargetPriority

<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_target_priority">DFS_TARGET_PRIORITY</a> structure that contains the specific priority class and rank of a DFS target.

## -see-also

<a href="/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions">Distributed File System (DFS) Functions</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetinfo">NetDfsSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>