---
UID: NF:errhandlingapi.UnhandledExceptionFilter
title: UnhandledExceptionFilter function (errhandlingapi.h)
author: windows-sdk-content
description: An application-defined function that passes unhandled exceptions to the debugger, if the process is being debugged.
old-location: base\unhandledexceptionfilter.htm
tech.root: Debug
ms.assetid: 9221e99b-6900-4b5d-923c-352bb27a5f8b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: UnhandledExceptionFilter, UnhandledExceptionFilter function, _win32_unhandledexceptionfilter, base.unhandledexceptionfilter, errhandlingapi/UnhandledExceptionFilter
ms.topic: function
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
api_name:
 - UnhandledExceptionFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UnhandledExceptionFilter function


## -description


An application-defined function that passes unhandled exceptions to the debugger, if the process is being debugged. Otherwise, it optionally displays an <b>Application Error</b> message box and causes the exception handler to be executed. This function can be called only from within the filter expression of an exception handler.


## -parameters




### -param ExceptionInfo [in]

A pointer to an 
<a href="https://msdn.microsoft.com/57e8cb3a-1b11-45b9-9676-3b6dc600d225">EXCEPTION_POINTERS</a> structure that specifies a description of the exception and the processor context at the time of the exception. This pointer is the return value of a call to the 
<a href="https://msdn.microsoft.com/e982794a-d5f1-4fb4-a2b9-aa8da18cb8ae">GetExceptionInformation</a> function.


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
<a href="https://msdn.microsoft.com/b88f5577-9124-433c-a7e8-a7f713b7b27d">SetErrorMode</a>, no Application Error message box is displayed. The function returns control to the exception handler, which is free to take any appropriate action.

</td>
</tr>
</table>
 




## -remarks



If the process is not being debugged, the function displays an <b>Application Error</b> message box, depending on the current error mode. The default behavior is to display the dialog box, but this can be disabled by specifying SEM_NOGPFAULTERRORBOX in a call to the 
<a href="https://msdn.microsoft.com/b88f5577-9124-433c-a7e8-a7f713b7b27d">SetErrorMode</a> function.

The system uses 
<b>UnhandledExceptionFilter</b> internally to handle exceptions that occur during process and thread creation.




## -see-also




<a href="https://msdn.microsoft.com/57e8cb3a-1b11-45b9-9676-3b6dc600d225">EXCEPTION_POINTERS</a>



<a href="https://msdn.microsoft.com/e982794a-d5f1-4fb4-a2b9-aa8da18cb8ae">GetExceptionInformation</a>



<a href="https://msdn.microsoft.com/b88f5577-9124-433c-a7e8-a7f713b7b27d">SetErrorMode</a>



<a href="https://msdn.microsoft.com/1c3bfdda-8049-4c3f-8ee6-0ee5c77b50ae">SetUnhandledExceptionFilter</a>



<a href="https://msdn.microsoft.com/61cf055b-eb9a-4e56-9d36-21fc95adea77">Structured Exception Handling Functions</a>



<a href="https://msdn.microsoft.com/6b6326d8-6875-4146-a4e3-7873f4e400cb">Structured Exception Handling Overview</a>
 

 

