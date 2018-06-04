---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

