---
UID: NF:synchapi.WakeConditionVariable
title: WakeConditionVariable function (synchapi.h)
description: Wake a single thread waiting on the specified condition variable.
helpviewer_keywords: ["WakeConditionVariable","WakeConditionVariable function","base.wakeconditionvariable","synchapi/WakeConditionVariable","winbase/WakeConditionVariable"]
old-location: base\wakeconditionvariable.htm
tech.root: base
ms.assetid: e175062a-ef25-4341-8197-df7ca6b008e6
ms.date: 12/05/2018
ms.keywords: WakeConditionVariable, WakeConditionVariable function, base.wakeconditionvariable, synchapi/WakeConditionVariable, winbase/WakeConditionVariable
req.header: synchapi.h
req.include-header: Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
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

The <a href="/windows/desktop/api/synchapi/nf-synchapi-wakeallconditionvariable">WakeAllConditionVariable</a> wakes all waiting threads while the <b>WakeConditionVariable</b> wakes only a single thread. Waking one thread is similar to setting an auto-reset event, while waking all threads is similar to pulsing a manual reset event but more reliable (see <a href="/windows/desktop/api/winbase/nf-winbase-pulseevent">PulseEvent</a> for details).


#### Examples

For an example that uses this function, see <a href="/windows/desktop/Sync/using-condition-variables">Using Condition Variables</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/Sync/condition-variables">Condition Variables</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>