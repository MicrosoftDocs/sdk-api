---
UID: NF:lmdfs.NetDfsRemoveFtRootForced
title: NetDfsRemoveFtRootForced function (lmdfs.h)
description: Removes the specified root target from a domain-based Distributed File System (DFS) namespace, even if the root target server is offline.
helpviewer_keywords: ["NetDfsRemoveFtRootForced","NetDfsRemoveFtRootForced function [Distributed File System]","_win32_netdfsremoveftrootforced","dfs.netdfsremoveftrootforced","fs.netdfsremoveftrootforced","lmdfs/NetDfsRemoveFtRootForced","netmgmt.netdfsremoveftrootforced"]
old-location: dfs\netdfsremoveftrootforced.htm
tech.root: Dfs
ms.assetid: 4eaa0e2a-fa09-4a20-98e1-4c0c4ff5d0ef
ms.date: 12/05/2018
ms.keywords: NetDfsRemoveFtRootForced, NetDfsRemoveFtRootForced function [Distributed File System], _win32_netdfsremoveftrootforced, dfs.netdfsremoveftrootforced, fs.netdfsremoveftrootforced, lmdfs/NetDfsRemoveFtRootForced, netmgmt.netdfsremoveftrootforced
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
 - NetDfsRemoveFtRootForced
 - lmdfs/NetDfsRemoveFtRootForced
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
 - NetDfsRemoveFtRootForced
---

# NetDfsRemoveFtRootForced function


## -description

Removes the specified root target from a domain-based Distributed File System (DFS) namespace, even if the root target server is offline. If the last root target of the DFS namespace is being removed, the function also deletes the DFS namespace. A DFS namespace can be deleted without first deleting all the links in it.
<div class="alert"><b>Note</b>  The 
<b>NetDfsRemoveFtRootForced</b> function does not update the registry on the DFS root target server. For more information, see the Remarks section.</div><div> </div>

## -parameters

### -param DomainName [in]

Pointer to a string that specifies the name of the Active Directory domain that contains the domain-based DFS namespace to be removed. This parameter is required.

### -param ServerName [in]

Pointer to a string that specifies the name of the DFS root target server to be removed. The server must host a root of the domain-based DFS namespace. This parameter is required.

### -param RootShare [in]

Pointer to a string that specifies the name of the DFS root target share to be removed. This parameter is required.

### -param FtDfsName [in]

Pointer to a string that specifies the name of the domain-based DFS namespace from which to remove the root target. This parameter is required. Typically, it is the same as the <i>RootShare</i> parameter.

### -param Flags

Must be zero.

## -returns

If the function succeeds, the return value is <b>NERR_Success</b>.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

The caller must have permission to update the DFS container in the directory service and must have Administrator privilege on the DFS host (root) server.

The <b>NetDfsRemoveFtRootForced</b> function forcibly removes a domain-based DFS root target from a DFS namespace.  It is used to delete a domain-based DFS namespace when the root target servers of the namespace are no longer available (for example, because they have been decommissioned).

Because  the DFS root target is removed by contacting the primary domain controller (PDC) and not by removing the DFS root target server, <b>NetDfsRemoveFtRootForced</b> does not update the registry of the root target server. Under normal circumstances, you can remove the root target from a DFS domain root by calling the 
<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftroot">NetDfsRemoveFtRoot</a> function.

## -see-also

<a href="/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions">Distributed File System (DFS) Functions</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddftroot">NetDfsAddFtRoot</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftroot">NetDfsRemoveFtRoot</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
    Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
    Overview</a>