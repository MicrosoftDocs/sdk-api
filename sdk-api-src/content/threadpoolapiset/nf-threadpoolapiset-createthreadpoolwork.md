---
UID: NF:threadpoolapiset.CreateThreadpoolWork
title: CreateThreadpoolWork function
author: windows-sdk-content
description: Creates a new work object.
old-location: base\createthreadpoolwork.htm
old-project: procthread
ms.assetid: 50647d87-1768-4918-8376-a6a04daca621
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateThreadpoolWork, CreateThreadpoolWork function, base.createthreadpoolwork, threadpoolapiset/CreateThreadpoolWork
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: threadpoolapiset.h
req.include-header: Windows.h
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
 - CreateThreadpoolWork
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# CreateThreadpoolWork function


## -description


Creates a new work object.


## -parameters




### -param pfnwk [in]

The callback function. A worker thread calls this callback each time you call <a href="https://msdn.microsoft.com/28df173d-b78c-4158-97d5-63117a2d3967">SubmitThreadpoolWork</a> to post the work object. For details, see <a href="https://msdn.microsoft.com/a63bf128-117e-4654-85d4-b0e7a0029ccb">WorkCallback</a>.


### -param pv [in, out, optional]

Optional application-defined data to pass to the callback function.


### -param pcbe [in, optional]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines the  environment in which to execute the callback. The <a href="https://msdn.microsoft.com/ad610b7a-9865-4feb-81d2-491f9f87ef3e">InitializeThreadpoolEnvironment</a> function returns this structure.

If this parameter is NULL, the callback executes in the default callback environment. For more information, see <a href="https://msdn.microsoft.com/ad610b7a-9865-4feb-81d2-491f9f87ef3e">InitializeThreadpoolEnvironment</a>.


## -returns



If the function succeeds, it returns a <b>TP_WORK</b> structure that defines the work object. Applications do not modify the members of this structure.

If the function fails, it returns NULL. To retrieve extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/3d349c83-8b1a-4a5b-9625-be905d613b92">Using the Thread Pool Functions</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/89d7362e-0814-4f7e-a27f-8a297e210559">CloseThreadpoolWork</a>



<a href="https://msdn.microsoft.com/28df173d-b78c-4158-97d5-63117a2d3967">SubmitThreadpoolWork</a>



<a href="https://msdn.microsoft.com/abe0798a-0b60-4bdb-a61e-45393f1e958d">Thread Pools</a>



<a href="https://msdn.microsoft.com/97c16892-d6ef-4216-ac79-344e83ab35bc">WaitForThreadpoolWorkCallbacks</a>
 

 

