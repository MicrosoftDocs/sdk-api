---
UID: NF:synchapi.WakeConditionVariable
title: WakeConditionVariable function (synchapi.h)
description: Wake a single thread waiting on the specified condition variable.
helpviewer_keywords: ["WakeConditionVariable","WakeConditionVariable function","base.wakeconditionvariable","synchapi/WakeConditionVariable","winbase/WakeConditionVariable"]
old-location: base\wakeconditionvariable.htm
tech.root: base
ms.assetid: e175062a-ef25-4341-8197-df7ca6b008e6
ms.date: 02/05/2024
ms.keywords: WakeConditionVariable, WakeConditionVariable function, base.wakeconditionvariable, synchapi/WakeConditionVariable, winbase/WakeConditionVariable
req.header: synchapi.h
req.include-header: Windows.h on Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
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
 - WakeConditionVariable
 - synchapi/WakeConditionVariable
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
 - WakeConditionVariable
---

# WakeConditionVariable function

## -description

Wake a single thread waiting on the specified condition variable.

## -parameters

### -param ConditionVariable [in, out]

A pointer to the condition variable.

## -remarks

The [WakeAllConditionVariable](nf-synchapi-wakeallconditionvariable.md) wakes all waiting threads while the **WakeConditionVariable** wakes only a single thread. Waking one thread is similar to setting an auto-reset event, while waking all threads is similar to pulsing a manual reset event but more reliable (see [PulseEvent](../winbase/nf-winbase-pulseevent.md) for details).

#### Examples

For an example that uses this function, see [Using Condition Variables](/windows/win32/Sync/using-condition-variables).

## -see-also

[Condition Variables](/windows/win32/Sync/condition-variables)

[Synchronization Functions](/windows/win32/Sync/synchronization-functions)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
