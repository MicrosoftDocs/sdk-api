---
UID: NF:winbase.CreateFiber
title: CreateFiber function (winbase.h)
description: Allocates a fiber object, assigns it a stack, and sets up execution to begin at the specified start address, typically the fiber function. This function does not schedule the fiber. (CreateFiber)
helpviewer_keywords: ["CreateFiber","CreateFiber function","_win32_createfiber","base.createfiber","winbase/CreateFiber"]
old-location: base\createfiber.htm
tech.root: backup
ms.assetid: 3e44776b-7ef2-43fb-a2ae-e8ab7e20644b
ms.date: 12/05/2018
ms.keywords: CreateFiber, CreateFiber function, _win32_createfiber, base.createfiber, winbase/CreateFiber
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
 - CreateFiber
 - winbase/CreateFiber
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
 - CreateFiber
---

# CreateFiber function


## -description

Allocates a fiber object, assigns it a stack, and sets up execution to begin at the specified start address, typically the fiber function. This function does not schedule the fiber.

To specify both a commit and reserve stack size, use the 
<a href="/windows/desktop/api/winbase/nf-winbase-createfiberex">CreateFiberEx</a> function.

## -parameters

### -param dwStackSize [in]

The initial committed size of the stack, in bytes. If this parameter is zero, the new fiber uses the default commit stack size for the executable. For more information, see <a href="/windows/desktop/ProcThread/thread-stack-size">Thread Stack Size</a>.

### -param lpStartAddress [in]

A pointer to the application-defined function to be executed by the fiber and represents the starting address of the fiber. Execution of the newly created fiber does not begin until another fiber calls the 
<a href="/windows/desktop/api/winbase/nf-winbase-switchtofiber">SwitchToFiber</a> function with this address. For more information of the fiber callback function, see 
<a href="/windows/desktop/api/winbase/nc-winbase-pfiber_start_routine">FiberProc</a>.

### -param lpParameter [in, optional]

A pointer to a variable that is passed to the fiber. The fiber can retrieve this data by using the 
<a href="/windows/desktop/api/winnt/nf-winnt-getfiberdata">GetFiberData</a> macro.

## -returns

If the function succeeds, the return value is the address of the fiber.

If the function fails, the return value is NULL. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The number of fibers a process can create is limited by the available virtual memory. For example, if you create each fiber with 1 megabyte of reserved stack space, you can create at most 2028 fibers. If you reduce the default stack size by using the STACKSIZE statement in the module definition (.def) file or 
by using <a href="/windows/desktop/api/winbase/nf-winbase-createfiberex">CreateFiberEx</a>, you can create more fibers. However, your application will have better performance if you use an alternate strategy for processing requests instead of creating such a large number of fibers.

Before a thread can schedule a fiber using the 
<a href="/windows/desktop/api/winbase/nf-winbase-switchtofiber">SwitchToFiber</a> function, it must call the 
<a href="/windows/desktop/api/winbase/nf-winbase-convertthreadtofiber">ConvertThreadToFiber</a> function so there is a fiber associated with the thread.

To compile an application that uses this function, define _WIN32_WINNT as 0x0400 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.


#### Examples

For an example, see <a href="/windows/desktop/ProcThread/using-fibers">Using Fibers</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-convertthreadtofiber">ConvertThreadToFiber</a>



<a href="/windows/desktop/api/winbase/nf-winbase-createfiberex">CreateFiberEx</a>



<a href="/windows/desktop/api/winbase/nc-winbase-pfiber_start_routine">FiberProc</a>



<a href="/windows/desktop/ProcThread/fibers">Fibers</a>



<a href="/windows/desktop/api/winnt/nf-winnt-getfiberdata">GetFiberData</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-switchtofiber">SwitchToFiber</a>
