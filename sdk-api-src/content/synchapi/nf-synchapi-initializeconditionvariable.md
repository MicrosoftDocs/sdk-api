---
UID: NF:synchapi.InitializeConditionVariable
title: InitializeConditionVariable function (synchapi.h)
description: Initializes a condition variable.
helpviewer_keywords: ["InitializeConditionVariable","InitializeConditionVariable function","base.initializeconditionvariable","synchapi/InitializeConditionVariable","winbase/InitializeConditionVariable"]
old-location: base\initializeconditionvariable.htm
tech.root: base
ms.assetid: 55cc8d1a-d5a8-4bb2-a5ac-50b4114b1b0b
ms.date: 02/05/2024
ms.keywords: InitializeConditionVariable, InitializeConditionVariable function, base.initializeconditionvariable, synchapi/InitializeConditionVariable, winbase/InitializeConditionVariable
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
 - InitializeConditionVariable
 - synchapi/InitializeConditionVariable
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
 - InitializeConditionVariable
---

# InitializeConditionVariable function

## -description

Initializes a condition variable.

## -parameters

### -param ConditionVariable [out]

A pointer to the condition variable.

## -remarks

Threads  can atomically release a lock and enter the sleeping state using the [SleepConditionVariableCS](nf-synchapi-sleepconditionvariablecs.md) or [SleepConditionVariableSRW](nf-synchapi-sleepconditionvariablesrw.md) function. The threads are woken using the [WakeConditionVariable](nf-synchapi-wakeconditionvariable.md) or [WakeAllConditionVariable](nf-synchapi-wakeallconditionvariable.md) function.

Condition variables are user-mode objects that cannot be shared across processes.

A condition variable cannot be moved or copied while in use. The process must not modify the object, and must instead treat it as logically opaque. Only use the condition variable functions to manage condition variables.

A condition variable with no waiting threads is in its initial state and can be copied, moved, and forgotten without being explicitly destroyed.

#### Examples

For an example that uses this function, see [Using Condition Variables](/windows/win32/Sync/using-condition-variables).

## -see-also

[Condition Variables](/windows/win32/Sync/condition-variables)

[Synchronization Functions](/windows/win32/Sync/synchronization-functions)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
