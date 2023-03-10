---
UID: NF:synchapi.CancelWaitableTimer
title: CancelWaitableTimer function (synchapi.h)
description: Sets the specified waitable timer to the inactive state.
helpviewer_keywords: ["CancelWaitableTimer","CancelWaitableTimer function","_win32_cancelwaitabletimer","base.cancelwaitabletimer","synchapi/CancelWaitableTimer","winbase/CancelWaitableTimer"]
old-location: base\cancelwaitabletimer.htm
tech.root: base
ms.assetid: 614a237b-71b3-4091-975d-4c0b3cd6ec69
ms.date: 12/05/2018
ms.keywords: CancelWaitableTimer, CancelWaitableTimer function, _win32_cancelwaitabletimer, base.cancelwaitabletimer, synchapi/CancelWaitableTimer, winbase/CancelWaitableTimer
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
 - CancelWaitableTimer
 - synchapi/CancelWaitableTimer
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
 - CancelWaitableTimer
---

# CancelWaitableTimer function


## -description

Sets the specified waitable timer to the inactive state.

## -parameters

### -param hTimer [in]

A handle to the timer object. The 
[CreateWaitableTimer](./nf-synchapi-createwaitabletimerw.md) or 
[OpenWaitableTimer](./nf-synchapi-openwaitabletimerw.md) function returns this handle. The handle must have the <b>TIMER_MODIFY_STATE</b> access right. For more information, see 
<a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Synchronization Object Security and Access Rights</a>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>CancelWaitableTimer</b> function does not change the signaled state of the timer. It stops the timer before it can be set to the signaled state and cancels outstanding APCs. Therefore, threads performing a wait operation on the timer remain waiting until they time out or the timer is reactivated and its state is set to signaled. If the timer is already in the signaled state, it remains in that state.

To reactivate the timer, call the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-setwaitabletimer">SetWaitableTimer</a> function.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0400 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

[CreateWaitableTimer](./nf-synchapi-createwaitabletimerw.md)



[OpenWaitableTimer](./nf-synchapi-openwaitabletimerw.md)



<a href="/windows/desktop/api/synchapi/nf-synchapi-setwaitabletimer">SetWaitableTimer</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>



<a href="/windows/desktop/Sync/waitable-timer-objects">Waitable Timer Objects</a>