---
UID: NF:winbase.SwitchToFiber
title: SwitchToFiber function (winbase.h)
description: Schedules a fiber. The function must be called on a fiber.
helpviewer_keywords: ["SwitchToFiber","SwitchToFiber function","_win32_switchtofiber","base.switchtofiber","winbase/SwitchToFiber"]
old-location: base\switchtofiber.htm
tech.root: backup
ms.assetid: 020a8c97-848d-4b33-9cfb-77e5bff644fd
ms.date: 12/05/2018
ms.keywords: SwitchToFiber, SwitchToFiber function, _win32_switchtofiber, base.switchtofiber, winbase/SwitchToFiber
req.header: winbase.h
req.include-header: Windows.h
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
 - SwitchToFiber
 - winbase/SwitchToFiber
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-fibers-l2-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-fibers-l2-1-1.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - KernelBase.dll
api_name:
 - SwitchToFiber
---

# SwitchToFiber function


## -description

Schedules a fiber. The function must be called on a fiber.

## -parameters

### -param lpFiber [in]

The address of the fiber to be scheduled.

## -remarks

You create fibers with the 
<a href="/windows/desktop/api/winbase/nf-winbase-createfiber">CreateFiber</a> function. Before you can schedule fibers associated with a thread, you must call 
<a href="/windows/desktop/api/winbase/nf-winbase-convertthreadtofiber">ConvertThreadToFiber</a> to set up an area in which to save the fiber state information. The thread is now the currently executing fiber.

The 
<b>SwitchToFiber</b> function saves the state information of the current fiber and restores the state of the specified fiber. You can call 
<b>SwitchToFiber</b> with the address of a fiber created by a different thread. To do this, you must have the address returned to the other thread when it called 
<a href="/windows/desktop/api/winbase/nf-winbase-createfiber">CreateFiber</a> and you must use proper synchronization.

Avoid making the following call:


``` syntax
SwitchToFiber( GetCurrentFiber() );
```

This call can cause unpredictable problems.

To compile an application that uses this function, define _WIN32_WINNT as 0x0400 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-convertthreadtofiber">ConvertThreadToFiber</a>



<a href="/windows/desktop/api/winbase/nf-winbase-createfiber">CreateFiber</a>



<a href="/windows/desktop/ProcThread/fibers">Fibers</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>
