---
UID: NS:lmdfs._DFS_INFO_1
title: "_DFS_INFO_1"
author: windows-sdk-content
description: Contains the name of a Distributed File System (DFS) root or link.
old-location: dfs\dfs_info_1_str.htm
old-project: Dfs
ms.assetid: 96647570-badd-4925-ab90-054a00ba04c4
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: "*LPDFS_INFO_1, *PDFS_INFO_1, DFS_INFO_1, DFS_INFO_1 structure [Distributed File System], LPDFS_INFO_1, LPDFS_INFO_1 structure pointer [Distributed File System], PDFS_INFO_1, PDFS_INFO_1 structure pointer [Distributed File System], _DFS_INFO_1, _win32_dfs_info_1_str, dfs.dfs_info_1_str, fs.dfs_info_1_str, lmdfs/DFS_INFO_1, lmdfs/LPDFS_INFO_1, lmdfs/PDFS_INFO_1, netmgmt.dfs_info_1_str"
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
req.typenames: DFS_INFO_1, *PDFS_INFO_1, *LPDFS_INFO_1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - LmDfs.h
api_name:
 - DFS_INFO_1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _DFS_INFO_1 structure


## -description


Contains the name of a Distributed File System (DFS) root or link. This structure is only for use with the 
    <a href="https://msdn.microsoft.com/c05a8d78-41f4-4c19-a25e-ef4885869584">NetDfsEnum</a>, 
    <a href="https://msdn.microsoft.com/065ec002-cb90-4d78-a70c-6ac37f71994f">NetDfsGetClientInfo</a>, and 
    <a href="https://msdn.microsoft.com/bbb2f24d-1c49-4016-a16b-60fde4a78193">NetDfsGetInfo</a> functions and the 
    <a href="https://msdn.microsoft.com/d4eec104-128b-43b5-9fae-08ab0b977dec">FSCTL_DFS_GET_PKT_ENTRY_STATE</a> control 
    code.


## -struct-fields




### -field EntryPath

Pointer to a null-terminated Unicode string that specifies the Universal Naming Convention (UNC) path of a DFS root or link.

For a link, the string can be in one of two forms. The first form is as follows:

\\<i>ServerName</i>\<i>DfsName</i>\<i>link_path</i>

where <i>ServerName</i> is the name of the root target server that hosts the stand-alone DFS namespace; <i>DfsName</i> is the name of the DFS namespace; and <i>link_path</i> is a DFS link.

The second form is as follows:

\\<i>DomainName</i>\<i>DomDfsname</i>\<i>link_path</i>

where <i>DomainName</i> is the name of the domain that hosts the domain-based DFS namespace; <i>DomDfsname</i> is the name of the DFS namespace; and <i>link_path</i> is a DFS link.

For a root, the string can be in one of two forms:

\\<i>ServerName</i>\<i>DfsName</i>

or

\\<i>DomainName</i>\<i>DomDfsname</i>

where the values of the names are the same as those described previously.


## -remarks



The DFS functions use the 
<b>DFS_INFO_1</b> structure to retrieve information about a DFS root or link.




## -see-also




<a href="https://msdn.microsoft.com/a29cde3e-483a-4658-94d4-27398f66abfb">Distributed File System (DFS) Functions</a>



<a href="https://msdn.microsoft.com/c05a8d78-41f4-4c19-a25e-ef4885869584">NetDfsEnum</a>



<a href="https://msdn.microsoft.com/065ec002-cb90-4d78-a70c-6ac37f71994f">NetDfsGetClientInfo</a>



<a href="https://msdn.microsoft.com/bbb2f24d-1c49-4016-a16b-60fde4a78193">NetDfsGetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>
 

 

