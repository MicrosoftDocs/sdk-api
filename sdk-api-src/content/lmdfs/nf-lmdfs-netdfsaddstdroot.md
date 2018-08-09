---
UID: NF:lmdfs.NetDfsAddStdRoot
title: NetDfsAddStdRoot function
author: windows-sdk-content
description: Creates a new stand-alone Distributed File System (DFS) namespace.
old-location: dfs\netdfsaddstdroot.htm
old-project: dfs
ms.assetid: e59236ac-06d7-4b2f-b318-ec13e6c662ac
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: NetDfsAddStdRoot, NetDfsAddStdRoot function [Distributed File System], _win32_netdfsaddstdroot, dfs.netdfsaddstdroot, fs.netdfsaddstdroot, lmdfs/NetDfsAddStdRoot, netmgmt.netdfsaddstdroot
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
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetDfsAddStdRoot
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
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
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



The share specified by the <i>RootShare</i> parameter must already exist on the server that will host the new DFS root target. This function does not create a new share.

The caller must have Administrator privilege on the DFS server.  For more information about calling functions that require administrator privileges, see 
    <a href="https://msdn.microsoft.com/b25db548-d5ab-4276-9b50-36d030909384">Running with Special Privileges</a>.




## -see-also




<a href="https://msdn.microsoft.com/a29cde3e-483a-4658-94d4-27398f66abfb">Distributed File System  (DFS) Functions</a>



<a href="https://msdn.microsoft.com/df3192f8-f8fc-40ad-a5ff-fb991befff09">NetDfsAddFtRoot</a>



<a href="https://msdn.microsoft.com/c4ce8f50-f090-4783-b6c9-834d9e0c33de">NetDfsAddRootTarget</a>



<a href="https://msdn.microsoft.com/850427cc-56da-45cc-8833-e242acc53589">NetDfsRemoveStdRoot</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
    Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
    Overview</a>
 

 

