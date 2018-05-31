---
UID: NE:combaseapi.tagCOWAIT_FLAGS
title: tagCOWAIT_FLAGS
author: windows-sdk-content
description: Specifies the behavior of the CoWaitForMultipleHandles function.
old-location: com\cowait_flags.htm
old-project: com
ms.assetid: e6f8300c-f74b-4383-8ee5-519a0ed0b358
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: COWAIT_ALERTABLE, COWAIT_DISPATCH_CALLS, COWAIT_DISPATCH_WINDOW_MESSAGES, COWAIT_FLAGS, COWAIT_FLAGS enumeration [COM], COWAIT_INPUTAVAILABLE, COWAIT_WAITALL, _com_COWAIT_FLAGS, com.cowait_flags, combaseapi/COWAIT_ALERTABLE, combaseapi/COWAIT_DISPATCH_CALLS, combaseapi/COWAIT_DISPATCH_WINDOW_MESSAGES, combaseapi/COWAIT_FLAGS, combaseapi/COWAIT_INPUTAVAILABLE, combaseapi/COWAIT_WAITALL, tagCOWAIT_FLAGS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComAdmin.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: COWAIT_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	combaseapi.h
api_name:
-	COWAIT_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

