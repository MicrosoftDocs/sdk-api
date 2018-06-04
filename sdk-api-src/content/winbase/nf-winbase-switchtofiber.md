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

# SwitchToFiber function


## -description


Schedules a fiber. The function must be called on a fiber.


## -parameters




### -param lpFiber [in]

The address of the fiber to be scheduled.


## -returns



This function does not return a value.




## -remarks



You create fibers with the 
<a href="https://msdn.microsoft.com/3e44776b-7ef2-43fb-a2ae-e8ab7e20644b">CreateFiber</a> function. Before you can schedule fibers associated with a thread, you must call 
<a href="https://msdn.microsoft.com/31954a7e-b9a3-4d60-b43a-54fe0047f380">ConvertThreadToFiber</a> to set up an area in which to save the fiber state information. The thread is now the currently executing fiber.

The 
<b>SwitchToFiber</b> function saves the state information of the current fiber and restores the state of the specified fiber. You can call 
<b>SwitchToFiber</b> with the address of a fiber created by a different thread. To do this, you must have the address returned to the other thread when it called 
<a href="https://msdn.microsoft.com/3e44776b-7ef2-43fb-a2ae-e8ab7e20644b">CreateFiber</a> and you must use proper synchronization.

Avoid making the following call:

<pre class="syntax" xml:space="preserve"><code>SwitchToFiber( GetCurrentFiber() );</code></pre>
This call can cause unpredictable problems.

To compile an application that uses this function, define _WIN32_WINNT as 0x0400 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/31954a7e-b9a3-4d60-b43a-54fe0047f380">ConvertThreadToFiber</a>



<a href="https://msdn.microsoft.com/3e44776b-7ef2-43fb-a2ae-e8ab7e20644b">CreateFiber</a>



<a href="https://msdn.microsoft.com/6283f56b-23ae-4840-abd0-2478a50c670c">Fibers</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>
 

 

