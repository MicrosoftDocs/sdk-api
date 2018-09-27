---
UID: NS:lmdfs._DFS_INFO_100
title: "_DFS_INFO_100"
author: windows-sdk-content
description: Contains a comment associated with a Distributed File System (DFS) root or link.
old-location: dfs\dfs_info_100_str.htm
tech.root: Dfs
ms.assetid: 763ba0f0-01e9-47cf-bbe5-93e13aa83aa0
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*LPDFS_INFO_100, *PDFS_INFO_100, DFS_INFO_100, DFS_INFO_100 structure [Distributed File System], LPDFS_INFO_100, LPDFS_INFO_100 structure pointer [Distributed File System], PDFS_INFO_100, PDFS_INFO_100 structure pointer [Distributed File System], _DFS_INFO_100, _win32_dfs_info_100_str, dfs.dfs_info_100_str, fs.dfs_info_100_str, lmdfs/DFS_INFO_100, lmdfs/LPDFS_INFO_100, lmdfs/PDFS_INFO_100, netmgmt.dfs_info_100_str"
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
 - DFS_INFO_100
product: Windows
targetos: Windows
req.typenames: DFS_INFO_100, *PDFS_INFO_100, *LPDFS_INFO_100
req.redist: 
---

# _DFS_INFO_100 structure


## -description


Contains a comment associated with a Distributed File System (DFS) root or link.


## -struct-fields




### -field Comment

Pointer to a null-terminated Unicode string that contains the comment associated with the specified DFS 
      root or link. The comment is associated with the DFS namespace root or link and not with a specific DFS root 
      target or link target.


## -remarks



The DFS functions use the <b>DFS_INFO_100</b> structure to 
    retrieve and set information about a DFS root or link.




## -see-also




<a href="https://msdn.microsoft.com/a29cde3e-483a-4658-94d4-27398f66abfb">Distributed File System (DFS) Functions</a>



<a href="https://msdn.microsoft.com/bbb2f24d-1c49-4016-a16b-60fde4a78193">NetDfsGetInfo</a>



<a href="https://msdn.microsoft.com/5526afa7-82bc-47c7-99d6-44e41ef772b1">NetDfsSetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>
 

 

