---
UID: NS:lmdfs._DFS_INFO_7
title: DFS_INFO_7 (lmdfs.h)
description: Contains information about a DFS namespace. This structure contains the version GUID for the metadata for the namespace.
helpviewer_keywords: ["*LPDFS_INFO_7","*PDFS_INFO_7","DFS_INFO_7","DFS_INFO_7 structure [Distributed File System]","LPDFS_INFO_7","LPDFS_INFO_7 structure pointer [Distributed File System]","PDFS_INFO_7","PDFS_INFO_7 structure pointer [Distributed File System]","dfs.dfs_info_7","fs.dfs_info_7","lmdfs/DFS_INFO_7","lmdfs/LPDFS_INFO_7","lmdfs/PDFS_INFO_7","netmgmt.dfs_info_7"]
old-location: dfs\dfs_info_7.htm
tech.root: Dfs
ms.assetid: 03bcd93d-e3ec-49aa-be6c-399922f67c28
ms.date: 12/05/2018
ms.keywords: '*LPDFS_INFO_7, *PDFS_INFO_7, DFS_INFO_7, DFS_INFO_7 structure [Distributed File System], LPDFS_INFO_7, LPDFS_INFO_7 structure pointer [Distributed File System], PDFS_INFO_7, PDFS_INFO_7 structure pointer [Distributed File System], dfs.dfs_info_7, fs.dfs_info_7, lmdfs/DFS_INFO_7, lmdfs/LPDFS_INFO_7, lmdfs/PDFS_INFO_7, netmgmt.dfs_info_7'
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
targetos: Windows
req.typenames: DFS_INFO_7, *PDFS_INFO_7, *LPDFS_INFO_7
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DFS_INFO_7
 - lmdfs/_DFS_INFO_7
 - PDFS_INFO_7
 - lmdfs/PDFS_INFO_7
 - DFS_INFO_7
 - lmdfs/DFS_INFO_7
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - LmDfs.h
api_name:
 - DFS_INFO_7
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
     <a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetinfo">NetDfsGetInfo</a> contains a null 
     <b>GUID</b> (all zeros). This structure cannot be used with 
     <a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo">NetDfsGetClientInfo</a>.