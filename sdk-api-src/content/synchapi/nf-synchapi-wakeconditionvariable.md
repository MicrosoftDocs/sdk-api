---
UID: NF:synchapi.WakeConditionVariable
title: WakeConditionVariable function
author: windows-sdk-content
description: Wake a single thread waiting on the specified condition variable.
old-location: base\wakeconditionvariable.htm
tech.root: Sync
ms.assetid: e175062a-ef25-4341-8197-df7ca6b008e6
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: WakeConditionVariable, WakeConditionVariable function, base.wakeconditionvariable, synchapi/WakeConditionVariable, winbase/WakeConditionVariable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- WakeConditionVariable
: 
---

# WakeConditionVariable function


## -description


Wake a single thread waiting on the specified condition variable.


## -parameters




### -param ConditionVariable [in, out]

A pointer to the condition variable.


## -returns



This function does not return a value.




## -remarks



The <a href="https://msdn.microsoft.com/1a57562a-fbbc-4a5f-910c-7a52a8dccbe3">WakeAllConditionVariable</a> wakes all waiting threads while the <b>WakeConditionVariable</b> wakes only a single thread. Waking one thread is similar to setting an auto-reset event, while waking all threads is similar to pulsing a manual reset event but more reliable (see <a href="https://msdn.microsoft.com/b3cfe15a-1a0e-4c29-8840-032e56404400">PulseEvent</a> for details).


#### Examples

For an example that uses this function, see <a href="https://msdn.microsoft.com/0f79de15-6ce9-4d89-afb5-b4a2f0cf2fe3">Using Condition Variables</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/fef9bab0-cd69-4812-869a-b43a10772d86">Condition Variables</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

