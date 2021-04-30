---
UID: NF:lmdfs.NetDfsRemoveFtRoot
title: NetDfsRemoveFtRoot function (lmdfs.h)
description: Removes the specified root target from a domain-based Distributed File System (DFS) namespace.
helpviewer_keywords: ["NetDfsRemoveFtRoot","NetDfsRemoveFtRoot function [Distributed File System]","_win32_netdfsremoveftroot","dfs.netdfsremoveftroot","fs.netdfsremoveftroot","lmdfs/NetDfsRemoveFtRoot","netmgmt.netdfsremoveftroot"]
old-location: dfs\netdfsremoveftroot.htm
tech.root: Dfs
ms.assetid: aa5c9991-ca8e-48ba-922d-feadaff45cc2
ms.date: 12/05/2018
ms.keywords: NetDfsRemoveFtRoot, NetDfsRemoveFtRoot function [Distributed File System], _win32_netdfsremoveftroot, dfs.netdfsremoveftroot, fs.netdfsremoveftroot, lmdfs/NetDfsRemoveFtRoot, netmgmt.netdfsremoveftroot
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
 - NetDfsRemoveFtRoot
 - lmdfs/NetDfsRemoveFtRoot
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
 - NetDfsRemoveFtRoot
---

# NetDfsRemoveFtRoot function


## -description

Removes the specified root target from a domain-based Distributed File System (DFS) namespace. If the last root target of the DFS namespace is being removed, the function also deletes the DFS namespace. A DFS namespace can be deleted without first deleting all the links in it.

## -parameters

### -param ServerName [in]

Pointer to a string that specifies the server name of the root target to be removed. The server must host the root of a domain-based DFS namespace. This parameter is required.

### -param RootShare [in]

Pointer to a string that specifies the name of the DFS root target share to be removed. This parameter is required.

### -param FtDfsName [in]

Pointer to a string that specifies the name of the domain-based DFS namespace from which to remove the root target. This parameter is required. Typically, it is the same as the <i>RootShare</i> parameter.

### -param Flags

This parameter is reserved and must be zero.

## -returns

If the function succeeds, the return value is <b>NERR_Success</b>.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

The root target server must be available and accessible; otherwise, the call to the <b>NetDfsRemoveFtRoot</b> function will fail.

The caller must have permission to update the DFS container in the directory service and must have Administrator privilege on the DFS host (root) server.

## -see-also

<a href="/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions">Distributed File System (DFS) Functions</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddftroot">NetDfsAddFtRoot</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremove">NetDfsRemove</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced">NetDfsRemoveFtRootForced</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
    Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
    Overview</a>