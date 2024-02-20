---
UID: NF:debugapi.OutputDebugStringW
title: OutputDebugStringW function (debugapi.h)
description: Sends a string to the debugger for display. (Unicode)
helpviewer_keywords: ["OutputDebugString", "OutputDebugString function", "OutputDebugStringW", "_win32_outputdebugstring", "base.outputdebugstring", "debugapi/OutputDebugString", "debugapi/OutputDebugStringW"]
old-location: base\outputdebugstring.htm
tech.root: Debug
ms.assetid: ca23d9a9-65b7-4a36-bd09-857a6997f482
ms.date: 02/02/2024
ms.keywords: OutputDebugString, OutputDebugString function, OutputDebugStringA, OutputDebugStringW, _win32_outputdebugstring, base.outputdebugstring, debugapi/OutputDebugString, debugapi/OutputDebugStringA, debugapi/OutputDebugStringW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OutputDebugStringW
 - debugapi/OutputDebugStringW
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
 - vertdll.dll
api_name:
 - OutputDebugString
 - OutputDebugStringA
 - OutputDebugStringW
---

# OutputDebugStringW function

## -description

Sends a string to the debugger for display.

## -parameters

### -param lpOutputString [in, optional]

The null-terminated string to be displayed.

## -remarks

> [!IMPORTANT]
> To use this function, you must include the Windows.h header in your application (not debugapi.h).

In the past, the operating system did not return Unicode strings through **OutputDebugStringW** (ASCII strings were returned instead). To force **OutputDebugStringW** to return Unicode strings, debuggers are required to call the [**WaitForDebugEventEx**](nf-debugapi-waitfordebugeventex.md) function to opt into the new behavior. In this way, the operating system knows that the debugger supports Unicode and is specifically opting into receiving Unicode strings.

If the application does not have a debugger, and the filter mask allows it, the system debugger displays the string. To display the string, this function calls the [**DbgPrint**](/windows-hardware/drivers/ddi/wdm/nf-wdm-dbgprint) function. Prior to Windows Vista, content was not filtered by the system debugger.

If the application does not have a debugger and the system debugger is not active, **OutputDebugString** does nothing.

[**OutputDebugStringW**](nf-debugapi-outputdebugstringw.md) converts the specified string based on the current system locale information and passes it to **OutputDebugStringA** to be displayed.  As a result, some Unicode characters may not be displayed correctly.

Applications should send very minimal debug output and provide a way for the user to enable or disable its use. See [Event Tracing](/windows/win32/etw/event-tracing-portal) to learn more about tracing details.

Visual Studio has changed how it handles the display of these strings throughout its revision history. Refer to the Visual Studio documentation for details of how your version deals with this.

The debugapi.h header defines OutputDebugString as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches and compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

[Communicating with the Debugger](/windows/win32/debug/communicating-with-the-debugger)

[Debugging Functions](/windows/win32/debug/debugging-functions)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
