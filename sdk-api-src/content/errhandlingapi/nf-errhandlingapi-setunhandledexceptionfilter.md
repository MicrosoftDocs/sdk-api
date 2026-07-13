---
UID: NF:errhandlingapi.SetUnhandledExceptionFilter
title: SetUnhandledExceptionFilter function (errhandlingapi.h)
description: Enables an application to supersede the top-level exception handler of each thread of a process.
helpviewer_keywords: ["EXCEPTION_CONTINUE_EXECUTION","EXCEPTION_CONTINUE_SEARCH","EXCEPTION_EXECUTE_HANDLER","SetUnhandledExceptionFilter","SetUnhandledExceptionFilter function","_win32_setunhandledexceptionfilter","base.setunhandledexceptionfilter","errhandlingapi/SetUnhandledExceptionFilter"]
old-location: base\setunhandledexceptionfilter.htm
tech.root: Debug
ms.assetid: 1c3bfdda-8049-4c3f-8ee6-0ee5c77b50ae
ms.date: 02/02/2024
ms.keywords: EXCEPTION_CONTINUE_EXECUTION, EXCEPTION_CONTINUE_SEARCH, EXCEPTION_EXECUTE_HANDLER, SetUnhandledExceptionFilter, SetUnhandledExceptionFilter function, _win32_setunhandledexceptionfilter, base.setunhandledexceptionfilter, errhandlingapi/SetUnhandledExceptionFilter
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
 - SetUnhandledExceptionFilter
 - errhandlingapi/SetUnhandledExceptionFilter
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
 - SetUnhandledExceptionFilter
---

# SetUnhandledExceptionFilter function

## -description

Enables an application to supersede the top-level exception handler of each thread of a process.

After calling this function, if an exception occurs in a process that is not being debugged, and the exception makes it to the unhandled exception filter, that filter will call the exception filter function specified by the <i>lpTopLevelExceptionFilter</i> parameter.

## -parameters

### -param lpTopLevelExceptionFilter [in]

A pointer to a top-level exception filter function that will be called whenever the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter">UnhandledExceptionFilter</a> function gets control, and the process is not being debugged. A value of <b>NULL</b> for this parameter specifies default handling within <b>UnhandledExceptionFilter</b>.

The filter function has syntax similar to that of <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter">UnhandledExceptionFilter</a>: It takes a single parameter of type <b>LPEXCEPTION_POINTERS</b>, has a WINAPI calling convention, and returns a value of type <b>LONG</b>. The filter function should return one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EXCEPTION_EXECUTE_HANDLER"></a><a id="exception_execute_handler"></a><dl>
<dt><b>EXCEPTION_EXECUTE_HANDLER</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Return from 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter">UnhandledExceptionFilter</a> and execute the associated exception handler. This usually results in process termination.

</td>
</tr>
<tr>
<td width="40%"><a id="EXCEPTION_CONTINUE_EXECUTION"></a><a id="exception_continue_execution"></a><dl>
<dt><b>EXCEPTION_CONTINUE_EXECUTION</b></dt>
<dt>0xffffffff</dt>
</dl>
</td>
<td width="60%">
Return from 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter">UnhandledExceptionFilter</a> and continue execution from the point of the exception. Note that the filter function is free to modify the continuation state by modifying the exception information supplied through its <b>LPEXCEPTION_POINTERS</b> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="EXCEPTION_CONTINUE_SEARCH"></a><a id="exception_continue_search"></a><dl>
<dt><b>EXCEPTION_CONTINUE_SEARCH</b></dt>
<dt>0x0</dt>
</dl>
</td>
<td width="60%">
Proceed with normal execution of <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter">UnhandledExceptionFilter</a>. That means obeying the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode">SetErrorMode</a> flags, or invoking the Application Error pop-up message box.

</td>
</tr>
</table>

## -returns

The <b>SetUnhandledExceptionFilter</b> function returns the address of the previous exception filter established with the function. A <b>NULL</b> return value means that there is no current top-level exception handler.

## -remarks

Issuing <b>SetUnhandledExceptionFilter</b> replaces the existing top-level exception filter for all existing and all future threads in the calling process.

The exception handler specified by <i>lpTopLevelExceptionFilter</i> is executed in the context of the thread that caused the fault. This can affect the exception handler's ability to recover from certain exceptions, such as an invalid stack.

## -see-also

[Structured Exception Handling Functions](/windows/win32/Debug/structured-exception-handling-functions)

[Structured Exception Handling Overview](/windows/win32/Debug/structured-exception-handling)

[UnhandledExceptionFilter](nf-errhandlingapi-unhandledexceptionfilter.md)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
