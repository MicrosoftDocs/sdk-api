---
UID: NF:synchapi.SetEvent
title: SetEvent function (synchapi.h)
description: Sets the specified event object to the signaled state.
helpviewer_keywords: ["SetEvent","SetEvent function","_win32_setevent","base.setevent","synchapi/SetEvent","winbase/SetEvent"]
old-location: base\setevent.htm
tech.root: base
ms.assetid: b474eef1-5df9-4729-b940-0c5f201c5f31
ms.date: 12/05/2018
ms.keywords: SetEvent, SetEvent function, _win32_setevent, base.setevent, synchapi/SetEvent, winbase/SetEvent
req.header: synchapi.h
req.include-header: Windows.h on Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetEvent
 - synchapi/SetEvent
dev_langs:
 - c++
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
---

# SetEvent function


## -description

Sets the specified event object to the signaled state.

## -parameters

### -param hEvent [in]

A handle to the event object. The 
<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a> or 
<a href="/windows/desktop/api/synchapi/nf-synchapi-openeventa">OpenEvent</a> function returns this handle. 




The handle must have the EVENT_MODIFY_STATE access right. For more information, see 
<a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Synchronization Object Security and Access Rights</a>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The state of a **manual-reset** event object remains signaled until it is set explicitly to the nonsignaled state by the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-resetevent">ResetEvent</a> function. Any number of waiting threads, or threads that subsequently begin wait operations for the specified event object by calling one of the 
<a href="/windows/desktop/Sync/wait-functions">wait functions</a>, can be released while the object's state is signaled.

In contrast, the state of an **auto-reset** event object remains signaled until a single waiting thread is released, at which time the system automatically sets the state to nonsignaled. If no threads are waiting, the event object's state remains signaled.

Setting an event that is already set has no effect.

Windows Store apps can respond to named events and semaphores as described in <a href="/previous-versions/windows/apps/jj248674(v=win.10)">How to respond to named events and semaphores</a>.


#### Examples

For an example that uses 
<b>SetEvent</b>, see 
<a href="/windows/desktop/Sync/using-event-objects">Using Event Objects</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a>



<a href="/windows/desktop/Sync/event-objects">Event Objects</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-openeventa">OpenEvent</a>



<a href="/windows/desktop/api/winbase/nf-winbase-pulseevent">PulseEvent</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-resetevent">ResetEvent</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>
