---
UID: NF:winbase.ConvertThreadToFiberEx
title: ConvertThreadToFiberEx function (winbase.h)
description: Converts the current thread into a fiber. You must convert a thread into a fiber before you can schedule other fibers. (ConvertThreadToFiberEx)
helpviewer_keywords: ["ConvertThreadToFiberEx","ConvertThreadToFiberEx function","_win32_convertthreadtofiberex","base.convertthreadtofiberex","winbase/ConvertThreadToFiberEx"]
old-location: base\convertthreadtofiberex.htm
tech.root: backup
ms.assetid: cb0473f8-bc49-44c9-a8b7-6d5b55aa37a5
ms.date: 12/05/2018
ms.keywords: ConvertThreadToFiberEx, ConvertThreadToFiberEx function, _win32_convertthreadtofiberex, base.convertthreadtofiberex, winbase/ConvertThreadToFiberEx
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
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
 - ConvertThreadToFiberEx
 - winbase/ConvertThreadToFiberEx
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
 - ConvertThreadToFiberEx
---

# ConvertThreadToFiberEx function


## -description

Converts the current thread into a fiber. You must convert a thread into a fiber before you can schedule other fibers.

## -parameters

### -param lpParameter [in, optional]

A  pointer to a variable that is passed to the fiber. The fiber can retrieve this data by using the 
<a href="/windows/desktop/api/winnt/nf-winnt-getfiberdata">GetFiberData</a> macro.

### -param dwFlags [in]

If this parameter is zero, the floating-point state on x86 systems is not switched and data can be corrupted if a fiber uses floating-point arithmetic. If this parameter is FIBER_FLAG_FLOAT_SWITCH, the floating-point state is switched for the fiber.

## -returns

If the function succeeds, the return value is the address of the fiber.

If the function fails, the return value is NULL. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Only fibers can execute other fibers. If a thread needs to execute a fiber, it must call 
<a href="/windows/desktop/api/winbase/nf-winbase-convertthreadtofiber">ConvertTheadToFiber</a> or 
<b>ConvertThreadToFiberEx</b> to create an area in which to save fiber state information. The thread is now the current fiber. The state information for this fiber includes the fiber data specified by <i>lpParameter</i>.

To compile an application that uses this function, define _WIN32_WINNT as 0x0400 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-convertfibertothread">ConvertFiberToThread</a>



<a href="/windows/desktop/ProcThread/fibers">Fibers</a>



<a href="/windows/desktop/api/winnt/nf-winnt-getfiberdata">GetFiberData</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>
