---
UID: NF:synchapi.SetEvent
title: SetEvent function
author: windows-sdk-content
description: Sets the specified event object to the signaled state.
old-location: base\setevent.htm
tech.root: sync
ms.assetid: b474eef1-5df9-4729-b940-0c5f201c5f31
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: SetEvent, SetEvent function, _win32_setevent, base.setevent, synchapi/SetEvent, winbase/SetEvent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: synchapi.h
req.include-header: Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - API-MS-Win-Core-Synch-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Synch-l1-2-0.dll
 - API-MS-Win-Core-Synch-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - SetEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetEvent function


## -description


Sets the specified event object to the signaled state.


## -parameters




### -param hEvent [in]

A handle to the event object. The 
<a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a> or 
<a href="https://msdn.microsoft.com/46741024-ace3-44d6-b8a6-5621ad121a1a">OpenEvent</a> function returns this handle. 




The handle must have the EVENT_MODIFY_STATE access right. For more information, see 
<a href="https://msdn.microsoft.com/92478298-617c-4672-a1cc-9a8e9af40327">Synchronization Object Security and Access Rights</a>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The state of a manual-reset event object remains signaled until it is set explicitly to the nonsignaled state by the 
<a href="https://msdn.microsoft.com/bba7caab-d1ed-4261-aeca-49f847458f4c">ResetEvent</a> function. Any number of waiting threads, or threads that subsequently begin wait operations for the specified event object by calling one of the 
<a href="https://msdn.microsoft.com/9c66c71d-fdfd-42ae-895c-2fc842b5bc7a">wait functions</a>, can be released while the object's state is signaled.

The state of an auto-reset event object remains signaled until a single waiting thread is released, at which time the system automatically sets the state to nonsignaled. If no threads are waiting, the event object's state remains signaled.

Setting an event that is already set has no effect.

Windows Store apps can respond to named events and semaphores as described in <a href="https://msdn.microsoft.com/F59B59EE-D21D-4C93-9C40-B0097A8CA351">How to respond to named events and semaphores</a>.


#### Examples

For an example that uses 
<b>SetEvent</b>, see 
<a href="https://msdn.microsoft.com/f3f455bb-7563-4920-a728-f75fa5854dc9">Using Event Objects</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a>



<a href="https://msdn.microsoft.com/63dc2991-e070-4981-9e2d-90b4fdaaee7a">Event Objects</a>



<a href="https://msdn.microsoft.com/46741024-ace3-44d6-b8a6-5621ad121a1a">OpenEvent</a>



<a href="https://msdn.microsoft.com/b3cfe15a-1a0e-4c29-8840-032e56404400">PulseEvent</a>



<a href="https://msdn.microsoft.com/bba7caab-d1ed-4261-aeca-49f847458f4c">ResetEvent</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

