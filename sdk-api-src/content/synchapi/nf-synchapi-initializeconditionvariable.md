---
UID: NF:synchapi.InitializeConditionVariable
title: InitializeConditionVariable function
author: windows-sdk-content
description: Initializes a condition variable.
old-location: base\initializeconditionvariable.htm
tech.root: sync
ms.assetid: 55cc8d1a-d5a8-4bb2-a5ac-50b4114b1b0b
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: InitializeConditionVariable, InitializeConditionVariable function, base.initializeconditionvariable, synchapi/InitializeConditionVariable, winbase/InitializeConditionVariable
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - InitializeConditionVariable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InitializeConditionVariable function


## -description


Initializes a condition variable.


## -parameters




### -param ConditionVariable [out]

A pointer to the condition variable.


## -returns



This function does not return a value.




## -remarks



Threads  can atomically release a lock and enter the sleeping state using the <a href="https://msdn.microsoft.com/af435aef-710a-4f97-bcfd-dcb7f2ec0253">SleepConditionVariableCS</a> or <a href="https://msdn.microsoft.com/133f710f-5304-4b92-bec4-d9e8863bfa6d">SleepConditionVariableSRW</a> function. The threads are woken using the <a href="https://msdn.microsoft.com/e175062a-ef25-4341-8197-df7ca6b008e6">WakeConditionVariable</a> or <a href="https://msdn.microsoft.com/1a57562a-fbbc-4a5f-910c-7a52a8dccbe3">WakeAllConditionVariable</a> function.

Condition variables are user-mode objects that cannot be shared across processes.

A condition variable cannot be moved or copied. The process must not modify the object, and must instead treat it as logically opaque. Only use the condition variable functions to manage condition variables.


#### Examples

For an example that uses this function, see <a href="https://msdn.microsoft.com/0f79de15-6ce9-4d89-afb5-b4a2f0cf2fe3">Using Condition Variables</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/fef9bab0-cd69-4812-869a-b43a10772d86">Condition Variables</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

