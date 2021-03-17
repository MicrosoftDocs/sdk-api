---
UID: NS:lmdfs._DFS_INFO_100
title: DFS_INFO_100 (lmdfs.h)
description: Contains a comment associated with a Distributed File System (DFS) root or link.
helpviewer_keywords: ["*LPDFS_INFO_100","*PDFS_INFO_100","DFS_INFO_100","DFS_INFO_100 structure [Distributed File System]","LPDFS_INFO_100","LPDFS_INFO_100 structure pointer [Distributed File System]","PDFS_INFO_100","PDFS_INFO_100 structure pointer [Distributed File System]","_win32_dfs_info_100_str","dfs.dfs_info_100_str","fs.dfs_info_100_str","lmdfs/DFS_INFO_100","lmdfs/LPDFS_INFO_100","lmdfs/PDFS_INFO_100","netmgmt.dfs_info_100_str"]
old-location: dfs\dfs_info_100_str.htm
tech.root: Dfs
ms.assetid: 763ba0f0-01e9-47cf-bbe5-93e13aa83aa0
ms.date: 12/05/2018
ms.keywords: '*LPDFS_INFO_100, *PDFS_INFO_100, DFS_INFO_100, DFS_INFO_100 structure [Distributed File System], LPDFS_INFO_100, LPDFS_INFO_100 structure pointer [Distributed File System], PDFS_INFO_100, PDFS_INFO_100 structure pointer [Distributed File System], _win32_dfs_info_100_str, dfs.dfs_info_100_str, fs.dfs_info_100_str, lmdfs/DFS_INFO_100, lmdfs/LPDFS_INFO_100, lmdfs/PDFS_INFO_100, netmgmt.dfs_info_100_str'
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
req.typenames: DFS_INFO_100, *PDFS_INFO_100, *LPDFS_INFO_100
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DFS_INFO_100
 - lmdfs/_DFS_INFO_100
 - PDFS_INFO_100
 - lmdfs/PDFS_INFO_100
 - DFS_INFO_100
 - lmdfs/DFS_INFO_100
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
 - DFS_INFO_100
---

# DFS_INFO_100 structure


## -description

Contains a comment associated with a Distributed File System (DFS) root or link.

## -struct-fields

### -field Comment

Pointer to a null-terminated Unicode string that contains the comment associated with the specified DFS 
      root or link. The comment is associated with the DFS namespace root or link and not with a specific DFS root 
      target or link target.

## -remarks

The DFS functions use the <b>DFS_INFO_100</b> structure to 
    retrieve and set information about a DFS root or link.

## -see-also

<a href="/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions">Distributed File System (DFS) Functions</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetinfo">NetDfsGetInfo</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetinfo">NetDfsSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>