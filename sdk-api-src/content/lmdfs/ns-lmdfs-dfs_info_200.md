---
UID: NS:lmdfs._DFS_INFO_200
title: DFS_INFO_200 (lmdfs.h)
description: Contains the name of a domain-based Distributed File System (DFS) namespace.
helpviewer_keywords: ["*LPDFS_INFO_200","*PDFS_INFO_200","DFS_INFO_200","DFS_INFO_200 structure [Distributed File System]","LPDFS_INFO_200","LPDFS_INFO_200 structure pointer [Distributed File System]","PDFS_INFO_200","PDFS_INFO_200 structure pointer [Distributed File System]","_win32_dfs_info_200_str","dfs.dfs_info_200_str","fs.dfs_info_200_str","lmdfs/DFS_INFO_200","lmdfs/LPDFS_INFO_200","lmdfs/PDFS_INFO_200","netmgmt.dfs_info_200_str"]
old-location: dfs\dfs_info_200_str.htm
tech.root: Dfs
ms.assetid: a37a97b2-f2f2-45fc-9466-da75e273b075
ms.date: 12/05/2018
ms.keywords: '*LPDFS_INFO_200, *PDFS_INFO_200, DFS_INFO_200, DFS_INFO_200 structure [Distributed File System], LPDFS_INFO_200, LPDFS_INFO_200 structure pointer [Distributed File System], PDFS_INFO_200, PDFS_INFO_200 structure pointer [Distributed File System], _win32_dfs_info_200_str, dfs.dfs_info_200_str, fs.dfs_info_200_str, lmdfs/DFS_INFO_200, lmdfs/LPDFS_INFO_200, lmdfs/PDFS_INFO_200, netmgmt.dfs_info_200_str'
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
req.typenames: DFS_INFO_200, *PDFS_INFO_200, *LPDFS_INFO_200
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DFS_INFO_200
 - lmdfs/_DFS_INFO_200
 - PDFS_INFO_200
 - lmdfs/PDFS_INFO_200
 - DFS_INFO_200
 - lmdfs/DFS_INFO_200
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
 - DFS_INFO_200
---

# DFS_INFO_200 structure


## -description

Contains the name of a domain-based Distributed File System (DFS) namespace.

## -struct-fields

### -field FtDfsName

Pointer to a null-terminated Unicode string that contains the name of a domain-based DFS namespace.

## -remarks

The <b>DFS_INFO_200</b> structure is used to enumerate domain-based DFS namespaces in a domain.

## -see-also

<a href="/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions">Distributed File System (DFS) Functions</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsenum">NetDfsEnum</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>