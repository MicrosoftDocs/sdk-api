---
UID: NF:threadpoolapiset.CreateThreadpoolCleanupGroup
title: CreateThreadpoolCleanupGroup function
author: windows-sdk-content
description: Creates a cleanup group that applications can use to track one or more thread pool callbacks.
old-location: base\createthreadpoolcleanupgroup.htm
tech.root: procthread
ms.assetid: 668593fe-2ed1-418d-8cd5-5fac61826ea1
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CreateThreadpoolCleanupGroup, CreateThreadpoolCleanupGroup function, base.createthreadpoolcleanupgroup, threadpoolapiset/CreateThreadpoolCleanupGroup, winbase/CreateThreadpoolCleanupGroup
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: threadpoolapiset.h
req.include-header: Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-threadpool-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-threadpool-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - CreateThreadpoolCleanupGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateThreadpoolCleanupGroup function


## -description


Creates a cleanup group that applications can use to track one or more thread pool callbacks.


## -parameters






## -returns



If the function succeeds, it returns a <b>TP_CLEANUP_GROUP</b> structure of the newly allocated cleanup group. Applications do not modify the members of this structure.

If function fails, it returns NULL. To retrieve extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



After creating the cleanup group, call <a href="https://msdn.microsoft.com/395db7ba-ff39-46ee-917b-2896a0e99d43">SetThreadpoolCallbackCleanupGroup</a> to associate the cleanup group with a callback environment.

A member is added to the group each time you call one of the following functions:<ul>
<li>
<a href="https://msdn.microsoft.com/621f4747-50fa-4538-bd6a-dbe4dbb05dd1">CreateThreadpoolIo</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1fa98b79-e646-4e48-9979-1817d2c1b713">CreateThreadpoolTimer</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ba19f5f9-d4b0-4865-9609-95e7697d61c0">CreateThreadpoolWait</a>
</li>
<li>
<a href="https://msdn.microsoft.com/50647d87-1768-4918-8376-a6a04daca621">CreateThreadpoolWork</a>
</li>
</ul>


You use one of the following corresponding close functions to remove a member from the group.<ul>
<li>
<a href="https://msdn.microsoft.com/499190de-54e8-4be6-909b-04505bcb0aa6">CloseThreadpoolIo</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c1270c5d-a1f5-4481-a343-c1ff3301a56e">CloseThreadpoolTimer</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f8323ad2-c0b6-4e5c-b6eb-7195673f8992">CloseThreadpoolWait</a>
</li>
<li>
<a href="https://msdn.microsoft.com/89d7362e-0814-4f7e-a27f-8a297e210559">CloseThreadpoolWork</a>
</li>
</ul>


To close all the callbacks, call <a href="https://msdn.microsoft.com/9c78db13-d8dd-4eda-83d9-c9dbbfc6e822">CloseThreadpoolCleanupGroupMembers</a>.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/3d349c83-8b1a-4a5b-9625-be905d613b92">Using the Thread Pool Functions</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/e38e4d99-63f2-4bac-8675-cf0f3aa149a7">CloseThreadpoolCleanupGroup</a>



<a href="https://msdn.microsoft.com/9c78db13-d8dd-4eda-83d9-c9dbbfc6e822">CloseThreadpoolCleanupGroupMembers</a>



<a href="https://msdn.microsoft.com/395db7ba-ff39-46ee-917b-2896a0e99d43">SetThreadpoolCallbackCleanupGroup</a>



<a href="https://msdn.microsoft.com/abe0798a-0b60-4bdb-a61e-45393f1e958d">Thread Pools</a>
 

 

