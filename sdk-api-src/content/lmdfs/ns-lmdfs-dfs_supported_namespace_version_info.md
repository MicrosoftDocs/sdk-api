---
UID: NS:lmdfs._DFS_SUPPORTED_NAMESPACE_VERSION_INFO
title: DFS_SUPPORTED_NAMESPACE_VERSION_INFO (lmdfs.h)
description: Contains version information for a DFS namespace.
helpviewer_keywords: ["*PDFS_SUPPORTED_NAMESPACE_VERSION_INFO","DFS_NAMESPACE_CAPABILITY_ABDE","DFS_SUPPORTED_NAMESPACE_VERSION_INFO","DFS_SUPPORTED_NAMESPACE_VERSION_INFO structure [Distributed File System]","PDFS_SUPPORTED_NAMESPACE_VERSION_INFO","PDFS_SUPPORTED_NAMESPACE_VERSION_INFO structure pointer [Distributed File System]","dfs.dfs_supported_namespace_version_info","fs.dfs_supported_namespace_version_info","lmdfs/DFS_SUPPORTED_NAMESPACE_VERSION_INFO","lmdfs/PDFS_SUPPORTED_NAMESPACE_VERSION_INFO"]
old-location: dfs\dfs_supported_namespace_version_info.htm
tech.root: Dfs
ms.assetid: ee75c500-70c6-4dce-9d38-36cacd695746
ms.date: 12/05/2018
ms.keywords: '*PDFS_SUPPORTED_NAMESPACE_VERSION_INFO, DFS_NAMESPACE_CAPABILITY_ABDE, DFS_SUPPORTED_NAMESPACE_VERSION_INFO, DFS_SUPPORTED_NAMESPACE_VERSION_INFO structure [Distributed File System], PDFS_SUPPORTED_NAMESPACE_VERSION_INFO, PDFS_SUPPORTED_NAMESPACE_VERSION_INFO structure pointer [Distributed File System], dfs.dfs_supported_namespace_version_info, fs.dfs_supported_namespace_version_info, lmdfs/DFS_SUPPORTED_NAMESPACE_VERSION_INFO, lmdfs/PDFS_SUPPORTED_NAMESPACE_VERSION_INFO'
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
req.typenames: DFS_SUPPORTED_NAMESPACE_VERSION_INFO, *PDFS_SUPPORTED_NAMESPACE_VERSION_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DFS_SUPPORTED_NAMESPACE_VERSION_INFO
 - lmdfs/_DFS_SUPPORTED_NAMESPACE_VERSION_INFO
 - PDFS_SUPPORTED_NAMESPACE_VERSION_INFO
 - lmdfs/PDFS_SUPPORTED_NAMESPACE_VERSION_INFO
 - DFS_SUPPORTED_NAMESPACE_VERSION_INFO
 - lmdfs/DFS_SUPPORTED_NAMESPACE_VERSION_INFO
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
 - DFS_SUPPORTED_NAMESPACE_VERSION_INFO
---

## -description

Contains version information for a DFS namespace.

## -struct-fields

### -field DomainDfsMajorVersion

The major version of the domain-based DFS namespace.

### -field DomainDfsMinorVersion

The minor version of the domain-based DFS namespace.

### -field DomainDfsCapabilities

Specifies a set of flags that describe specific capabilities of a domain-based DFS namespace.

#### DFS_NAMESPACE_CAPABILITY_ABDE (0x0000000000000001)

The DFS namespace supports associating a security descriptor with a DFS link for Access-Based Directory Enumeration (ABDE) purposes.

### -field StandaloneDfsMajorVersion

The major version of the stand-alone DFS namespace.

### -field StandaloneDfsMinorVersion

The minor version of the stand-alone DFS namespace.

### -field StandaloneDfsCapabilities

Specifies a set of flags that describe specific capabilities of a stand-alone DFS namespace.

#### DFS_NAMESPACE_CAPABILITY_ABDE (0x0000000000000001)

The DFS namespace supports associating a security descriptor with a DFS link for ABDE purposes.

## -see-also

<a href="/previous-versions/windows/desktop/api/lmdfs/ne-lmdfs-dfs_namespace_version_origin">DFS_NAMESPACE_VERSION_ORIGIN</a>

<a href="/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions">Distributed File System Functions</a>

<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddroottarget">NetDfsAddRootTarget</a>

<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsupportednamespaceversion">NetDfsGetSupportedNamespaceVersion</a>
