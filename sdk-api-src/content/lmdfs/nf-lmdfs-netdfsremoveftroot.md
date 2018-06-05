---
UID: NF:lmdfs.NetDfsRemoveFtRoot
title: NetDfsRemoveFtRoot function
author: windows-sdk-content
description: Removes the specified root target from a domain-based Distributed File System (DFS) namespace.
old-location: dfs\netdfsremoveftroot.htm
old-project: Dfs
ms.assetid: aa5c9991-ca8e-48ba-922d-feadaff45cc2
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: NetDfsRemoveFtRoot, NetDfsRemoveFtRoot function [Distributed File System], _win32_netdfsremoveftroot, dfs.netdfsremoveftroot, fs.netdfsremoveftroot, lmdfs/NetDfsRemoveFtRoot, netmgmt.netdfsremoveftroot
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DFS_TARGET_PRIORITY_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Netapi32.dll
api_name:
-	NetDfsRemoveFtRoot
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
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
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



The root target server must be available and accessible; otherwise, the call to the <b>NetDfsRemoveFtRoot</b> function will fail.

The caller must have permission to update the DFS container in the directory service and must have Administrator privilege on the DFS host (root) server.




## -see-also




<a href="https://msdn.microsoft.com/a29cde3e-483a-4658-94d4-27398f66abfb">Distributed File System (DFS) Functions</a>



<a href="https://msdn.microsoft.com/df3192f8-f8fc-40ad-a5ff-fb991befff09">NetDfsAddFtRoot</a>



<a href="https://msdn.microsoft.com/c879ba56-cc42-4fa3-960f-ddc65a75dbe3">NetDfsRemove</a>



<a href="https://msdn.microsoft.com/4eaa0e2a-fa09-4a20-98e1-4c0c4ff5d0ef">NetDfsRemoveFtRootForced</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
    Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
    Overview</a>
 

 

