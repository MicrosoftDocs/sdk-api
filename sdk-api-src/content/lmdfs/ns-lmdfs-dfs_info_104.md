---
UID: NS:lmdfs._DFS_INFO_104
title: DFS_INFO_104
author: windows-sdk-content
description: Contains the priority of a DFS root target or link target.
old-location: dfs\dfs_info_104.htm
tech.root: Dfs
ms.assetid: 95b2cd36-4933-440d-889d-ebf36d7b9cc7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPDFS_INFO_104, *PDFS_INFO_104, DFS_INFO_104, DFS_INFO_104 structure [Distributed File System], LPDFS_INFO_104, LPDFS_INFO_104 structure pointer [Distributed File System], PDFS_INFO_104, PDFS_INFO_104 structure pointer [Distributed File System], dfs.dfs_info_104, fs.dfs_info_104, lmdfs/DFS_INFO_104, lmdfs/LPDFS_INFO_104, lmdfs/PDFS_INFO_104, netmgmt.dfs_info_104"
ms.topic: struct
req.header: lmdfs.h
req.include-header: LmDfs.h, Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008, Windows Server 2008
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
 - DFS_INFO_104
product: Windows
targetos: Windows
req.typenames: DFS_INFO_104, *PDFS_INFO_104, *LPDFS_INFO_104
req.redist: 
---

# DFS_INFO_104 structure


## -description


Contains the priority of a DFS root target or link target. This structure is only for use with the <a href="https://msdn.microsoft.com/5526afa7-82bc-47c7-99d6-44e41ef772b1">NetDfsSetInfo</a> function.


## -struct-fields




### -field TargetPriority


<a href="https://msdn.microsoft.com/b8f645ab-e3b4-4e0f-809a-57e27ab1e641">DFS_TARGET_PRIORITY</a> structure that contains the specific priority class and rank of a DFS target.


## -see-also




<a href="https://msdn.microsoft.com/a29cde3e-483a-4658-94d4-27398f66abfb">Distributed File System (DFS) Functions</a>



<a href="https://msdn.microsoft.com/5526afa7-82bc-47c7-99d6-44e41ef772b1">NetDfsSetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>
 

 

