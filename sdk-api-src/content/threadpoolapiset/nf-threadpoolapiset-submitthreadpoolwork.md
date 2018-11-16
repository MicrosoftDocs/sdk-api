---
UID: NF:threadpoolapiset.SubmitThreadpoolWork
title: SubmitThreadpoolWork function
author: windows-sdk-content
description: Posts a work object to the thread pool. A worker thread calls the work object's callback function.
old-location: base\submitthreadpoolwork.htm
tech.root: ProcThread
ms.assetid: 28df173d-b78c-4158-97d5-63117a2d3967
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: SubmitThreadpoolWork, SubmitThreadpoolWork function, base.submitthreadpoolwork, threadpoolapiset/SubmitThreadpoolWork, winbase/SubmitThreadpoolWork
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
 - SubmitThreadpoolWork
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- SubmitThreadpoolWork
: 
---

# SubmitThreadpoolWork function


## -description


Posts a work object to the thread pool. A worker thread calls the work object's callback function.


## -parameters




### -param pwk [in, out]

A <b>TP_WORK</b> structure that defines the work object. The <a href="https://msdn.microsoft.com/50647d87-1768-4918-8376-a6a04daca621">CreateThreadpoolWork</a> function returns this structure.


## -returns



This function does not return a value.




## -remarks



You can post a work object one or more times (up to MAXULONG) without waiting for prior callbacks to complete.  The callbacks will execute in parallel. To improve efficiency, the thread pool may throttle the threads.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/3d349c83-8b1a-4a5b-9625-be905d613b92">Using the Thread Pool Functions</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/89d7362e-0814-4f7e-a27f-8a297e210559">CloseThreadpoolWork</a>



<a href="https://msdn.microsoft.com/50647d87-1768-4918-8376-a6a04daca621">CreateThreadpoolWork</a>



<a href="https://msdn.microsoft.com/abe0798a-0b60-4bdb-a61e-45393f1e958d">Thread Pools</a>



<a href="https://msdn.microsoft.com/97c16892-d6ef-4216-ac79-344e83ab35bc">WaitForThreadpoolWorkCallbacks</a>
 

 

