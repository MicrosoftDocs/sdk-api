---
UID: NF:threadpoolapiset.CreateThreadpoolTimer
title: CreateThreadpoolTimer function (threadpoolapiset.h)
description: Creates a new timer object.
helpviewer_keywords: ["CreateThreadpoolTimer","CreateThreadpoolTimer function","base.createthreadpooltimer","threadpoolapiset/CreateThreadpoolTimer","winbase/CreateThreadpoolTimer"]
old-location: base\createthreadpooltimer.htm
tech.root: backup
ms.assetid: 1fa98b79-e646-4e48-9979-1817d2c1b713
ms.date: 12/05/2018
ms.keywords: CreateThreadpoolTimer, CreateThreadpoolTimer function, base.createthreadpooltimer, threadpoolapiset/CreateThreadpoolTimer, winbase/CreateThreadpoolTimer
req.header: threadpoolapiset.h
req.include-header: Windows.h on Windows 7, Windows Server 2008  Windows Server 2008 R2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateThreadpoolTimer
 - threadpoolapiset/CreateThreadpoolTimer
dev_langs:
 - c++
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
---

# CreateThreadpoolTimer function


## -description

Creates a new timer object.

## -parameters

### -param pfnti [in]

The callback function to call each time the timer object expires. For details, see <a href="/previous-versions/windows/desktop/legacy/ms686790(v=vs.85)">TimerCallback</a>.

### -param pv [in, out, optional]

Optional application-defined data to pass to the callback function.

### -param pcbe [in, optional]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines the environment in which to execute the callback. The <a href="/windows/desktop/api/winbase/nf-winbase-initializethreadpoolenvironment">InitializeThreadpoolEnvironment</a> function returns this structure.

If this parameter is NULL, the callback executes in the default callback environment. For more information, see <a href="/windows/desktop/api/winbase/nf-winbase-initializethreadpoolenvironment">InitializeThreadpoolEnvironment</a>.

## -returns

If the function succeeds, it returns a pointer to a <b>TP_TIMER</b> structure that defines the timer object. Applications do not modify the members of this structure.

If the function fails, it returns NULL. To retrieve extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To set the timer object, call the <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpooltimer">SetThreadpoolTimer</a> function.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="/windows/desktop/ProcThread/using-the-thread-pool-functions">Using the Thread Pool Functions</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpooltimer">CloseThreadpoolTimer</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-isthreadpooltimerset">IsThreadpoolTimerSet</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpooltimer">SetThreadpoolTimer</a>



<a href="/windows/desktop/ProcThread/thread-pools">Thread Pools</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpooltimercallbacks">WaitForThreadpoolTimerCallbacks</a>