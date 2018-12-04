---
UID: NF:lmdfs.NetDfsRemoveFtRootForced
title: NetDfsRemoveFtRootForced function
author: windows-sdk-content
description: Removes the specified root target from a domain-based Distributed File System (DFS) namespace, even if the root target server is offline.
old-location: dfs\netdfsremoveftrootforced.htm
tech.root: Dfs
ms.assetid: 4eaa0e2a-fa09-4a20-98e1-4c0c4ff5d0ef
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: NetDfsRemoveFtRootForced, NetDfsRemoveFtRootForced function [Distributed File System], _win32_netdfsremoveftrootforced, dfs.netdfsremoveftrootforced, fs.netdfsremoveftrootforced, lmdfs/NetDfsRemoveFtRootForced, netmgmt.netdfsremoveftrootforced
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - NetDfsRemoveFtRootForced
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



The caller must have permission to update the DFS container in the directory service and must have Administrator privilege on the DFS host (root) server.

The <b>NetDfsRemoveFtRootForced</b> function forcibly removes a domain-based DFS root target from a DFS namespace.  It is used to delete a domain-based DFS namespace when the root target servers of the namespace are no longer available (for example, because they have been decommissioned).

Because  the DFS root target is removed by contacting the primary domain controller (PDC) and not by removing the DFS root target server, <b>NetDfsRemoveFtRootForced</b> does not update the registry of the root target server. Under normal circumstances, you can remove the root target from a DFS domain root by calling the 
<a href="https://msdn.microsoft.com/aa5c9991-ca8e-48ba-922d-feadaff45cc2">NetDfsRemoveFtRoot</a> function.




## -see-also




<a href="https://msdn.microsoft.com/a29cde3e-483a-4658-94d4-27398f66abfb">Distributed File System (DFS) Functions</a>



<a href="https://msdn.microsoft.com/df3192f8-f8fc-40ad-a5ff-fb991befff09">NetDfsAddFtRoot</a>



<a href="https://msdn.microsoft.com/aa5c9991-ca8e-48ba-922d-feadaff45cc2">NetDfsRemoveFtRoot</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
    Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
    Overview</a>
 

 

