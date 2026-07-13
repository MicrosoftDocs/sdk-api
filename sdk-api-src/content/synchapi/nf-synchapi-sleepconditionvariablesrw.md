---
UID: NF:synchapi.SleepConditionVariableSRW
title: SleepConditionVariableSRW function (synchapi.h)
description: Sleeps on the specified condition variable and releases the specified lock as an atomic operation.
helpviewer_keywords: ["SleepConditionVariableSRW","SleepConditionVariableSRW function","base.sleepconditionvariablesrw","synchapi/SleepConditionVariableSRW","winbase/SleepConditionVariableSRW"]
old-location: base\sleepconditionvariablesrw.htm
tech.root: base
ms.assetid: 133f710f-5304-4b92-bec4-d9e8863bfa6d
ms.date: 02/05/2024
ms.keywords: SleepConditionVariableSRW, SleepConditionVariableSRW function, base.sleepconditionvariablesrw, synchapi/SleepConditionVariableSRW, winbase/SleepConditionVariableSRW
req.header: synchapi.h
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
 - SleepConditionVariableSRW
 - synchapi/SleepConditionVariableSRW
dev_langs:
 - c++
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
 - vertdll.dll
api_name:
 - SleepConditionVariableSRW
---

# SleepConditionVariableSRW function

## -description

Sleeps on the specified condition variable and releases the specified lock as an atomic operation.

## -parameters

### -param ConditionVariable [in, out]

A pointer to the condition variable. This variable must be initialized by either calling [InitializeConditionVariable](nf-synchapi-initializeconditionvariable.md) (to initialize the structure dynamically) or assign the constant CONDITION_VARIABLE_INIT to the structure variable (to initialize the structure statically).

### -param SRWLock [in, out]

A pointer to the lock. This lock must be held in the manner specified by the *Flags* parameter.

### -param dwMilliseconds [in]

The time-out interval, in milliseconds. The function returns if the interval elapses. If *dwMilliseconds* is zero, the function tests the states of the specified objects and returns immediately. If *dwMilliseconds* is **INFINITE**, the function's time-out interval never elapses.

### -param Flags [in]

If this parameter is **CONDITION_VARIABLE_LOCKMODE_SHARED**, the SRW lock is in shared mode. Otherwise, the lock is in exclusive mode.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is `0`. To get extended error information, call [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md).

If the timeout expires the function returns `FALSE` and [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md) returns **ERROR_TIMEOUT**.

## -remarks

If the lock is unlocked when this function is called, the function behavior is undefined.

The thread can be woken using the [WakeConditionVariable](nf-synchapi-wakeconditionvariable.md) or [WakeAllConditionVariable](nf-synchapi-wakeallconditionvariable.md) function. After the thread is woken, it re-acquires the lock it released when the thread entered the sleeping state.

Condition variables are subject to spurious wakeups (those not associated with an explicit wake) and stolen wakeups (another thread manages to run before the woken thread). Therefore, you should recheck a predicate (typically in a `while` loop) after a sleep operation returns.

## -see-also

[Slim Reader/Writer (SRW) Locks](/windows/win32/Sync/slim-reader-writer--srw--locks)

[Synchronization Functions](/windows/win32/Sync/synchronization-functions)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
