---
UID: NS:lmdfs._DFS_STORAGE_INFO
title: DFS_STORAGE_INFO (lmdfs.h)
description: Contains information about a DFS root or link target in a DFS namespace or from the cache maintained by the DFS client.
helpviewer_keywords: ["*LPDFS_STORAGE_INFO","*PDFS_STORAGE_INFO","DFS_STORAGE_INFO","DFS_STORAGE_INFO structure [Distributed File System]","DFS_STORAGE_STATE_ACTIVE","DFS_STORAGE_STATE_OFFLINE","DFS_STORAGE_STATE_ONLINE","LPDFS_STORAGE_INFO","LPDFS_STORAGE_INFO structure pointer [Distributed File System]","PDFS_STORAGE_INFO","PDFS_STORAGE_INFO structure pointer [Distributed File System]","_win32_dfs_storage_info_str","dfs.dfs_storage_info","fs.dfs_storage_info","fs.dfs_storage_info_str","lmdfs/DFS_STORAGE_INFO","lmdfs/LPDFS_STORAGE_INFO","lmdfs/PDFS_STORAGE_INFO","netmgmt.dfs_storage_info"]
old-location: dfs\dfs_storage_info.htm
tech.root: Dfs
ms.assetid: f50f32d8-1745-4ff6-97a6-ddd6fff95955
ms.date: 12/05/2018
ms.keywords: '*LPDFS_STORAGE_INFO, *PDFS_STORAGE_INFO, DFS_STORAGE_INFO, DFS_STORAGE_INFO structure [Distributed File System], DFS_STORAGE_STATE_ACTIVE, DFS_STORAGE_STATE_OFFLINE, DFS_STORAGE_STATE_ONLINE, LPDFS_STORAGE_INFO, LPDFS_STORAGE_INFO structure pointer [Distributed File System], PDFS_STORAGE_INFO, PDFS_STORAGE_INFO structure pointer [Distributed File System], _win32_dfs_storage_info_str, dfs.dfs_storage_info, fs.dfs_storage_info, fs.dfs_storage_info_str, lmdfs/DFS_STORAGE_INFO, lmdfs/LPDFS_STORAGE_INFO, lmdfs/PDFS_STORAGE_INFO, netmgmt.dfs_storage_info'
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
targetos: Windows
req.typenames: DFS_STORAGE_INFO, *PDFS_STORAGE_INFO, *LPDFS_STORAGE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DFS_STORAGE_INFO
 - lmdfs/_DFS_STORAGE_INFO
 - PDFS_STORAGE_INFO
 - lmdfs/PDFS_STORAGE_INFO
 - DFS_STORAGE_INFO
 - lmdfs/DFS_STORAGE_INFO
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
 - DFS_STORAGE_INFO
---

# DFS_STORAGE_INFO structure


## -description

Contains information about a DFS root or link target in a DFS namespace or from the cache maintained 
    by the DFS client. Information about a DFS root or link target in a DFS namespace is retrieved by 
    calling the <a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetinfo">NetDfsGetInfo</a> function. Information about a 
    DFS root or link target from the cache maintained by the DFS client is retrieved by calling the 
    <a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo">NetDfsGetClientInfo</a> function.

## -struct-fields

### -field State

State of the target.

When this structure is returned as a result of calling the 
      <a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetinfo">NetDfsGetInfo</a> function, this member can be one of the 
      following values.



#### DFS_STORAGE_STATE_OFFLINE (0x00000001)

The DFS root or link target is offline.



#### DFS_STORAGE_STATE_ONLINE (0x00000002)

The DFS root or link target is online.

When this structure is returned as a result of calling the 
      <a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo">NetDfsGetClientInfo</a> function, the 
      <b>DFS_STORAGE_STATE_ONLINE</b> (0x00000002) state is set by default. If the target is the 
      active target in the DFS client cache, the following value is logically combined with the default value via the 
      <b>OR</b> operator.



#### DFS_STORAGE_STATE_ACTIVE (0x00000004)

The DFS root or link target is the active target.

### -field ServerName

Pointer to a null-terminated Unicode string that specifies the DFS root target or link target server 
      name.

### -field ShareName

Pointer to a null-terminated Unicode string that specifies the DFS root target or link target share 
      name.

## -remarks

The <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_3">DFS_INFO_3</a> and 
    <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_4">DFS_INFO_4</a> structures each contain one or more 
    <b>DFS_STORAGE_INFO</b> structures, one for each DFS target. 
    Only one target can be marked as the active target. It is possible that no targets will be marked active.

## -see-also

<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_3">DFS_INFO_3</a>



<a href="/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions">Distributed File System (DFS) Functions</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsenum">NetDfsEnum</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetinfo">NetDfsGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>