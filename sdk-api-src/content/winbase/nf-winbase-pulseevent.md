---
UID: NF:winbase.PulseEvent
title: PulseEvent function (winbase.h)
description: Sets the specified event object to the signaled state and then resets it to the nonsignaled state after releasing the appropriate number of waiting threads.
helpviewer_keywords: ["PulseEvent","PulseEvent function","_win32_pulseevent","base.pulseevent","winbase/PulseEvent"]
old-location: base\pulseevent.htm
tech.root: backup
ms.assetid: b3cfe15a-1a0e-4c29-8840-032e56404400
ms.date: 12/05/2018
ms.keywords: PulseEvent, PulseEvent function, _win32_pulseevent, base.pulseevent, winbase/PulseEvent
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - PulseEvent
 - winbase/PulseEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-misc-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - PulseEvent
---

# PulseEvent function


## -description

Sets the specified event object to the signaled state and then resets it to the nonsignaled state after releasing the appropriate number of waiting threads.
<div class="alert"><b>Note</b>  This function is unreliable and should not be used. It exists mainly for backward compatibility. For more information, see Remarks.</div><div> </div>

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

A thread waiting on a synchronization object can be momentarily removed from the wait state  by a kernel-mode APC, and then returned to the wait state after the APC is complete.  If the call to  <b>PulseEvent</b> occurs during the time when the thread has been   removed from the wait state, the thread will not be released  because  <b>PulseEvent</b> releases only those threads that are waiting at the moment it is called.  Therefore,  <b>PulseEvent</b> is unreliable and should  not be  used by new applications.
Instead, use <a href="/windows/desktop/Sync/condition-variables">condition variables</a>.

For a manual-reset event object, all waiting threads that can be released immediately are released. The function then resets the event object's state to nonsignaled and returns.

For an auto-reset event object, the function resets the state to nonsignaled and returns after releasing a single waiting thread, even if multiple threads are waiting.

If no threads are waiting, or if no thread can be released immediately, 
<b>PulseEvent</b> simply sets the event object's state to nonsignaled and returns.

Note that for a thread using the multiple-object 
<a href="/windows/desktop/Sync/wait-functions">wait functions</a> to wait for all specified objects to be signaled, 
<b>PulseEvent</b> can set the event object's state to signaled and reset it to nonsignaled without causing the wait function to return. This happens if not all of the specified objects are simultaneously signaled.

Use extreme caution when using  [SignalObjectAndWait](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait)  and <b>PulseEvent</b> with Windows 7, since using these APIs among multiple threads can cause an application to deadlock. Threads that are signaled by <b>SignalObjectAndWait</b>  call <b>PulseEvent</b> to signal the waiting object of the <b>SignalObjectAndWait</b> call. In some circumstances, the caller of <b>SignalObjectAndWait</b> can't receive signal state of the waiting object in time, causing a deadlock.

## -see-also

<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a>



<a href="/windows/desktop/Sync/event-objects">Event Objects</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-openeventa">OpenEvent</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-resetevent">ResetEvent</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-setevent">SetEvent</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>
