---
UID: NS:lmdfs._DFS_INFO_101
title: DFS_INFO_101 (lmdfs.h)
description: Describes the state of storage on a DFS root, link, root target, or link target.
helpviewer_keywords: ["*LPDFS_INFO_101","*PDFS_INFO_101","DFS_INFO_101","DFS_INFO_101 structure [Distributed File System]","DFS_STORAGE_STATE_ACTIVE","DFS_STORAGE_STATE_OFFLINE","DFS_STORAGE_STATE_ONLINE","DFS_VOLUME_STATE_INCONSISTENT","DFS_VOLUME_STATE_OFFLINE","DFS_VOLUME_STATE_OK","DFS_VOLUME_STATE_ONLINE","DFS_VOLUME_STATE_RESYNCHRONIZE","DFS_VOLUME_STATE_STANDBY","LPDFS_INFO_101","LPDFS_INFO_101 structure pointer [Distributed File System]","PDFS_INFO_101","PDFS_INFO_101 structure pointer [Distributed File System]","_win32_dfs_info_101_str","dfs.dfs_info_101_str","fs.dfs_info_101_str","lmdfs/DFS_INFO_101","lmdfs/LPDFS_INFO_101","lmdfs/PDFS_INFO_101","netmgmt.dfs_info_101_str"]
old-location: dfs\dfs_info_101_str.htm
tech.root: Dfs
ms.assetid: 506aaf68-2f23-4dd2-b43c-aeb86334a3d8
ms.date: 12/05/2018
ms.keywords: '*LPDFS_INFO_101, *PDFS_INFO_101, DFS_INFO_101, DFS_INFO_101 structure [Distributed File System], DFS_STORAGE_STATE_ACTIVE, DFS_STORAGE_STATE_OFFLINE, DFS_STORAGE_STATE_ONLINE, DFS_VOLUME_STATE_INCONSISTENT, DFS_VOLUME_STATE_OFFLINE, DFS_VOLUME_STATE_OK, DFS_VOLUME_STATE_ONLINE, DFS_VOLUME_STATE_RESYNCHRONIZE, DFS_VOLUME_STATE_STANDBY, LPDFS_INFO_101, LPDFS_INFO_101 structure pointer [Distributed File System], PDFS_INFO_101, PDFS_INFO_101 structure pointer [Distributed File System], _win32_dfs_info_101_str, dfs.dfs_info_101_str, fs.dfs_info_101_str, lmdfs/DFS_INFO_101, lmdfs/LPDFS_INFO_101, lmdfs/PDFS_INFO_101, netmgmt.dfs_info_101_str'
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
req.typenames: DFS_INFO_101, *PDFS_INFO_101, *LPDFS_INFO_101
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DFS_INFO_101
 - lmdfs/_DFS_INFO_101
 - PDFS_INFO_101
 - lmdfs/PDFS_INFO_101
 - DFS_INFO_101
 - lmdfs/DFS_INFO_101
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
 - DFS_INFO_101
---

# DFS_INFO_101 structure


## -description

Describes the state of storage on a DFS root, link, root target, or link target.

## -struct-fields

### -field State

Specifies a set of bit flags that describe the status of the host server. Following are valid values for this member. Note that the <b>DFS_STORAGE_STATE_OFFLINE</b> and <b>DFS_STORAGE_STATE_ONLINE</b> values are mutually exclusive. 

The storage states can only be set on DFS root targets or DFS link targets. The DFS volume states can only be set on a DFS namespace root or DFS link and not on individual targets.



#### DFS_STORAGE_STATE_OFFLINE (0x00000001)

The DFS storage is offline.



#### DFS_STORAGE_STATE_ONLINE (0x00000002)

The DFS storage is online.



#### DFS_STORAGE_STATE_ACTIVE (0x00000004)

The DFS storage is active. This value is only for use with the <a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetclientinfo">NetDfsSetClientInfo</a> function.



#### DFS_VOLUME_STATE_OK (0x00000001)

The specified DFS root or link is in the normal state.



#### DFS_VOLUME_STATE_INCONSISTENT (0x00000002)

The internal DFS database is inconsistent with the specified DFS root or link. Attempts to repair the inconsistency have failed. This value is read-only.



#### DFS_VOLUME_STATE_OFFLINE (0x00000003)

The specified DFS root or link is offline or unavailable.



#### DFS_VOLUME_STATE_ONLINE (0x00000004)

The specified DFS root or link is available.



#### DFS_VOLUME_STATE_RESYNCHRONIZE (0x00000010)

Forces a resynchronization on the DFS root target. This flag is valid only for a DFS root target, and is write-only.



#### DFS_VOLUME_STATE_STANDBY (0x00000020)

Puts a root volume in standby mode. This flag is valid for a clustered DFS namespace only.

## -see-also

<a href="/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions">Distributed File System (DFS) Functions</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetclientinfo">NetDfsSetClientInfo</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetinfo">NetDfsSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>