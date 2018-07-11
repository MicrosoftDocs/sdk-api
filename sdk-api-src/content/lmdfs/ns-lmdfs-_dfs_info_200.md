---
UID: NS:lmdfs._DFS_INFO_200
title: "_DFS_INFO_200"
author: windows-sdk-content
description: Contains the name of a domain-based Distributed File System (DFS) namespace.
old-location: dfs\dfs_info_200_str.htm
old-project: dfs
ms.assetid: a37a97b2-f2f2-45fc-9466-da75e273b075
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: "*LPDFS_INFO_200, *PDFS_INFO_200, DFS_INFO_200, DFS_INFO_200 structure [Distributed File System], LPDFS_INFO_200, LPDFS_INFO_200 structure pointer [Distributed File System], PDFS_INFO_200, PDFS_INFO_200 structure pointer [Distributed File System], _DFS_INFO_200, _win32_dfs_info_200_str, dfs.dfs_info_200_str, fs.dfs_info_200_str, lmdfs/DFS_INFO_200, lmdfs/LPDFS_INFO_200, lmdfs/PDFS_INFO_200, netmgmt.dfs_info_200_str"
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
req.typenames: DFS_INFO_200, *PDFS_INFO_200, *LPDFS_INFO_200
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - LmDfs.h
api_name:
 - DFS_INFO_200
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _DFS_INFO_200 structure


## -description


Contains the name of a domain-based Distributed File System (DFS) namespace.


## -struct-fields




### -field FtDfsName

Pointer to a null-terminated Unicode string that contains the name of a domain-based DFS namespace.


## -remarks



The <b>DFS_INFO_200</b> structure is used to enumerate domain-based DFS namespaces in a domain.




## -see-also




<a href="https://msdn.microsoft.com/a29cde3e-483a-4658-94d4-27398f66abfb">Distributed File System (DFS) Functions</a>



<a href="https://msdn.microsoft.com/c05a8d78-41f4-4c19-a25e-ef4885869584">NetDfsEnum</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>
 

 

