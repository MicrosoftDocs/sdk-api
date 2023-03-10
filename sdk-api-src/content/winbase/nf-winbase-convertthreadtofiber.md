---
UID: NF:winbase.ConvertThreadToFiber
title: ConvertThreadToFiber function (winbase.h)
description: Converts the current thread into a fiber. You must convert a thread into a fiber before you can schedule other fibers. (ConvertThreadToFiber)
helpviewer_keywords: ["ConvertThreadToFiber","ConvertThreadToFiber function","_win32_convertthreadtofiber","base.convertthreadtofiber","winbase/ConvertThreadToFiber"]
old-location: base\convertthreadtofiber.htm
tech.root: backup
ms.assetid: 31954a7e-b9a3-4d60-b43a-54fe0047f380
ms.date: 12/05/2018
ms.keywords: ConvertThreadToFiber, ConvertThreadToFiber function, _win32_convertthreadtofiber, base.convertthreadtofiber, winbase/ConvertThreadToFiber
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
 - ConvertThreadToFiber
 - winbase/ConvertThreadToFiber
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
 - ConvertThreadToFiber
---

# ConvertThreadToFiber function


## -description

Converts the current thread into a fiber. You must convert a thread into a fiber before you can schedule other fibers.

## -parameters

### -param lpParameter [in, optional]

A pointer to a variable that is passed to the fiber. The fiber can retrieve this data by using the 
<a href="/windows/desktop/api/winnt/nf-winnt-getfiberdata">GetFiberData</a> macro.

## -returns

If the function succeeds, the return value is the address of the fiber.

If the function fails, the return value is NULL. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Only fibers can execute other fibers. If a thread needs to execute a fiber, it must call 
<b>ConvertThreadToFiber</b> or 
<a href="/windows/desktop/api/winbase/nf-winbase-convertthreadtofiberex">ConvertThreadToFiberEx</a> to create an area in which to save fiber state information. The thread is now the current fiber. The state information for this fiber includes the fiber data specified by <i>lpParameter</i>.

To compile an application that uses this function, define _WIN32_WINNT as 0x0400 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.


#### Examples

For an example, see <a href="/windows/desktop/ProcThread/using-fibers">Using Fibers</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-convertfibertothread">ConvertFiberToThread</a>



<a href="/windows/desktop/api/winbase/nf-winbase-convertthreadtofiberex">ConvertThreadToFiberEx</a>



<a href="/windows/desktop/ProcThread/fibers">Fibers</a>



<a href="/windows/desktop/api/winnt/nf-winnt-getfiberdata">GetFiberData</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>
