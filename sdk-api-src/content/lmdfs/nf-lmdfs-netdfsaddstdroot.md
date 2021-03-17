---
UID: NF:lmdfs.NetDfsAddStdRoot
title: NetDfsAddStdRoot function (lmdfs.h)
description: Creates a new stand-alone Distributed File System (DFS) namespace.
helpviewer_keywords: ["NetDfsAddStdRoot","NetDfsAddStdRoot function [Distributed File System]","_win32_netdfsaddstdroot","dfs.netdfsaddstdroot","fs.netdfsaddstdroot","lmdfs/NetDfsAddStdRoot","netmgmt.netdfsaddstdroot"]
old-location: dfs\netdfsaddstdroot.htm
tech.root: Dfs
ms.assetid: e59236ac-06d7-4b2f-b318-ec13e6c662ac
ms.date: 12/05/2018
ms.keywords: NetDfsAddStdRoot, NetDfsAddStdRoot function [Distributed File System], _win32_netdfsaddstdroot, dfs.netdfsaddstdroot, fs.netdfsaddstdroot, lmdfs/NetDfsAddStdRoot, netmgmt.netdfsaddstdroot
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
 - NetDfsAddStdRoot
 - lmdfs/NetDfsAddStdRoot
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
 - NetDfsAddStdRoot
---

# NetDfsAddStdRoot function


## -description

Creates a new stand-alone Distributed File System (DFS) namespace.

## -parameters

### -param ServerName [in]

Pointer to a string that specifies the name of the server that will host the new stand-alone DFS namespace. This parameter is required.

### -param RootShare [in]

Pointer to a string that specifies the name of the shared folder for the new stand-alone DFS namespace on the server that will host the namespace. This parameter is required.

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

The caller must have Administrator privilege on the DFS server.  For more information about calling functions that require administrator privileges, see 
    <a href="/windows/desktop/SecBP/running-with-special-privileges">Running with Special Privileges</a>.

## -see-also

<a href="/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions">Distributed File System  (DFS) Functions</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddftroot">NetDfsAddFtRoot</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddroottarget">NetDfsAddRootTarget</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremovestdroot">NetDfsRemoveStdRoot</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
    Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
    Overview</a>