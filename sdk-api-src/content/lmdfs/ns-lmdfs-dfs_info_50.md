---
UID: NS:lmdfs._DFS_INFO_50
title: DFS_INFO_50 (lmdfs.h)
description: Contains the DFS metadata version and capabilities of an existing DFS namespace.
helpviewer_keywords: ["*LPDFS_INFO_50","*PDFS_INFO_50","DFS_INFO_50","DFS_INFO_50 structure [Distributed File System]","DFS_NAMESPACE_CAPABILITY_ABDE","PDFS_INFO_50","PDFS_INFO_50 structure pointer [Distributed File System]","dfs.dfs_info_50","fs.dfs_info_50","lmdfs/DFS_INFO_50","lmdfs/PDFS_INFO_50"]
old-location: dfs\dfs_info_50.htm
tech.root: Dfs
ms.assetid: 1af2866c-fe83-43fc-b4cc-9976157fb269
ms.date: 12/05/2018
ms.keywords: '*LPDFS_INFO_50, *PDFS_INFO_50, DFS_INFO_50, DFS_INFO_50 structure [Distributed File System], DFS_NAMESPACE_CAPABILITY_ABDE, PDFS_INFO_50, PDFS_INFO_50 structure pointer [Distributed File System], dfs.dfs_info_50, fs.dfs_info_50, lmdfs/DFS_INFO_50, lmdfs/PDFS_INFO_50'
req.header: lmdfs.h
req.include-header: LmDfs.h, Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1
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
req.typenames: DFS_INFO_50, *PDFS_INFO_50, *LPDFS_INFO_50
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DFS_INFO_50
 - lmdfs/_DFS_INFO_50
 - PDFS_INFO_50
 - lmdfs/PDFS_INFO_50
 - DFS_INFO_50
 - lmdfs/DFS_INFO_50
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
 - DFS_INFO_50
---

# DFS_INFO_50 structure


## -description

Contains the DFS metadata version and capabilities of an existing DFS namespace. This 
     structure is only for use with the <a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetinfo">NetDfsGetInfo</a> 
     function.

## -struct-fields

### -field NamespaceMajorVersion

The major version of the DFS metadata.

### -field NamespaceMinorVersion

The minor version of the DFS metadata.

### -field NamespaceCapabilities

Specifies a set of flags that describe specific capabilities of a DFS namespace.



#### DFS_NAMESPACE_CAPABILITY_ABDE (0x0000000000000001)

The DFS namespace supports associating a security descriptor with a DFS link for Access-Based Directory 
        Enumeration (ABDE) purposes.

## -see-also

<a href="/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions">Distributed File System Functions</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetinfo">NetDfsGetInfo</a>