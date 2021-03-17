---
UID: NS:lmdfs._DFS_INFO_300
title: DFS_INFO_300 (lmdfs.h)
description: Contains the name and type (domain-based or stand-alone) of a DFS namespace.
helpviewer_keywords: ["*LPDFS_INFO_300","*PDFS_INFO_300","DFS_INFO_300","DFS_INFO_300 structure [Distributed File System]","DFS_VOLUME_FLAVOR_AD_BLOB","DFS_VOLUME_FLAVOR_STANDALONE","LPDFS_INFO_300","LPDFS_INFO_300 structure pointer [Distributed File System]","PDFS_INFO_300","PDFS_INFO_300 structure pointer [Distributed File System]","_win32_dfs_info_300_str","dfs.dfs_info_300_str","fs.dfs_info_300_str","lmdfs/DFS_INFO_300","lmdfs/LPDFS_INFO_300","lmdfs/PDFS_INFO_300","netmgmt.dfs_info_300_str"]
old-location: dfs\dfs_info_300_str.htm
tech.root: Dfs
ms.assetid: b418517a-9313-49e9-a679-69b02f4ee37f
ms.date: 12/05/2018
ms.keywords: '*LPDFS_INFO_300, *PDFS_INFO_300, DFS_INFO_300, DFS_INFO_300 structure [Distributed File System], DFS_VOLUME_FLAVOR_AD_BLOB, DFS_VOLUME_FLAVOR_STANDALONE, LPDFS_INFO_300, LPDFS_INFO_300 structure pointer [Distributed File System], PDFS_INFO_300, PDFS_INFO_300 structure pointer [Distributed File System], _win32_dfs_info_300_str, dfs.dfs_info_300_str, fs.dfs_info_300_str, lmdfs/DFS_INFO_300, lmdfs/LPDFS_INFO_300, lmdfs/PDFS_INFO_300, netmgmt.dfs_info_300_str'
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
req.typenames: DFS_INFO_300, *PDFS_INFO_300, *LPDFS_INFO_300
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DFS_INFO_300
 - lmdfs/_DFS_INFO_300
 - PDFS_INFO_300
 - lmdfs/PDFS_INFO_300
 - DFS_INFO_300
 - lmdfs/DFS_INFO_300
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
 - DFS_INFO_300
---

# DFS_INFO_300 structure


## -description

Contains the name and type (domain-based or stand-alone) of a DFS namespace.

## -struct-fields

### -field Flags

Value that specifies the type of the DFS namespace. This member can be one of the following values.



#### DFS_VOLUME_FLAVOR_STANDALONE (0x00000100)

Specifies a stand-alone DFS namespace.



#### DFS_VOLUME_FLAVOR_AD_BLOB (0x00000200)

Specifies a domain-based DFS namespace.

### -field DfsName

Pointer to a null-terminated Unicode string that contains the name of a DFS namespace. This member can have one of the following two formats.

The first format is:

&#92;<i>ServerName</i>&#92;<i>DfsName</i>

where <i>ServerName</i> is the name of the root target server that hosts the stand-alone DFS namespace and <i>DfsName</i> is the name of the DFS namespace.

The second format is:

&#92;<i>DomainName</i>&#92;<i>DomDfsName</i>

where <i>DomainName</i> is the name of the domain that hosts the domain-based DFS namespace and <i>DomDfsname</i> is the name of the DFS namespace.

## -remarks

The DFS functions use the 
<b>DFS_INFO_300</b> structure to enumerate DFS namespaces hosted on a machine.

## -see-also

<a href="/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions">Distributed File System (DFS) Functions</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsenum">NetDfsEnum</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>