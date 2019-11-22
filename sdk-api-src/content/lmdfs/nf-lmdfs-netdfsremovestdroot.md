---
UID: NF:lmdfs.NetDfsRemoveStdRoot
title: NetDfsRemoveStdRoot function (lmdfs.h)

description: Deletes a stand-alone Distributed File System (DFS) namespace.
old-location: dfs\netdfsremovestdroot.htm
tech.root: Dfs
ms.assetid: 850427cc-56da-45cc-8833-e242acc53589

ms.date: 12/05/2018
ms.keywords: NetDfsRemoveStdRoot, NetDfsRemoveStdRoot function [Distributed File System], _win32_netdfsremovestdroot, dfs.netdfsremovestdroot, fs.netdfsremovestdroot, lmdfs/NetDfsRemoveStdRoot, netmgmt.netdfsremovestdroot
ms.topic: function
f1_keywords: 
 - "lmdfs/NetDfsRemoveStdRoot"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetDfsRemoveStdRoot
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NetDfsRemoveStdRoot function


## -description


Deletes a stand-alone Distributed File System (DFS) namespace.


## -parameters




### -param ServerName [in]

Pointer to a string that specifies the DFS root target server name of the stand-alone DFS namespace to be removed. This parameter is required.


### -param RootShare [in]

Pointer to a string that specifies the DFS root target share name of the stand-alone DFS namespace to be removed. This parameter is required.


### -param Flags [in]

Must be zero.


## -returns



If the function succeeds, the return value is <b>NERR_Success</b>.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">System Error Codes</a>.




## -remarks



The caller must have Administrator privilege on the DFS server. For more information about calling functions that require administrator privileges, see <a href="https://docs.microsoft.com/windows/desktop/SecBP/running-with-special-privileges">Running with Special Privileges</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions">Distributed File System (DFS) Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddstdroot">NetDfsAddStdRoot</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremove">NetDfsRemove</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftroot">NetDfsRemoveFtRoot</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management-functions">Network
    Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management">Network Management
    Overview</a>
 

 

