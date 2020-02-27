---
UID: NE:lmdfs.__unnamed_enum_0
title: DFS_NAMESPACE_VERSION_ORIGIN (lmdfs.h)
description: Identifies the origin of DFS namespace version information.
old-location: dfs\dfs_namespace_version_origin.htm
tech.root: Dfs
ms.assetid: b260e132-41fd-460b-87e6-c6e0490dc8b4
ms.date: 12/05/2018
ms.keywords: '*PDFS_NAMESPACE_VERSION_ORIGIN, DFS_NAMESPACE_VERSION_ORIGIN, DFS_NAMESPACE_VERSION_ORIGIN enumeration [Distributed File System], DFS_NAMESPACE_VERSION_ORIGIN_COMBINED, DFS_NAMESPACE_VERSION_ORIGIN_DOMAIN, DFS_NAMESPACE_VERSION_ORIGIN_SERVER, dfs.dfs_namespace_version_origin, fs.dfs_namespace_version_origin, lmdfs/DFS_NAMESPACE_VERSION_ORIGIN, lmdfs/DFS_NAMESPACE_VERSION_ORIGIN_COMBINED, lmdfs/DFS_NAMESPACE_VERSION_ORIGIN_DOMAIN, lmdfs/DFS_NAMESPACE_VERSION_ORIGIN_SERVER'
f1_keywords:
- lmdfs/DFS_NAMESPACE_VERSION_ORIGIN
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- LmDfs.h
api_name:
- DFS_NAMESPACE_VERSION_ORIGIN
targetos: Windows
req.typenames: DFS_NAMESPACE_VERSION_ORIGIN, *PDFS_NAMESPACE_VERSION_ORIGIN
req.redist: 
ms.custom: 19H1
---

# DFS_NAMESPACE_VERSION_ORIGIN enumeration


## -description


Identifies the origin of DFS namespace version information.


## -enum-fields




### -field DFS_NAMESPACE_VERSION_ORIGIN_COMBINED

The version information specifies the maximum version that the server and the Active Directory Domain Service (AD DS) domain can support.


### -field DFS_NAMESPACE_VERSION_ORIGIN_SERVER

The version information specifies the maximum version that the server can support.


### -field DFS_NAMESPACE_VERSION_ORIGIN_DOMAIN

The version information specifies the maximum version that the AD DS domain can support.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/lmdfs/ns-lmdfs-dfs_supported_namespace_version_info">DFS_SUPPORTED_NAMESPACE_VERSION_INFO</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddroottarget">NetDfsAddRootTarget</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsupportednamespaceversion">NetDfsGetSupportedNamespaceVersion</a>
 

 

