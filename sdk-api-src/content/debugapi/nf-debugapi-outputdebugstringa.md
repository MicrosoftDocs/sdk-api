---
UID: NF:debugapi.OutputDebugStringA
title: OutputDebugStringA function (debugapi.h)
author: windows-sdk-content
description: Sends a string to the debugger for display.
old-location: base\outputdebugstring.htm
tech.root: Debug
ms.assetid: ca23d9a9-65b7-4a36-bd09-857a6997f482
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: OutputDebugString, OutputDebugString function, OutputDebugStringA, OutputDebugStringW, _win32_outputdebugstring, base.outputdebugstring, debugapi/OutputDebugString, debugapi/OutputDebugStringA, debugapi/OutputDebugStringW
ms.topic: function
f1_keywords: 
 - "debugapi/OutputDebugString"
dev_langs:
 - c++
req.header: debugapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OutputDebugStringW (Unicode) and OutputDebugStringA (ANSI)
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
 - API-MS-Win-Core-debug-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-debug-l1-1-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Debug-L1-1-2.dll
api_name:
 - OutputDebugString
 - OutputDebugStringA
 - OutputDebugStringW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# OutputDebugStringA function


## -description


Sends a string to the debugger for display.
<div class="alert"><b>Important</b>  In the past, the operating system did not output Unicode strings via <b>OutputDebugStringW</b> and instead only output ASCII strings. To force <b>OutputDebugStringW</b> to correctly output Unicode strings, debuggers are required to call <a href="https://docs.microsoft.com/windows/desktop/api/debugapi/nf-debugapi-waitfordebugeventex">WaitForDebugEventEx</a> to opt into the new behavior. On calling <b>WaitForDebugEventEx</b>, the operating system will know that the debugger supports Unicode and is specifically opting into receiving Unicode strings. </div><div> </div>

## -parameters




### -param lpOutputString [in, optional]

The null-terminated string to be displayed.


## -returns



This function does not return a value.




## -remarks



If the application has no debugger, the system debugger displays the string if the filter mask allows it. (Note that this function calls the <b>DbgPrint</b> function to display the string. For details on how the filter mask controls what the system debugger displays, see the <b>DbgPrint</b> function in the Windows Driver Kit (WDK) on MSDN.) If the application has no debugger and the system debugger is not active, 
<b>OutputDebugString</b> does nothing.<b>Prior to Windows Vista:  </b>The system debugger does not filter content.



<b>OutputDebugStringW</b> converts the specified string based on the current system locale information and passes it to <b>OutputDebugStringA</b> to be displayed.  As a result, some Unicode characters may not be displayed correctly.

Applications should send very minimal debug output and provide a way for the user to enable or disable its use. To provide more detailed tracing, see <a href="https://docs.microsoft.com/windows/desktop/ETW/event-tracing-portal">Event Tracing</a>.

Visual Studio has changed how it handles the display of these strings throughout its revision history.  Refer to the Visual Studio documentation for details of how your version deals with this.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Debug/communicating-with-the-debugger">Communicating with the Debugger</a>



<a href="https://docs.microsoft.com/windows/desktop/Debug/debugging-functions">Debugging Functions</a>
 

 

