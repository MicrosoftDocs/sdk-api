---
UID: NF:debugapi.WaitForDebugEventEx
title: WaitForDebugEventEx function (debugapi.h)
description: Waits for a debugging event to occur in a process being debugged. (WaitForDebugEventEx)
helpviewer_keywords: ["WaitForDebugEventEx","WaitForDebugEventEx function","base.waitfordebugeventex","debugapi/WaitForDebugEventEx"]
old-location: base\waitfordebugeventex.htm
tech.root: Debug
ms.assetid: 2C79C4BE-9787-415E-AB82-1E33AB92D32F
ms.date: 12/05/2018
ms.keywords: WaitForDebugEventEx, WaitForDebugEventEx function, base.waitfordebugeventex, debugapi/WaitForDebugEventEx
req.header: debugapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - WaitForDebugEventEx
 - debugapi/WaitForDebugEventEx
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
 - WaitForDebugEventEx
---

# WaitForDebugEventEx function


## -description

Waits for a debugging event to occur in a process being debugged.
<div class="alert"><b>Important</b>  In the past, the operating system did not output Unicode strings via <b>OutputDebugStringW</b> and instead only output ASCII strings. To force <b>OutputDebugStringW</b> to correctly output Unicode strings, debuggers are required to call <b>WaitForDebugEventEx</b> to opt into the new behavior. On calling <b>WaitForDebugEventEx</b>, the operating system will know that the debugger supports Unicode and is specifically opting into receiving Unicode strings. </div><div> </div>

## -parameters

### -param lpDebugEvent [out]

A pointer to a 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-debug_event">DEBUG_EVENT</a> structure that receives information about the debugging event.

### -param dwMilliseconds [in]

The number of milliseconds to wait for a debugging event. If this parameter is zero, the function tests for a debugging event and returns immediately. If the parameter is INFINITE, the function does not return until a debugging event has occurred.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Only the thread that created the process being debugged can call 
<b>WaitForDebugEventEx</b>.

When a CREATE_PROCESS_DEBUG_EVENT occurs, the debugger application receives a handle to the image file of the process being debugged, a handle to the process being debugged, and a handle to the initial thread of the process being debugged in the 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-debug_event">DEBUG_EVENT</a> structure. The members these handles are returned in are <b>u.CreateProcessInfo.hFile</b> (image file), <b>u.CreateProcessInfo.hProcess</b> (process), and <b>u.CreateProcessInfo.hThread</b> (initial thread). If the system previously reported an EXIT_PROCESS_DEBUG_EVENT debugging event, the system closes the handles to the process and thread when the debugger calls the 
<a href="/windows/desktop/api/debugapi/nf-debugapi-continuedebugevent">ContinueDebugEvent</a> function. The debugger should close the handle to the image file by calling the 
<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function.

Similarly, when a CREATE_THREAD_DEBUG_EVENT occurs, the debugger application receives a handle to the thread whose creation caused the debugging event in the <b>u.CreateThread.hThread</b> member of the 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-debug_event">DEBUG_EVENT</a> structure. If the system previously reported an EXIT_THREAD_DEBUG_EVENT debugging event, the system closes the handles to the thread when the debugger calls the 
<a href="/windows/desktop/api/debugapi/nf-debugapi-continuedebugevent">ContinueDebugEvent</a> function.

When a LOAD_DLL_DEBUG_EVENT occurs, the debugger application receives a handle to the loaded DLL in the <b>u.LoadDll.hFile</b> member of the 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-debug_event">DEBUG_EVENT</a> structure. This handle should be closed by the debugger application by calling the 
<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function.

<div class="alert"><b>Warning</b>  Do not queue an 
<a href="/windows/desktop/Sync/asynchronous-procedure-calls">asynchronous procedure call</a> (APC) to a thread that calls 
<b>WaitForDebugEventEx</b>.</div>
<div> </div>

#### Examples

For an example, see 
<a href="/windows/desktop/Debug/writing-the-debugger-s-main-loop">Writing the Debugger's Main Loop</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/debugapi/nf-debugapi-continuedebugevent">ContinueDebugEvent</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-debug_event">DEBUG_EVENT</a>



<a href="/windows/desktop/api/debugapi/nf-debugapi-debugactiveprocess">DebugActiveProcess</a>



<a href="/windows/desktop/api/debugapi/nf-debugapi-debugbreak">DebugBreak</a>



<a href="/windows/desktop/Debug/debugging-events">Debugging Events</a>



<a href="/windows/desktop/Debug/debugging-functions">Debugging Functions</a>



<a href="/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw">OutputDebugString</a>
