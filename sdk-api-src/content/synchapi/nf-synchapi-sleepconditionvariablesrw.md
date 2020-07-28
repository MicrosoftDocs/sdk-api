---
UID: NF:synchapi.SleepConditionVariableSRW
title: SleepConditionVariableSRW function (synchapi.h)
description: Sleeps on the specified condition variable and releases the specified lock as an atomic operation.
helpviewer_keywords: ["SleepConditionVariableSRW","SleepConditionVariableSRW function","base.sleepconditionvariablesrw","synchapi/SleepConditionVariableSRW","winbase/SleepConditionVariableSRW"]
old-location: base\sleepconditionvariablesrw.htm
tech.root: backup
ms.assetid: 133f710f-5304-4b92-bec4-d9e8863bfa6d
ms.date: 12/05/2018
ms.keywords: SleepConditionVariableSRW, SleepConditionVariableSRW function, base.sleepconditionvariablesrw, synchapi/SleepConditionVariableSRW, winbase/SleepConditionVariableSRW
f1_keywords:
- synchapi/SleepConditionVariableSRW
dev_langs:
- c++
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
- SleepConditionVariableSRW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SleepConditionVariableSRW function


## -description


Sleeps on the specified condition variable and releases the specified lock as an atomic operation.


## -parameters




### -param ConditionVariable [in, out]

A pointer to the condition variable. This variable must be initialized using the <a href="https://docs.microsoft.com/windows/desktop/api/synchapi/nf-synchapi-initializeconditionvariable">InitializeConditionVariable</a> function.


### -param SRWLock [in, out]

A pointer to the lock. This lock must be held in the manner specified by the <i>Flags</i> parameter.


### -param dwMilliseconds [in]

The time-out interval, in milliseconds. The function returns if the interval elapses. If <i>dwMilliseconds</i> is zero, the function tests the states of the specified objects and returns immediately. If <i>dwMilliseconds</i> is <b>INFINITE</b>, the function's time-out interval never elapses.


### -param Flags [in]

If this parameter is <b>CONDITION_VARIABLE_LOCKMODE_SHARED</b>, the SRW lock is in shared mode. Otherwise, the lock is in exclusive mode.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If the timeout expires the function returns FALSE and <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_TIMEOUT.




## -remarks



If the lock is unlocked when this function is called, the function behavior is undefined.

The thread can be woken using the <a href="https://docs.microsoft.com/windows/desktop/api/synchapi/nf-synchapi-wakeconditionvariable">WakeConditionVariable</a> or <a href="https://docs.microsoft.com/windows/desktop/api/synchapi/nf-synchapi-wakeallconditionvariable">WakeAllConditionVariable</a> function.

Condition variables are subject to spurious wakeups (those not associated with an explicit wake) and stolen wakeups (another thread manages to run before the woken thread). Therefore, you should recheck a predicate (typically in a <b>while</b> loop) after a sleep operation returns.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Sync/slim-reader-writer--srw--locks">Slim Reader/Writer (SRW) Locks</a>



<a href="https://docs.microsoft.com/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>
 

 

