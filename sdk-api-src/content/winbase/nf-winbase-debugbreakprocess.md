---
UID: NF:winbase.DebugBreakProcess
title: DebugBreakProcess function (winbase.h)
description: Causes a breakpoint exception to occur in the specified process. This allows the calling thread to signal the debugger to handle the exception.
helpviewer_keywords: ["DebugBreakProcess","DebugBreakProcess function","_win32_debugbreakprocess","base.debugbreakprocess","winbase/DebugBreakProcess"]
old-location: base\debugbreakprocess.htm
tech.root: Debug
ms.assetid: db90d46b-fdbc-49c9-ac99-6b1db1db708c
ms.date: 12/05/2018
ms.keywords: DebugBreakProcess, DebugBreakProcess function, _win32_debugbreakprocess, base.debugbreakprocess, winbase/DebugBreakProcess
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
 - DebugBreakProcess
 - winbase/DebugBreakProcess
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - DebugBreakProcess
---

# DebugBreakProcess function


## -description

Causes a breakpoint exception to occur in the specified process. This allows the calling thread to signal the debugger to handle the exception.

## -parameters

### -param Process [in]

A handle to the process.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the process is not being debugged, the function uses the search logic of a standard exception handler. In most cases, this causes the process to terminate because of an unhandled breakpoint exception.

## -see-also

<a href="/windows/desktop/Debug/communicating-with-the-debugger">Communicating with the Debugger</a>



<a href="/windows/desktop/api/debugapi/nf-debugapi-debugbreak">DebugBreak</a>



<a href="/windows/desktop/Debug/debugging-functions">Debugging Functions</a>