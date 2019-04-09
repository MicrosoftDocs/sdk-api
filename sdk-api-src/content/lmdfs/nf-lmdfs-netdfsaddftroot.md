---
UID: NF:lmdfs.NetDfsAddFtRoot
title: NetDfsAddFtRoot function (lmdfs.h)
author: windows-sdk-content
description: Creates a new domain-based Distributed File System (DFS) namespace. If the namespace already exists, the function adds the specified root target to it.
old-location: dfs\netdfsaddftroot.htm
tech.root: Dfs
ms.assetid: df3192f8-f8fc-40ad-a5ff-fb991befff09
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: NetDfsAddFtRoot, NetDfsAddFtRoot function [Distributed File System], _win32_netdfsaddftroot, dfs.netdfsaddftroot, fs.netdfsaddftroot, lmdfs/NetDfsAddFtRoot, netmgmt.netdfsaddftroot
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
 - NetDfsAddFtRoot
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



The share specified by the <i>RootShare</i> parameter must already exist on the server that will host the new DFS root target. This function does not create a new share.

The caller must have permission to update the DFS container in the directory service and must have Administrator privilege on the DFS host (root) server.




## -see-also




<a href="https://msdn.microsoft.com/a29cde3e-483a-4658-94d4-27398f66abfb">Distributed File System  (DFS) Functions</a>



<a href="https://msdn.microsoft.com/2c8816b2-5489-486e-b749-605932ba9fe9">NetDfsAdd</a>



<a href="https://msdn.microsoft.com/c4ce8f50-f090-4783-b6c9-834d9e0c33de">NetDfsAddRootTarget</a>



<a href="https://msdn.microsoft.com/e59236ac-06d7-4b2f-b318-ec13e6c662ac">NetDfsAddStdRoot</a>



<a href="https://msdn.microsoft.com/aa5c9991-ca8e-48ba-922d-feadaff45cc2">NetDfsRemoveFtRoot</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
    Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
    Overview</a>
 

 

