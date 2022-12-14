---
UID: NF:winbase.ConvertFiberToThread
title: ConvertFiberToThread function (winbase.h)
description: Converts the current fiber into a thread.
helpviewer_keywords: ["ConvertFiberToThread","ConvertFiberToThread function","_win32_convertfibertothread","base.convertfibertothread","winbase/ConvertFiberToThread"]
old-location: base\convertfibertothread.htm
tech.root: backup
ms.assetid: 194c5289-0d25-4ce1-9c32-9e87b12db825
ms.date: 12/05/2018
ms.keywords: ConvertFiberToThread, ConvertFiberToThread function, _win32_convertfibertothread, base.convertfibertothread, winbase/ConvertFiberToThread
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
 - ConvertFiberToThread
 - winbase/ConvertFiberToThread
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
 - ConvertFiberToThread
---

# ConvertFiberToThread function


## -description

Converts the current fiber into a thread.



## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The function releases the resources allocated by the 
<a href="/windows/desktop/api/winbase/nf-winbase-convertthreadtofiber">ConvertThreadToFiber</a> function. After calling this function, you cannot call any of the fiber functions from the thread.

To compile an application that uses this function, define \_WIN32_WINNT as \_WIN32_WINNT_WS03 (0x0502) or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-convertthreadtofiber">ConvertThreadToFiber</a>



<a href="/windows/desktop/ProcThread/fibers">Fibers</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>
