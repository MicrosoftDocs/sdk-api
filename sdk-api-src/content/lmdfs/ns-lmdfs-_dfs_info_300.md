---
UID: NS:lmdfs._DFS_INFO_300
title: "_DFS_INFO_300"
author: windows-sdk-content
description: Contains the name and type (domain-based or stand-alone) of a DFS namespace.
old-location: dfs\dfs_info_300_str.htm
old-project: Dfs
ms.assetid: b418517a-9313-49e9-a679-69b02f4ee37f
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: "*LPDFS_INFO_300, *PDFS_INFO_300, DFS_INFO_300, DFS_INFO_300 structure [Distributed File System], DFS_VOLUME_FLAVOR_AD_BLOB, DFS_VOLUME_FLAVOR_STANDALONE, LPDFS_INFO_300, LPDFS_INFO_300 structure pointer [Distributed File System], PDFS_INFO_300, PDFS_INFO_300 structure pointer [Distributed File System], _DFS_INFO_300, _win32_dfs_info_300_str, dfs.dfs_info_300_str, fs.dfs_info_300_str, lmdfs/DFS_INFO_300, lmdfs/LPDFS_INFO_300, lmdfs/PDFS_INFO_300, netmgmt.dfs_info_300_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: DFS_INFO_300, *PDFS_INFO_300, *LPDFS_INFO_300
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - LmDfs.h
api_name:
 - DFS_INFO_300
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _DFS_INFO_300 structure


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

\<i>ServerName</i>\<i>DfsName</i>

where <i>ServerName</i> is the name of the root target server that hosts the stand-alone DFS namespace and <i>DfsName</i> is the name of the DFS namespace.

The second format is:

\<i>DomainName</i>\<i>DomDfsName</i>

where <i>DomainName</i> is the name of the domain that hosts the domain-based DFS namespace and <i>DomDfsname</i> is the name of the DFS namespace.


## -remarks



The DFS functions use the 
<b>DFS_INFO_300</b> structure to enumerate DFS namespaces hosted on a machine.




## -see-also




<a href="https://msdn.microsoft.com/a29cde3e-483a-4658-94d4-27398f66abfb">Distributed File System (DFS) Functions</a>



<a href="https://msdn.microsoft.com/c05a8d78-41f4-4c19-a25e-ef4885869584">NetDfsEnum</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>
 

 

