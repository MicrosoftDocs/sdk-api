---
UID: NF:errhandlingapi.UnhandledExceptionFilter
title: UnhandledExceptionFilter function (errhandlingapi.h)
description: An application-defined function that passes unhandled exceptions to the debugger, if the process is being debugged.
helpviewer_keywords: ["UnhandledExceptionFilter","UnhandledExceptionFilter function","_win32_unhandledexceptionfilter","base.unhandledexceptionfilter","errhandlingapi/UnhandledExceptionFilter"]
old-location: base\unhandledexceptionfilter.htm
tech.root: Debug
ms.assetid: 9221e99b-6900-4b5d-923c-352bb27a5f8b
ms.date: 12/05/2018
ms.keywords: UnhandledExceptionFilter, UnhandledExceptionFilter function, _win32_unhandledexceptionfilter, base.unhandledexceptionfilter, errhandlingapi/UnhandledExceptionFilter
req.header: errhandlingapi.h
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
 - UnhandledExceptionFilter
 - errhandlingapi/UnhandledExceptionFilter
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
 - ntdll.dll
api_name:
 - UnhandledExceptionFilter
 - RtlUnhandledExceptionFilter
---

# UnhandledExceptionFilter function


## -description

An application-defined function that passes unhandled exceptions to the debugger, if the process is being debugged. Otherwise, it optionally displays an <b>Application Error</b> message box and causes the exception handler to be executed. This function can be called only from within the filter expression of an exception handler.

## -parameters

### -param ExceptionInfo [in]

A pointer to an 
<a href="/windows/desktop/api/winnt/ns-winnt-exception_pointers">EXCEPTION_POINTERS</a> structure that specifies a description of the exception and the processor context at the time of the exception. This pointer is the return value of a call to the 
<a href="/windows/desktop/Debug/getexceptioninformation">GetExceptionInformation</a> function.

## -returns

The function returns one of the following values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>EXCEPTION_CONTINUE_SEARCH</b></dt>
<dt>0x0</dt>
</dl>
</td>
<td width="60%">
The process is being debugged, so the exception should be passed (as second chance) to the application's debugger.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>EXCEPTION_EXECUTE_HANDLER</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
If the SEM_NOGPFAULTERRORBOX flag was specified in a previous call to 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode">SetErrorMode</a>, no Application Error message box is displayed. The function returns control to the exception handler, which is free to take any appropriate action.

</td>
</tr>
</table>

## -remarks

If the process is not being debugged, the function displays an <b>Application Error</b> message box, depending on the current error mode. The default behavior is to display the dialog box, but this can be disabled by specifying SEM_NOGPFAULTERRORBOX in a call to the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode">SetErrorMode</a> function.

The system uses 
<b>UnhandledExceptionFilter</b> internally to handle exceptions that occur during process and thread creation.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-exception_pointers">EXCEPTION_POINTERS</a>



<a href="/windows/desktop/Debug/getexceptioninformation">GetExceptionInformation</a>



<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode">SetErrorMode</a>



<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setunhandledexceptionfilter">SetUnhandledExceptionFilter</a>



<a href="/windows/desktop/Debug/structured-exception-handling-functions">Structured Exception Handling Functions</a>



<a href="/windows/desktop/Debug/structured-exception-handling">Structured Exception Handling Overview</a>