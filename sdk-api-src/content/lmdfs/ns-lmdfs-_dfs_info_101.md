---
UID: NS:lmdfs._DFS_INFO_101
title: "_DFS_INFO_101"
author: windows-driver-content
description: Describes the state of storage on a DFS root, link, root target, or link target.
old-location: dfs\dfs_info_101_str.htm
old-project: Dfs
ms.assetid: 506aaf68-2f23-4dd2-b43c-aeb86334a3d8
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: "*LPDFS_INFO_101, *PDFS_INFO_101, DFS_INFO_101, DFS_INFO_101 structure [Distributed File System], DFS_STORAGE_STATE_ACTIVE, DFS_STORAGE_STATE_OFFLINE, DFS_STORAGE_STATE_ONLINE, DFS_VOLUME_STATE_INCONSISTENT, DFS_VOLUME_STATE_OFFLINE, DFS_VOLUME_STATE_OK, DFS_VOLUME_STATE_ONLINE, DFS_VOLUME_STATE_RESYNCHRONIZE, DFS_VOLUME_STATE_STANDBY, LPDFS_INFO_101, LPDFS_INFO_101 structure pointer [Distributed File System], PDFS_INFO_101, PDFS_INFO_101 structure pointer [Distributed File System], _DFS_INFO_101, _win32_dfs_info_101_str, dfs.dfs_info_101_str, fs.dfs_info_101_str, lmdfs/DFS_INFO_101, lmdfs/LPDFS_INFO_101, lmdfs/PDFS_INFO_101, netmgmt.dfs_info_101_str"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: DFS_INFO_101, *PDFS_INFO_101, *LPDFS_INFO_101
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	LmDfs.h
api_name:
-	DFS_INFO_101
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _DFS_INFO_101 structure


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

The DFS storage is active. This value is only for use with the <a href="https://msdn.microsoft.com/4c95dffb-a092-45ad-9a3f-37d3abbf4427">NetDfsSetClientInfo</a> function.



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




<a href="https://msdn.microsoft.com/a29cde3e-483a-4658-94d4-27398f66abfb">Distributed File System (DFS) Functions</a>



<a href="https://msdn.microsoft.com/4c95dffb-a092-45ad-9a3f-37d3abbf4427">NetDfsSetClientInfo</a>



<a href="https://msdn.microsoft.com/5526afa7-82bc-47c7-99d6-44e41ef772b1">NetDfsSetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>
 

 

