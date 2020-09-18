---
UID: NF:lmdfs.NetDfsAddFtRoot
title: NetDfsAddFtRoot function (lmdfs.h)
description: Creates a new domain-based Distributed File System (DFS) namespace. If the namespace already exists, the function adds the specified root target to it.
helpviewer_keywords: ["NetDfsAddFtRoot","NetDfsAddFtRoot function [Distributed File System]","_win32_netdfsaddftroot","dfs.netdfsaddftroot","fs.netdfsaddftroot","lmdfs/NetDfsAddFtRoot","netmgmt.netdfsaddftroot"]
old-location: dfs\netdfsaddftroot.htm
tech.root: Dfs
ms.assetid: df3192f8-f8fc-40ad-a5ff-fb991befff09
ms.date: 12/05/2018
ms.keywords: NetDfsAddFtRoot, NetDfsAddFtRoot function [Distributed File System], _win32_netdfsaddftroot, dfs.netdfsaddftroot, fs.netdfsaddftroot, lmdfs/NetDfsAddFtRoot, netmgmt.netdfsaddftroot
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
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetDfsAddFtRoot
 - lmdfs/NetDfsAddFtRoot
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetDfsAddFtRoot
---

# NetDfsAddFtRoot function


## -description

Creates a new domain-based Distributed File System (DFS) namespace. If the namespace already exists, the function adds the specified root target to it.

## -parameters

### -param ServerName [in]

Pointer to a string that specifies the name of the server that will host the new DFS root target. This value cannot be an IP address. This parameter is required.

### -param RootShare [in]

Pointer to a string that specifies the name of the shared folder on the server that will host the new DFS root target. This parameter is required.

### -param FtDfsName [in]

Pointer to a string that specifies the name of the new or existing domain-based DFS namespace. This parameter is required. For compatibility reasons, it should specify the same string as the <i>RootShare</i> parameter.

### -param Comment [in, optional]

Pointer to a string that contains an optional comment associated with the DFS namespace.

### -param Flags [in]

This parameter is reserved and must be zero.

## -returns

If the function succeeds, the return value is <b>NERR_Success</b>.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

The share specified by the <i>RootShare</i> parameter must already exist on the server that will host the new DFS root target. This function does not create a new share.

The caller must have permission to update the DFS container in the directory service and must have Administrator privilege on the DFS host (root) server.

## -see-also

<a href="/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions">Distributed File System  (DFS) Functions</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsadd">NetDfsAdd</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddroottarget">NetDfsAddRootTarget</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddstdroot">NetDfsAddStdRoot</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftroot">NetDfsRemoveFtRoot</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
    Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
    Overview</a>