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

# tagCOWAIT_FLAGS enumeration


## -description


Specifies the behavior of the <a href="https://msdn.microsoft.com/3eeecd34-aa94-4a48-8b41-167a71b52860">CoWaitForMultipleHandles</a> function.


## -enum-fields




### -field COWAIT_DEFAULT


### -field COWAIT_WAITALL

If set, the call to <a href="https://msdn.microsoft.com/3eeecd34-aa94-4a48-8b41-167a71b52860">CoWaitForMultipleHandles</a> will return S_OK only when all handles associated with the synchronization object have been signaled and an input event has been received, all at the same time.  In this case, the behavior of <b>CoWaitForMultipleHandles</b> corresponds to  the behavior of the <a href="https://msdn.microsoft.com/1774b721-3ad4-492e-96af-b71de9066f0c">MsgWaitForMultipleObjectsEx</a> function with the <i>dwFlags</i> parameter set to <b>MWMO_WAITALL</b>. If <b>COWAIT_WAITALL</b> is not set, the call to <b>CoWaitForMultipleHandles</b> will return S_OK as soon as any handle associated with the synchronization object has been signaled, regardless of whether an input event is received.


### -field COWAIT_ALERTABLE

If set, the call to <a href="https://msdn.microsoft.com/3eeecd34-aa94-4a48-8b41-167a71b52860">CoWaitForMultipleHandles</a> will return S_OK if an asynchronous procedure call (APC) has been queued to the calling thread with a call to the <a href="https://msdn.microsoft.com/5b141372-7c95-4eb2-987b-64fdf7d0783d">QueueUserAPC</a> function, even if no handle has been signaled.


### -field COWAIT_INPUTAVAILABLE

If set, the call to <a href="https://msdn.microsoft.com/3eeecd34-aa94-4a48-8b41-167a71b52860">CoWaitForMultipleHandles</a> will return S_OK  if input exists for the queue, even if the input has been seen (but not removed) using a call to another function, such as <a href="_win32_PeekMessage_cpp">PeekMessage</a>.


### -field COWAIT_DISPATCH_CALLS

Dispatch calls from <a href="https://msdn.microsoft.com/3eeecd34-aa94-4a48-8b41-167a71b52860">CoWaitForMultipleHandles</a> in an ASTA. Default is no call dispatch. This value has no meaning in other apartment types and is ignored.


### -field COWAIT_DISPATCH_WINDOW_MESSAGES

Enables dispatch of window messages from <a href="https://msdn.microsoft.com/3eeecd34-aa94-4a48-8b41-167a71b52860">CoWaitForMultipleHandles</a> in an ASTA or STA. Default in ASTA is no window messages dispatched, default in STA is only a small set of special-cased messages dispatched. The value has no meaning in MTA and is ignored.


## -see-also




<a href="https://msdn.microsoft.com/3eeecd34-aa94-4a48-8b41-167a71b52860">CoWaitForMultipleHandles</a>



<a href="https://msdn.microsoft.com/1abed0be-b4e3-41f4-af6c-e327ce934b59">ISynchronize::Wait</a>



<a href="https://msdn.microsoft.com/2754b744-3ba8-4e60-9847-1d0eb3c24180">ISynchronizeContainer::WaitMultiple</a>
 

 

