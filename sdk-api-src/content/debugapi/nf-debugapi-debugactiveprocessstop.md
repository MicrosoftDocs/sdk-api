---
UID: NF:debugapi.DebugActiveProcessStop
title: DebugActiveProcessStop function (debugapi.h)
description: Stops the debugger from debugging the specified process.
helpviewer_keywords: ["DebugActiveProcessStop","DebugActiveProcessStop function","_win32_debugactiveprocessstop","base.debugactiveprocessstop","debugapi/DebugActiveProcessStop"]
old-location: base\debugactiveprocessstop.htm
tech.root: Debug
ms.assetid: 29d1a6d1-0c10-43c1-bef1-b063f07b16a4
ms.date: 12/05/2018
ms.keywords: DebugActiveProcessStop, DebugActiveProcessStop function, _win32_debugactiveprocessstop, base.debugactiveprocessstop, debugapi/DebugActiveProcessStop
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
 - DebugActiveProcessStop
 - debugapi/DebugActiveProcessStop
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-debug-l1-1-1.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Debug-L1-1-2.dll
api_name:
 - DebugActiveProcessStop
---

# DebugActiveProcessStop function


## -description

Stops the debugger from debugging the specified process.

## -parameters

### -param dwProcessId [in]

The identifier of the process to stop debugging.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/debugapi/nf-debugapi-debugactiveprocess">DebugActiveProcess</a>



<a href="/windows/desktop/Debug/debugging-functions">Debugging Functions</a>



<a href="/windows/desktop/Debug/debugging-a-running-process">Debugging a Running Process</a>



<a href="/windows/desktop/Debug/process-functions-for-debugging">Process Functions for Debugging</a>