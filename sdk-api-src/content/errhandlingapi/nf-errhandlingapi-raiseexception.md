---
UID: NF:errhandlingapi.RaiseException
title: RaiseException function (errhandlingapi.h)
description: Raises an exception in the calling thread.
helpviewer_keywords: ["RaiseException","RaiseException function","_win32_raiseexception","base.raiseexception","errhandlingapi/RaiseException"]
old-location: base\raiseexception.htm
tech.root: Debug
ms.assetid: 47c3c85e-15ca-4645-89c1-bbfd3bbd58e5
ms.date: 02/02/2024
ms.keywords: RaiseException, RaiseException function, _win32_raiseexception, base.raiseexception, errhandlingapi/RaiseException
req.header: errhandlingapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
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
 - RaiseException
 - errhandlingapi/RaiseException
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-errorhandling-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-errorhandling-l1-1-1.dll
 - API-MS-Win-Core-errorhandling-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ErrorHandling-L1-1-3.dll
 - vertdll.dll
api_name:
 - RaiseException
---

# RaiseException function

## -description

Raises an exception in the calling thread.

## -parameters

### -param dwExceptionCode [in]

An application-defined exception code of the exception being raised. The filter expression and exception-handler block of an exception handler can use the <a href="/windows/desktop/Debug/getexceptioncode">GetExceptionCode</a> function to retrieve this value.

Note that the system will clear bit 28 of <i>dwExceptionCode</i> before displaying a message This bit is a reserved exception bit, used by the system for its own purposes.

### -param dwExceptionFlags [in]

The exception flags. This can be either zero to indicate a continuable exception, or EXCEPTION_NONCONTINUABLE to indicate a noncontinuable exception. Any attempt to continue execution after a noncontinuable exception causes the EXCEPTION_NONCONTINUABLE_EXCEPTION exception.

### -param nNumberOfArguments [in]

The number of arguments in the <i>lpArguments</i> array. This value must not exceed EXCEPTION_MAXIMUM_PARAMETERS. This parameter is ignored if <i>lpArguments</i> is <b>NULL</b>.

### -param lpArguments [in]

An array of arguments. This parameter can be <b>NULL</b>. These arguments can contain any application-defined data that needs to be passed to the filter expression of the exception handler.

## -returns

This function does not return a value.

## -remarks

The <b>RaiseException</b> function enables a process to use structured exception handling to handle private, software-generated, application-defined exceptions.

Raising an exception causes the exception dispatcher to go through the following search for an exception handler:

<ol>
<li>The system first attempts to notify the process's debugger, if any.</li>
<li>If the process is not being debugged, or if the associated debugger does not handle the exception, the system attempts to locate a frame-based exception handler by searching the stack frames of the thread in which the exception occurred. The system searches the current stack frame first, then proceeds backward through preceding stack frames.</li>
<li>If no frame-based handler can be found, or no frame-based handler handles the exception, the system makes a second attempt to notify the process's debugger.</li>
<li>If the process is not being debugged, or if the associated debugger does not handle the exception, the system provides default handling based on the exception type. For most exceptions, the default action is to call the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitprocess">ExitProcess</a> function.</li>
</ol>

The values specified in the <i>dwExceptionCode</i>, <i>dwExceptionFlags</i>, <i>nNumberOfArguments</i>, and <i>lpArguments</i> parameters can be retrieved in the filter expression of a frame-based exception handler by calling the <a href="/windows/desktop/Debug/getexceptioninformation">GetExceptionInformation</a> function. A debugger can retrieve these values by calling the <a href="/windows/desktop/api/debugapi/nf-debugapi-waitfordebugevent">WaitForDebugEvent</a> function.

#### Examples

For an example, see <a href="/windows/desktop/Debug/using-an-exception-handler">Using an Exception Handler</a>.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitprocess">ExitProcess</a>

<a href="/windows/desktop/Debug/getexceptioncode">GetExceptionCode</a>

<a href="/windows/desktop/Debug/getexceptioninformation">GetExceptionInformation</a>

<a href="/windows/desktop/Debug/structured-exception-handling-functions">Structured Exception Handling Functions</a>

<a href="/windows/desktop/Debug/structured-exception-handling">Structured Exception Handling Overview</a>

<a href="/windows/desktop/api/debugapi/nf-debugapi-waitfordebugevent">WaitForDebugEvent</a>

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
