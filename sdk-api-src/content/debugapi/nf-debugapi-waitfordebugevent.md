---
UID: NF:debugapi.WaitForDebugEvent
title: WaitForDebugEvent function
author: windows-sdk-content
description: Waits for a debugging event to occur in a process being debugged.
old-location: base\waitfordebugevent.htm
tech.root: Debug
ms.assetid: 0d81a4ac-dd66-4648-9f3f-1f54aca84243
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WaitForDebugEvent, WaitForDebugEvent function, _win32_waitfordebugevent, base.waitfordebugevent, debugapi/WaitForDebugEvent
ms.topic: function
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
 - WaitForDebugEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WaitForDebugEvent function


## -description


Waits for a debugging event to occur in a process being debugged.
<div class="alert"><b>Important</b>  In the past, the operating system did not output Unicode strings via <b>OutputDebugStringW</b> and instead only output ASCII strings. To force <b>OutputDebugStringW</b> to correctly output Unicode strings, debuggers are required to call <a href="https://msdn.microsoft.com/2C79C4BE-9787-415E-AB82-1E33AB92D32F">WaitForDebugEventEx</a> to opt into the new behavior. On calling <b>WaitForDebugEventEx</b>, the operating system will know that the debugger supports Unicode and is specifically opting into receiving Unicode strings. </div><div> </div>

## -parameters




### -param lpDebugEvent [out]

A pointer to a 
<a href="https://msdn.microsoft.com/056aa7ee-51ca-48ec-9cd7-26085bb85b11">DEBUG_EVENT</a> structure that receives information about the debugging event.


### -param dwMilliseconds [in]

The number of milliseconds to wait for a debugging event. If this parameter is zero, the function tests for a debugging event and returns immediately. If the parameter is INFINITE, the function does not return until a debugging event has occurred.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Only the thread that created the process being debugged can call 
<b>WaitForDebugEvent</b>.

When a CREATE_PROCESS_DEBUG_EVENT occurs, the debugger application receives a handle to the image file of the process being debugged, a handle to the process being debugged, and a handle to the initial thread of the process being debugged in the 
<a href="https://msdn.microsoft.com/056aa7ee-51ca-48ec-9cd7-26085bb85b11">DEBUG_EVENT</a> structure. The members these handles are returned in are <b>u.CreateProcessInfo.hFile</b> (image file), <b>u.CreateProcessInfo.hProcess</b> (process), and <b>u.CreateProcessInfo.hThread</b> (initial thread). If the system previously reported an EXIT_PROCESS_DEBUG_EVENT debugging event, the system closes the handles to the process and thread when the debugger calls the 
<a href="https://msdn.microsoft.com/d15847d9-7947-4653-b3a2-3da1d1dd7078">ContinueDebugEvent</a> function. The debugger should close the handle to the image file by calling the 
<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function.

Similarly, when a CREATE_THREAD_DEBUG_EVENT occurs, the debugger application receives a handle to the thread whose creation caused the debugging event in the <b>u.CreateThread.hThread</b> member of the 
<a href="https://msdn.microsoft.com/056aa7ee-51ca-48ec-9cd7-26085bb85b11">DEBUG_EVENT</a> structure. If the system previously reported an EXIT_THREAD_DEBUG_EVENT debugging event, the system closes the handles to the thread when the debugger calls the 
<a href="https://msdn.microsoft.com/d15847d9-7947-4653-b3a2-3da1d1dd7078">ContinueDebugEvent</a> function.

When a LOAD_DLL_DEBUG_EVENT occurs, the debugger application receives a handle to the loaded DLL in the <b>u.LoadDll.hFile</b> member of the 
<a href="https://msdn.microsoft.com/056aa7ee-51ca-48ec-9cd7-26085bb85b11">DEBUG_EVENT</a> structure. This handle should be closed by the debugger application by calling the 
<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function.

<div class="alert"><b>Warning</b>  Do not queue an 
<a href="https://msdn.microsoft.com/0197d78e-a4dc-414b-88ba-c5ec5f2ed614">asynchronous procedure call</a> (APC) to a thread that calls 
<b>WaitForDebugEvent</b>.</div>
<div> </div>

#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/5a45854e-2711-49d5-982b-6b85248ec632">Writing the Debugger's Main Loop</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/d15847d9-7947-4653-b3a2-3da1d1dd7078">ContinueDebugEvent</a>



<a href="https://msdn.microsoft.com/056aa7ee-51ca-48ec-9cd7-26085bb85b11">DEBUG_EVENT</a>



<a href="https://msdn.microsoft.com/306a5b28-658a-4dab-a516-c638b73f4a77">DebugActiveProcess</a>



<a href="https://msdn.microsoft.com/1ca9d2d1-eed4-4982-8964-64b44e8be256">DebugBreak</a>



<a href="https://msdn.microsoft.com/43ca51f1-ba73-4031-96c3-5815311ce6f6">Debugging Events</a>



<a href="https://msdn.microsoft.com/95a838a2-f138-4682-b733-3f363b6c4a4b">Debugging Functions</a>



<a href="https://msdn.microsoft.com/ca23d9a9-65b7-4a36-bd09-857a6997f482">OutputDebugString</a>
 

 

