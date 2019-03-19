---
UID: NF:threadpoolapiset.CreateThreadpoolTimer
title: CreateThreadpoolTimer function (threadpoolapiset.h)
author: windows-sdk-content
description: Creates a new timer object.
old-location: base\createthreadpooltimer.htm
tech.root: ProcThread
ms.assetid: 1fa98b79-e646-4e48-9979-1817d2c1b713
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateThreadpoolTimer, CreateThreadpoolTimer function, base.createthreadpooltimer, threadpoolapiset/CreateThreadpoolTimer, winbase/CreateThreadpoolTimer
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
 - CreateThreadpoolTimer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateThreadpoolTimer function


## -description


Creates a new timer object.


## -parameters




### -param pfnti [in]

The callback function to call each time the timer object expires. For details, see <a href="https://msdn.microsoft.com/105bdf34-e61d-4419-988b-625589064d2a">TimerCallback</a>.


### -param pv [in, out, optional]

Optional application-defined data to pass to the callback function.


### -param pcbe [in, optional]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines the environment in which to execute the callback. The <a href="https://msdn.microsoft.com/ad610b7a-9865-4feb-81d2-491f9f87ef3e">InitializeThreadpoolEnvironment</a> function returns this structure.

If this parameter is NULL, the callback executes in the default callback environment. For more information, see <a href="https://msdn.microsoft.com/ad610b7a-9865-4feb-81d2-491f9f87ef3e">InitializeThreadpoolEnvironment</a>.


## -returns



If the function succeeds, it returns a <b>TP_TIMER</b> structure that defines the timer object. Applications do not modify the members of this structure.

If the function fails, it returns NULL. To retrieve extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To set the timer object, call the <a href="https://msdn.microsoft.com/017f88c6-e14c-47ba-94d2-e7bb0dc95d12">SetThreadpoolTimer</a> function.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/3d349c83-8b1a-4a5b-9625-be905d613b92">Using the Thread Pool Functions</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/c1270c5d-a1f5-4481-a343-c1ff3301a56e">CloseThreadpoolTimer</a>



<a href="https://msdn.microsoft.com/f9dee0aa-6310-4218-b207-72a24c5019e2">IsThreadpoolTimerSet</a>



<a href="https://msdn.microsoft.com/017f88c6-e14c-47ba-94d2-e7bb0dc95d12">SetThreadpoolTimer</a>



<a href="https://msdn.microsoft.com/abe0798a-0b60-4bdb-a61e-45393f1e958d">Thread Pools</a>



<a href="https://msdn.microsoft.com/511488b8-9e92-47b9-8b3c-7ece9d9f996c">WaitForThreadpoolTimerCallbacks</a>
 

 

