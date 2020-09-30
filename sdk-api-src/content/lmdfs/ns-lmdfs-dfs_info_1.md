---
UID: NS:lmdfs._DFS_INFO_1
title: DFS_INFO_1 (lmdfs.h)
description: Contains the name of a Distributed File System (DFS) root or link.
helpviewer_keywords: ["*LPDFS_INFO_1","*PDFS_INFO_1","DFS_INFO_1","DFS_INFO_1 structure [Distributed File System]","LPDFS_INFO_1","LPDFS_INFO_1 structure pointer [Distributed File System]","PDFS_INFO_1","PDFS_INFO_1 structure pointer [Distributed File System]","_win32_dfs_info_1_str","dfs.dfs_info_1_str","fs.dfs_info_1_str","lmdfs/DFS_INFO_1","lmdfs/LPDFS_INFO_1","lmdfs/PDFS_INFO_1","netmgmt.dfs_info_1_str"]
old-location: dfs\dfs_info_1_str.htm
tech.root: Dfs
ms.assetid: 96647570-badd-4925-ab90-054a00ba04c4
ms.date: 12/05/2018
ms.keywords: '*LPDFS_INFO_1, *PDFS_INFO_1, DFS_INFO_1, DFS_INFO_1 structure [Distributed File System], LPDFS_INFO_1, LPDFS_INFO_1 structure pointer [Distributed File System], PDFS_INFO_1, PDFS_INFO_1 structure pointer [Distributed File System], _win32_dfs_info_1_str, dfs.dfs_info_1_str, fs.dfs_info_1_str, lmdfs/DFS_INFO_1, lmdfs/LPDFS_INFO_1, lmdfs/PDFS_INFO_1, netmgmt.dfs_info_1_str'
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
req.typenames: DFS_INFO_1, *PDFS_INFO_1, *LPDFS_INFO_1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DFS_INFO_1
 - lmdfs/_DFS_INFO_1
 - PDFS_INFO_1
 - lmdfs/PDFS_INFO_1
 - DFS_INFO_1
 - lmdfs/DFS_INFO_1
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
 - DFS_INFO_1
---

# DFS_INFO_1 structure


## -description

Contains the name of a Distributed File System (DFS) root or link. This structure is only for use with the 
    <a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsenum">NetDfsEnum</a>, 
    <a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo">NetDfsGetClientInfo</a>, and 
    <a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetinfo">NetDfsGetInfo</a> functions and the 
    <a href="/windows/desktop/dfs/fsctl-dfs-get-pkt-entry-state">FSCTL_DFS_GET_PKT_ENTRY_STATE</a> control 
    code.

## -struct-fields

### -field EntryPath

Pointer to a null-terminated Unicode string that specifies the Universal Naming Convention (UNC) path of a DFS root or link.

For a link, the string can be in one of two forms. The first form is as follows:

&#92;&#92;<i>ServerName</i>&#92;<i>DfsName</i>&#92;<i>link_path</i>

where <i>ServerName</i> is the name of the root target server that hosts the stand-alone DFS namespace; <i>DfsName</i> is the name of the DFS namespace; and <i>link_path</i> is a DFS link.

The second form is as follows:

&#92;&#92;<i>DomainName</i>&#92;<i>DomDfsname</i>&#92;<i>link_path</i>

where <i>DomainName</i> is the name of the domain that hosts the domain-based DFS namespace; <i>DomDfsname</i> is the name of the DFS namespace; and <i>link_path</i> is a DFS link.

For a root, the string can be in one of two forms:

&#92;&#92;<i>ServerName</i>&#92;<i>DfsName</i>

or

&#92;&#92;<i>DomainName</i>&#92;<i>DomDfsname</i>

where the values of the names are the same as those described previously.

## -remarks

The DFS functions use the 
<b>DFS_INFO_1</b> structure to retrieve information about a DFS root or link.

## -see-also

<a href="/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions">Distributed File System (DFS) Functions</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsenum">NetDfsEnum</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo">NetDfsGetClientInfo</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetinfo">NetDfsGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>