---
UID: NS:lmdfs._DFS_INFO_50
title: "_DFS_INFO_50"
author: windows-sdk-content
description: Contains the DFS metadata version and capabilities of an existing DFS namespace.
old-location: dfs\dfs_info_50.htm
old-project: Dfs
ms.assetid: 1af2866c-fe83-43fc-b4cc-9976157fb269
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: "*LPDFS_INFO_50, *PDFS_INFO_50, DFS_INFO_50, DFS_INFO_50 structure [Distributed File System], DFS_NAMESPACE_CAPABILITY_ABDE, PDFS_INFO_50, PDFS_INFO_50 structure pointer [Distributed File System], _DFS_INFO_50, dfs.dfs_info_50, fs.dfs_info_50, lmdfs/DFS_INFO_50, lmdfs/PDFS_INFO_50"
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
req.typenames: DFS_INFO_50, *PDFS_INFO_50, *LPDFS_INFO_50
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	LmDfs.h
api_name:
-	DFS_INFO_50
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _DFS_INFO_50 structure


## -description


Contains the DFS metadata version and capabilities of an existing DFS namespace. This 
     structure is only for use with the <a href="https://msdn.microsoft.com/bbb2f24d-1c49-4016-a16b-60fde4a78193">NetDfsGetInfo</a> 
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




<a href="https://msdn.microsoft.com/a29cde3e-483a-4658-94d4-27398f66abfb">Distributed File System Functions</a>



<a href="https://msdn.microsoft.com/bbb2f24d-1c49-4016-a16b-60fde4a78193">NetDfsGetInfo</a>
 

 

