---
UID: NS:lmdfs._DFS_SUPPORTED_NAMESPACE_VERSION_INFO
title: "_DFS_SUPPORTED_NAMESPACE_VERSION_INFO"
author: windows-sdk-content
description: Contains version information for a DFS namespace.
old-location: dfs\dfs_supported_namespace_version_info.htm
tech.root: Dfs
ms.assetid: ee75c500-70c6-4dce-9d38-36cacd695746
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PDFS_SUPPORTED_NAMESPACE_VERSION_INFO, DFS_NAMESPACE_CAPABILITY_ABDE, DFS_SUPPORTED_NAMESPACE_VERSION_INFO, DFS_SUPPORTED_NAMESPACE_VERSION_INFO structure [Distributed File System], PDFS_SUPPORTED_NAMESPACE_VERSION_INFO, PDFS_SUPPORTED_NAMESPACE_VERSION_INFO structure pointer [Distributed File System], _DFS_SUPPORTED_NAMESPACE_VERSION_INFO, dfs.dfs_supported_namespace_version_info, fs.dfs_supported_namespace_version_info, lmdfs/DFS_SUPPORTED_NAMESPACE_VERSION_INFO, lmdfs/PDFS_SUPPORTED_NAMESPACE_VERSION_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - DFS_SUPPORTED_NAMESPACE_VERSION_INFO
product: Windows
targetos: Windows
req.typenames: DFS_SUPPORTED_NAMESPACE_VERSION_INFO, *PDFS_SUPPORTED_NAMESPACE_VERSION_INFO
req.redist: 
---

# _DFS_SUPPORTED_NAMESPACE_VERSION_INFO structure


## -description


Contains version information for a DFS namespace.


## -struct-fields




### -field DomainDfsMajorVersion

The major version of the domain-based DFS namespace.


### -field DomainDfsMinorVersion

 


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


#### - NamespaceMinorVersion

The minor version of the domain-based DFS namespace.


## -see-also




<a href="https://msdn.microsoft.com/b260e132-41fd-460b-87e6-c6e0490dc8b4">DFS_NAMESPACE_VERSION_ORIGIN</a>



<a href="https://msdn.microsoft.com/a29cde3e-483a-4658-94d4-27398f66abfb">Distributed File System Functions</a>



<a href="https://msdn.microsoft.com/c4ce8f50-f090-4783-b6c9-834d9e0c33de">NetDfsAddRootTarget</a>



<a href="https://msdn.microsoft.com/32ccf4a7-9d07-45e1-93db-29eddee01680">NetDfsGetSupportedNamespaceVersion</a>
 

 

