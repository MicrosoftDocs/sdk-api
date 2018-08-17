---
UID: NF:threadpoolapiset.CloseThreadpoolWait
title: CloseThreadpoolWait function
author: windows-sdk-content
description: Releases the specified wait object.
old-location: base\closethreadpoolwait.htm
old-project: procthread
ms.assetid: f8323ad2-c0b6-4e5c-b6eb-7195673f8992
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: CloseThreadpoolWait, CloseThreadpoolWait function, base.closethreadpoolwait, threadpoolapiset/CloseThreadpoolWait, winbase/CloseThreadpoolWait
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: threadpoolapiset.h
req.include-header: Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.redist: 
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
tech.root: 
req.typenames: TS_TEXTCHANGE
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
 - CloseThreadpoolWait
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# CloseThreadpoolWait function


## -description


Releases the specified wait object.


## -parameters




### -param pwa [in, out]

A <b>TP_WAIT</b> structure that defines the wait object. The <a href="https://msdn.microsoft.com/ba19f5f9-d4b0-4865-9609-95e7697d61c0">CreateThreadpoolWait</a> function returns this structure.


## -returns



This function does not return a value.




## -remarks



The wait object is freed immediately if there are no outstanding callbacks; otherwise, the timer object is freed asynchronously after the outstanding callbacks complete.

If there is a cleanup group associated with the wait object, it is not necessary to call this function; calling the <a href="https://msdn.microsoft.com/9c78db13-d8dd-4eda-83d9-c9dbbfc6e822">CloseThreadpoolCleanupGroupMembers</a> function releases the  work, wait, and timer objects associated with the cleanup group.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/3d349c83-8b1a-4a5b-9625-be905d613b92">Using the Thread Pool Functions</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/ba19f5f9-d4b0-4865-9609-95e7697d61c0">CreateThreadpoolWait</a>



<a href="https://msdn.microsoft.com/ebd0ecad-a864-43cf-a1cb-e4c2d595ef81">SetThreadpoolWait</a>



<a href="https://msdn.microsoft.com/abe0798a-0b60-4bdb-a61e-45393f1e958d">Thread Pools</a>



<a href="https://msdn.microsoft.com/49c40b35-a0ed-40a1-9c35-5d3985ebd98f">WaitForThreadpoolWaitCallbacks</a>
 

 

