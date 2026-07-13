---
UID: NF:debugapi.DebugBreak
title: DebugBreak function (debugapi.h)
description: Causes a breakpoint exception to occur in the current process. This allows the calling thread to signal the debugger to handle the exception.
helpviewer_keywords: ["DebugBreak","DebugBreak function","_win32_debugbreak","base.debugbreak","debugapi/DebugBreak"]
old-location: base\debugbreak.htm
tech.root: Debug
ms.assetid: 1ca9d2d1-eed4-4982-8964-64b44e8be256
ms.date: 12/05/2018
ms.keywords: DebugBreak, DebugBreak function, _win32_debugbreak, base.debugbreak, debugapi/DebugBreak
req.header: debugapi.h
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
 - DebugBreak
 - debugapi/DebugBreak
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-debug-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-debug-l1-1-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Debug-L1-1-2.dll
api_name:
 - DebugBreak
---

# DebugBreak function


## -description

Causes a breakpoint exception to occur in the current process. This allows the calling thread to signal the debugger to handle the exception.

To cause a breakpoint exception in another process, use the 
<a href="/windows/desktop/api/winbase/nf-winbase-debugbreakprocess">DebugBreakProcess</a> function.



## -remarks

If the process is not being debugged, the function uses the search logic of a standard exception handler. In most cases, this causes the calling process to terminate because of an unhandled breakpoint exception.


#### Examples

For an example, see 
<a href="/windows/desktop/Debug/using-an-exception-handler">Using an Exception Handler</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/Debug/communicating-with-the-debugger">Communicating with the Debugger</a>



<a href="/windows/desktop/api/debugapi/nf-debugapi-debugactiveprocess">DebugActiveProcess</a>



<a href="/windows/desktop/api/winbase/nf-winbase-debugbreakprocess">DebugBreakProcess</a>



<a href="/windows/desktop/Debug/debugging-functions">Debugging Functions</a>
