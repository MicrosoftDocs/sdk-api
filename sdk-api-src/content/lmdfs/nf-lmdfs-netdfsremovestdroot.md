---
UID: NF:lmdfs.NetDfsRemoveStdRoot
title: NetDfsRemoveStdRoot function
author: windows-sdk-content
description: Deletes a stand-alone Distributed File System (DFS) namespace.
old-location: dfs\netdfsremovestdroot.htm
tech.root: Dfs
ms.assetid: 850427cc-56da-45cc-8833-e242acc53589
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: NetDfsRemoveStdRoot, NetDfsRemoveStdRoot function [Distributed File System], _win32_netdfsremovestdroot, dfs.netdfsremovestdroot, fs.netdfsremovestdroot, lmdfs/NetDfsRemoveStdRoot, netmgmt.netdfsremovestdroot
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
 - NetDfsRemoveStdRoot
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- NetDfsRemoveStdRoot
: 
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
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



The caller must have Administrator privilege on the DFS server. For more information about calling functions that require administrator privileges, see <a href="https://msdn.microsoft.com/b25db548-d5ab-4276-9b50-36d030909384">Running with Special Privileges</a>.




## -see-also




<a href="https://msdn.microsoft.com/a29cde3e-483a-4658-94d4-27398f66abfb">Distributed File System (DFS) Functions</a>



<a href="https://msdn.microsoft.com/e59236ac-06d7-4b2f-b318-ec13e6c662ac">NetDfsAddStdRoot</a>



<a href="https://msdn.microsoft.com/c879ba56-cc42-4fa3-960f-ddc65a75dbe3">NetDfsRemove</a>



<a href="https://msdn.microsoft.com/aa5c9991-ca8e-48ba-922d-feadaff45cc2">NetDfsRemoveFtRoot</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
    Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
    Overview</a>
 

 

