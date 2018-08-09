---
UID: NF:synchapi.WakeAllConditionVariable
title: WakeAllConditionVariable function
author: windows-sdk-content
description: Wake all threads waiting on the specified condition variable.
old-location: base\wakeallconditionvariable.htm
old-project: sync
ms.assetid: 1a57562a-fbbc-4a5f-910c-7a52a8dccbe3
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WakeAllConditionVariable, WakeAllConditionVariable function, base.wakeallconditionvariable, synchapi/WakeAllConditionVariable, winbase/WakeAllConditionVariable
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: ITEMPROP, *LPITEMPROP
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
 - WakeAllConditionVariable
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# WakeAllConditionVariable function


## -description


Wake all threads waiting on the specified condition variable.


## -parameters




### -param ConditionVariable [in, out]

A pointer to the condition variable.


## -returns



This function does not return a value.




## -remarks



The <b>WakeAllConditionVariable</b> wakes all 
    waiting threads while the <a href="https://msdn.microsoft.com/e175062a-ef25-4341-8197-df7ca6b008e6">WakeConditionVariable</a> 
    wakes only a single thread. Waking one thread is similar to setting an auto-reset event, while waking all threads 
    is similar to pulsing a manual reset event but more reliable (see 
    <a href="https://msdn.microsoft.com/b3cfe15a-1a0e-4c29-8840-032e56404400">PulseEvent</a> for details).




## -see-also




<a href="https://msdn.microsoft.com/fef9bab0-cd69-4812-869a-b43a10772d86">Condition Variables</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

