---
UID: NE:lmdfs.__unnamed_enum_0
title: DFS_NAMESPACE_VERSION_ORIGIN (lmdfs.h)
author: windows-sdk-content
description: Identifies the origin of DFS namespace version information.
old-location: dfs\dfs_namespace_version_origin.htm
tech.root: Dfs
ms.assetid: b260e132-41fd-460b-87e6-c6e0490dc8b4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PDFS_NAMESPACE_VERSION_ORIGIN, DFS_NAMESPACE_VERSION_ORIGIN, DFS_NAMESPACE_VERSION_ORIGIN enumeration [Distributed File System], DFS_NAMESPACE_VERSION_ORIGIN_COMBINED, DFS_NAMESPACE_VERSION_ORIGIN_DOMAIN, DFS_NAMESPACE_VERSION_ORIGIN_SERVER, dfs.dfs_namespace_version_origin, fs.dfs_namespace_version_origin, lmdfs/DFS_NAMESPACE_VERSION_ORIGIN, lmdfs/DFS_NAMESPACE_VERSION_ORIGIN_COMBINED, lmdfs/DFS_NAMESPACE_VERSION_ORIGIN_DOMAIN, lmdfs/DFS_NAMESPACE_VERSION_ORIGIN_SERVER"
ms.topic: enum
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
product: Windows
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




<a href="https://msdn.microsoft.com/ee75c500-70c6-4dce-9d38-36cacd695746">DFS_SUPPORTED_NAMESPACE_VERSION_INFO</a>



<a href="https://msdn.microsoft.com/c4ce8f50-f090-4783-b6c9-834d9e0c33de">NetDfsAddRootTarget</a>



<a href="https://msdn.microsoft.com/32ccf4a7-9d07-45e1-93db-29eddee01680">NetDfsGetSupportedNamespaceVersion</a>
 

 

