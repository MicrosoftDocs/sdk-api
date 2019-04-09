---
UID: NF:synchapi.SleepConditionVariableCS
title: SleepConditionVariableCS function (synchapi.h)
author: windows-sdk-content
description: Sleeps on the specified condition variable and releases the specified critical section as an atomic operation.
old-location: base\sleepconditionvariablecs.htm
tech.root: Sync
ms.assetid: af435aef-710a-4f97-bcfd-dcb7f2ec0253
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SleepConditionVariableCS, SleepConditionVariableCS function, base.sleepconditionvariablecs, synchapi/SleepConditionVariableCS, winbase/SleepConditionVariableCS
ms.topic: function
req.header: synchapi.h
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
 - API-MS-Win-Core-Synch-l1-2-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Synch-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - SleepConditionVariableCS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SleepConditionVariableCS function


## -description


Sleeps on the specified condition variable and releases the specified critical section as an atomic operation.


## -parameters




### -param ConditionVariable [in, out]

A pointer to the condition variable. This variable must be initialized using the <a href="https://msdn.microsoft.com/55cc8d1a-d5a8-4bb2-a5ac-50b4114b1b0b">InitializeConditionVariable</a> function.


### -param CriticalSection [in, out]

A pointer to the critical section object. This critical section must be entered exactly once by the caller at the time <b>SleepConditionVariableCS</b> is called.


### -param dwMilliseconds [in]

The time-out interval, in milliseconds. If the time-out interval elapses, the function re-acquires the critical section and returns zero. If <i>dwMilliseconds</i> is zero, the function tests the states of the specified objects and returns immediately. If <i>dwMilliseconds</i> is <b>INFINITE</b>, the function's time-out interval never elapses. For more information, see Remarks.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails or the time-out interval elapses, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Possible error codes include <b>ERROR_TIMEOUT</b>, which indicates that the time-out interval has elapsed before another thread has attempted to wake the sleeping thread.




## -remarks



A thread that is sleeping on a condition variable can be woken before the specified time-out interval has elapsed  using the <a href="https://msdn.microsoft.com/e175062a-ef25-4341-8197-df7ca6b008e6">WakeConditionVariable</a> or <a href="https://msdn.microsoft.com/1a57562a-fbbc-4a5f-910c-7a52a8dccbe3">WakeAllConditionVariable</a> function. In this case, the thread wakes when the wake processing is complete, and not when its time-out interval elapses. After the thread is woken, it re-acquires the critical section it released when the thread entered the sleeping state.

Condition variables are subject to spurious wakeups (those not associated with an explicit wake) and stolen wakeups (another thread manages to run before the woken thread). Therefore, you should recheck a predicate (typically in a <b>while</b> loop) after a sleep operation returns.


#### Examples

For an example that uses this function, see <a href="https://msdn.microsoft.com/0f79de15-6ce9-4d89-afb5-b4a2f0cf2fe3">Using Condition Variables</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/fef9bab0-cd69-4812-869a-b43a10772d86">Condition Variables</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

