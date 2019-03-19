---
UID: NS:lmdfs._DFS_INFO_7
title: DFS_INFO_7 (lmdfs.h)
author: windows-sdk-content
description: Contains information about a DFS namespace. This structure contains the version GUID for the metadata for the namespace.
old-location: dfs\dfs_info_7.htm
tech.root: Dfs
ms.assetid: 03bcd93d-e3ec-49aa-be6c-399922f67c28
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPDFS_INFO_7, *PDFS_INFO_7, DFS_INFO_7, DFS_INFO_7 structure [Distributed File System], LPDFS_INFO_7, LPDFS_INFO_7 structure pointer [Distributed File System], PDFS_INFO_7, PDFS_INFO_7 structure pointer [Distributed File System], dfs.dfs_info_7, fs.dfs_info_7, lmdfs/DFS_INFO_7, lmdfs/LPDFS_INFO_7, lmdfs/PDFS_INFO_7, netmgmt.dfs_info_7"
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
 - DFS_INFO_7
product: Windows
targetos: Windows
req.typenames: DFS_INFO_7, *PDFS_INFO_7, *LPDFS_INFO_7
req.redist: 
---

# DFS_INFO_7 structure


## -description


Contains information about a DFS namespace. This structure contains the version 
    <b>GUID</b> for the metadata for the namespace.

This information level is available to DFS roots only.


## -struct-fields




### -field GenerationGuid

The value of this <b>GUID</b> changes each time the DFS metadata is changed.


## -remarks



This structure is used to detect when the metadata of a DFS namespace has changed. It is currently supported 
     only for  domain-based DFS namespace servers.

If a DFS namespace server does not support generation <b>GUID</b>s, the 
     <b>GUID</b> value returned by 
     <a href="https://msdn.microsoft.com/bbb2f24d-1c49-4016-a16b-60fde4a78193">NetDfsGetInfo</a> contains a null 
     <b>GUID</b> (all zeros). This structure cannot be used with 
     <a href="https://msdn.microsoft.com/065ec002-cb90-4d78-a70c-6ac37f71994f">NetDfsGetClientInfo</a>.



