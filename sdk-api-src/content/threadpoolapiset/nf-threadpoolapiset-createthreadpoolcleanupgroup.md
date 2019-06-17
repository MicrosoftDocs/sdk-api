---
UID: NF:threadpoolapiset.CreateThreadpoolCleanupGroup
title: CreateThreadpoolCleanupGroup function (threadpoolapiset.h)
author: windows-sdk-content
description: Creates a cleanup group that applications can use to track one or more thread pool callbacks.
old-location: base\createthreadpoolcleanupgroup.htm
tech.root: ProcThread
ms.assetid: 668593fe-2ed1-418d-8cd5-5fac61826ea1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateThreadpoolCleanupGroup, CreateThreadpoolCleanupGroup function, base.createthreadpoolcleanupgroup, threadpoolapiset/CreateThreadpoolCleanupGroup, winbase/CreateThreadpoolCleanupGroup
ms.topic: function
f1_keywords: ["threadpoolapiset/CreateThreadpoolCleanupGroup"]
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
ms.custom: 19H1
---

# CreateThreadpoolCleanupGroup function


## -description


Creates a cleanup group that applications can use to track one or more thread pool callbacks.


## -parameters






## -returns



If the function succeeds, it returns a <b>TP_CLEANUP_GROUP</b> structure of the newly allocated cleanup group. Applications do not modify the members of this structure.

If function fails, it returns NULL. To retrieve extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



After creating the cleanup group, call <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbackcleanupgroup">SetThreadpoolCallbackCleanupGroup</a> to associate the cleanup group with a callback environment.

A member is added to the group each time you call one of the following functions:<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolio">CreateThreadpoolIo</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpooltimer">CreateThreadpoolTimer</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwait">CreateThreadpoolWait</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwork">CreateThreadpoolWork</a>
</li>
</ul>


You use one of the following corresponding close functions to remove a member from the group.<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolio">CloseThreadpoolIo</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpooltimer">CloseThreadpoolTimer</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolwait">CloseThreadpoolWait</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolwork">CloseThreadpoolWork</a>
</li>
</ul>


To close all the callbacks, call <a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolcleanupgroupmembers">CloseThreadpoolCleanupGroupMembers</a>.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="https://docs.microsoft.com/windows/desktop/ProcThread/using-the-thread-pool-functions">Using the Thread Pool Functions</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolcleanupgroup">CloseThreadpoolCleanupGroup</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolcleanupgroupmembers">CloseThreadpoolCleanupGroupMembers</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbackcleanupgroup">SetThreadpoolCallbackCleanupGroup</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/thread-pools">Thread Pools</a>
 

 

