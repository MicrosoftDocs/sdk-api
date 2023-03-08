---
UID: NF:synchapi.ResetEvent
title: ResetEvent function (synchapi.h)
description: Sets the specified event object to the nonsignaled state.
helpviewer_keywords: ["ResetEvent","ResetEvent function","_win32_resetevent","base.resetevent","synchapi/ResetEvent","winbase/ResetEvent"]
old-location: base\resetevent.htm
tech.root: base
ms.assetid: bba7caab-d1ed-4261-aeca-49f847458f4c
ms.date: 12/05/2018
ms.keywords: ResetEvent, ResetEvent function, _win32_resetevent, base.resetevent, synchapi/ResetEvent, winbase/ResetEvent
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
 - ResetEvent
 - synchapi/ResetEvent
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
 - ResetEvent
---

# ResetEvent function


## -description

Sets the specified event object to the nonsignaled state.

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

The state of an event object remains nonsignaled until it is explicitly set to signaled by the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-setevent">SetEvent</a> or 
<a href="/windows/desktop/api/winbase/nf-winbase-pulseevent">PulseEvent</a> function. This nonsignaled state blocks the execution of any threads that have specified the event object in a call to one of the 
<a href="/windows/desktop/Sync/wait-functions">wait functions</a>.

The 
<b>ResetEvent</b> function is used primarily for manual-reset event objects, which must be set explicitly to the nonsignaled state. Auto-reset event objects automatically change from signaled to nonsignaled after a single waiting thread is released.

Resetting an event that is already reset has no effect.

## -see-also

<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a>



<a href="/windows/desktop/Sync/event-objects">Event Objects</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-openeventa">OpenEvent</a>



<a href="/windows/desktop/api/winbase/nf-winbase-pulseevent">PulseEvent</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-setevent">SetEvent</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>