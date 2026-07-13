---
UID: NF:synchapi.SleepConditionVariableCS
title: SleepConditionVariableCS function (synchapi.h)
description: Sleeps on the specified condition variable and releases the specified critical section as an atomic operation.
helpviewer_keywords: ["SleepConditionVariableCS","SleepConditionVariableCS function","base.sleepconditionvariablecs","synchapi/SleepConditionVariableCS","winbase/SleepConditionVariableCS"]
old-location: base\sleepconditionvariablecs.htm
tech.root: base
ms.assetid: af435aef-710a-4f97-bcfd-dcb7f2ec0253
ms.date: 02/05/2024
ms.keywords: SleepConditionVariableCS, SleepConditionVariableCS function, base.sleepconditionvariablecs, synchapi/SleepConditionVariableCS, winbase/SleepConditionVariableCS
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
 - SleepConditionVariableCS
 - synchapi/SleepConditionVariableCS
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
 - SleepConditionVariableCS
---

# SleepConditionVariableCS function

## -description

Sleeps on the specified condition variable and releases the specified critical section as an atomic operation.

## -parameters

### -param ConditionVariable [in, out]

A pointer to the condition variable. This variable must be initialized by either calling [InitializeConditionVariable](nf-synchapi-initializeconditionvariable.md) (to initialize the structure dynamically) or assign the constant CONDITION_VARIABLE_INIT to the structure variable (to initialize the structure statically).

### -param CriticalSection [in, out]

A pointer to the critical section object. This critical section must be entered exactly once by the caller at the time **SleepConditionVariableCS** is called.

### -param dwMilliseconds [in]

The time-out interval, in milliseconds. If the time-out interval elapses, the function re-acquires the critical section and returns zero. If *dwMilliseconds* is zero, the function tests the states of the specified objects and returns immediately. If *dwMilliseconds* is **INFINITE**, the function's time-out interval never elapses. For more information, see Remarks.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails or the time-out interval elapses, the return value is zero. To get extended error information, call [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md). Possible error codes include **ERROR_TIMEOUT**, which indicates that the time-out interval has elapsed before another thread has attempted to wake the sleeping thread.

## -remarks

A thread that is sleeping on a condition variable can be woken before the specified time-out interval has elapsed  using the [WakeConditionVariable](nf-synchapi-wakeconditionvariable.md) or [WakeAllConditionVariable](nf-synchapi-wakeallconditionvariable.md) function. In this case, the thread wakes when the wake processing is complete, and not when its time-out interval elapses. After the thread is woken, it re-acquires the critical section it released when the thread entered the sleeping state.

Condition variables are subject to spurious wakeups (those not associated with an explicit wake) and stolen wakeups (another thread manages to run before the woken thread). Therefore, you should recheck a predicate (typically in a `while` loop) after a sleep operation returns.

#### Examples

For an example that uses this function, see [Using Condition Variables](/windows/win32/Sync/using-condition-variables).

## -see-also

[Condition Variables](/windows/win32/Sync/condition-variables)

[Synchronization Functions](/windows/win32/Sync/synchronization-functions)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
