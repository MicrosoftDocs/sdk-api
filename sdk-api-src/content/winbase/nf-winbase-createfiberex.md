---
UID: NF:winbase.CreateFiberEx
title: CreateFiberEx function (winbase.h)
description: Allocates a fiber object, assigns it a stack, and sets up execution to begin at the specified start address, typically the fiber function. This function does not schedule the fiber. (CreateFiberEx)
helpviewer_keywords: ["CreateFiberEx","CreateFiberEx function","_win32_createfiberex","base.createfiberex","winbase/CreateFiberEx"]
old-location: base\createfiberex.htm
tech.root: backup
ms.assetid: eb27cfcf-6086-47df-a5b4-93c51a5e1577
ms.date: 12/05/2018
ms.keywords: CreateFiberEx, CreateFiberEx function, _win32_createfiberex, base.createfiberex, winbase/CreateFiberEx
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
 - CreateFiberEx
 - winbase/CreateFiberEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-fibers-l2-1-1.dll
 - kernel32legacy.dll
 - KernelBase.dll
api_name:
 - CreateFiberEx
---

# CreateFiberEx function


## -description

Allocates a fiber object, assigns it a stack, and sets up execution to begin at the specified start address, typically the fiber function. This function does not schedule the fiber.

## -parameters

### -param dwStackCommitSize [in]

The initial commit size of the stack, in bytes. If this parameter is zero, the new fiber uses the default commit stack size for the executable. For more information, see <a href="/windows/desktop/ProcThread/thread-stack-size">Thread Stack Size</a>.

### -param dwStackReserveSize [in]

The initial reserve size of the stack, in bytes. If this parameter is zero, the new fiber uses the default reserved stack size for the executable. For more information, see <a href="/windows/desktop/ProcThread/thread-stack-size">Thread Stack Size</a>.

### -param dwFlags [in]

If this parameter is zero, the floating-point state on x86 systems is not switched and data can be corrupted if a fiber uses floating-point arithmetic. If this parameter is <b>FIBER_FLAG_FLOAT_SWITCH</b>, the floating-point state is switched for the fiber.

<b>Windows XP:  </b>The <b>FIBER_FLAG_FLOAT_SWITCH</b> flag is not supported.

### -param lpStartAddress [in]

A pointer to the application-defined function to be executed by the fiber and represents the starting address of the fiber. Execution of the newly created fiber does not begin until another fiber calls the 
<a href="/windows/desktop/api/winbase/nf-winbase-switchtofiber">SwitchToFiber</a> function with this address. For more information on the fiber callback function, see 
<a href="/windows/desktop/api/winbase/nc-winbase-pfiber_start_routine">FiberProc</a>.

### -param lpParameter [in, optional]

A pointer to a variable that is passed to the fiber. The fiber can retrieve this data by using the 
<a href="/windows/desktop/api/winnt/nf-winnt-getfiberdata">GetFiberData</a> macro.

## -returns

If the function succeeds, the return value is the address of the fiber.

If the function fails, the return value is NULL. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The number of fibers a process can create is limited by the available virtual memory. By default, every fiber has 1 megabyte of reserved stack space. Therefore, you can create at most 2028 fibers. If you reduce the default stack size, you can create more fibers. However, your application will have better performance if you use an alternate strategy for processing requests.

Before a thread can schedule a fiber using the 
<a href="/windows/desktop/api/winbase/nf-winbase-switchtofiber">SwitchToFiber</a> function, it must call the 
<a href="/windows/desktop/api/winbase/nf-winbase-convertthreadtofiber">ConvertThreadToFiber</a> function so there is a fiber associated with the thread.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0400 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-convertthreadtofiber">ConvertThreadToFiber</a>



<a href="/windows/desktop/api/winbase/nc-winbase-pfiber_start_routine">FiberProc</a>



<a href="/windows/desktop/ProcThread/fibers">Fibers</a>



<a href="/windows/desktop/api/winnt/nf-winnt-getfiberdata">GetFiberData</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-switchtofiber">SwitchToFiber</a>
