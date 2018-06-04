---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# SleepConditionVariableSRW function


## -description


Sleeps on the specified condition variable and releases the specified lock as an atomic operation.


## -parameters




### -param ConditionVariable [in, out]

A pointer to the condition variable. This variable must be initialized using the <a href="https://msdn.microsoft.com/55cc8d1a-d5a8-4bb2-a5ac-50b4114b1b0b">InitializeConditionVariable</a> function.


### -param SRWLock [in, out]

A pointer to the lock. This lock must be held in the manner specified by the <i>Flags</i> parameter.


### -param dwMilliseconds [in]

The time-out interval, in milliseconds. The function returns if the interval elapses. If <i>dwMilliseconds</i> is zero, the function tests the states of the specified objects and returns immediately. If <i>dwMilliseconds</i> is <b>INFINITE</b>, the function's time-out interval never elapses.


### -param Flags [in]

If this parameter is <b>CONDITION_VARIABLE_LOCKMODE_SHARED</b>, the SRW lock is in shared mode. Otherwise, the lock is in exclusive mode.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If the timeout expires the function returns FALSE and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_TIMEOUT.




## -remarks



If the lock is unlocked when this function is called, the function behavior is undefined.

The thread can be woken using the <a href="https://msdn.microsoft.com/e175062a-ef25-4341-8197-df7ca6b008e6">WakeConditionVariable</a> or <a href="https://msdn.microsoft.com/1a57562a-fbbc-4a5f-910c-7a52a8dccbe3">WakeAllConditionVariable</a> function.

Condition variables are subject to spurious wakeups (those not associated with an explicit wake) and stolen wakeups (another thread manages to run before the woken thread). Therefore, you should recheck a predicate (typically in a <b>while</b> loop) after a sleep operation returns.




## -see-also




<a href="https://msdn.microsoft.com/2d439b21-291f-4ff0-910a-c1c27e800019">Slim Reader/Writer (SRW) Locks</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

