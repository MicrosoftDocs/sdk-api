---
UID: NF:synchapi.InitializeConditionVariable
title: InitializeConditionVariable function (synchapi.h)
description: Initializes a condition variable.helpviewer_keywords: ["InitializeConditionVariable","InitializeConditionVariable function","base.initializeconditionvariable","synchapi/InitializeConditionVariable","winbase/InitializeConditionVariable"]
old-location: base\initializeconditionvariable.htm
tech.root: Sync
ms.assetid: 55cc8d1a-d5a8-4bb2-a5ac-50b4114b1b0b
ms.date: 12/05/2018
ms.keywords: InitializeConditionVariable, InitializeConditionVariable function, base.initializeconditionvariable, synchapi/InitializeConditionVariable, winbase/InitializeConditionVariable
f1_keywords:
- synchapi/InitializeConditionVariable
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
- vertdll.dll
api_name:
- InitializeConditionVariable
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# InitializeConditionVariable function


## -description


Initializes a condition variable.


## -parameters




### -param ConditionVariable [out]

A pointer to the condition variable.


## -remarks



Threads  can atomically release a lock and enter the sleeping state using the <a href="https://docs.microsoft.com/windows/desktop/api/synchapi/nf-synchapi-sleepconditionvariablecs">SleepConditionVariableCS</a> or <a href="https://docs.microsoft.com/windows/desktop/api/synchapi/nf-synchapi-sleepconditionvariablesrw">SleepConditionVariableSRW</a> function. The threads are woken using the <a href="https://docs.microsoft.com/windows/desktop/api/synchapi/nf-synchapi-wakeconditionvariable">WakeConditionVariable</a> or <a href="https://docs.microsoft.com/windows/desktop/api/synchapi/nf-synchapi-wakeallconditionvariable">WakeAllConditionVariable</a> function.

Condition variables are user-mode objects that cannot be shared across processes.

A condition variable cannot be moved or copied. The process must not modify the object, and must instead treat it as logically opaque. Only use the condition variable functions to manage condition variables.


#### Examples

For an example that uses this function, see <a href="https://docs.microsoft.com/windows/desktop/Sync/using-condition-variables">Using Condition Variables</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Sync/condition-variables">Condition Variables</a>



<a href="https://docs.microsoft.com/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>
 

 

