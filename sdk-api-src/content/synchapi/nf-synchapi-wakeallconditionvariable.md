---
UID: NF:synchapi.WakeAllConditionVariable
title: WakeAllConditionVariable function (synchapi.h)
description: Wake all threads waiting on the specified condition variable.
helpviewer_keywords: ["WakeAllConditionVariable","WakeAllConditionVariable function","base.wakeallconditionvariable","synchapi/WakeAllConditionVariable","winbase/WakeAllConditionVariable"]
old-location: base\wakeallconditionvariable.htm
tech.root: base
ms.assetid: 1a57562a-fbbc-4a5f-910c-7a52a8dccbe3
ms.date: 12/05/2018
ms.keywords: WakeAllConditionVariable, WakeAllConditionVariable function, base.wakeallconditionvariable, synchapi/WakeAllConditionVariable, winbase/WakeAllConditionVariable
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WakeAllConditionVariable
 - synchapi/WakeAllConditionVariable
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
 - WakeAllConditionVariable
---

# WakeAllConditionVariable function


## -description

Wake all threads waiting on the specified condition variable.

## -parameters

### -param ConditionVariable [in, out]

A pointer to the condition variable.

## -remarks

The <b>WakeAllConditionVariable</b> wakes all 
    waiting threads while the <a href="/windows/desktop/api/synchapi/nf-synchapi-wakeconditionvariable">WakeConditionVariable</a> 
    wakes only a single thread. Waking one thread is similar to setting an auto-reset event, while waking all threads 
    is similar to pulsing a manual reset event but more reliable (see 
    <a href="/windows/desktop/api/winbase/nf-winbase-pulseevent">PulseEvent</a> for details).

## -see-also

<a href="/windows/desktop/Sync/condition-variables">Condition Variables</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>