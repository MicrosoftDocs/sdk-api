---
UID: NF:werapi.WerRegisterRuntimeExceptionModule
title: WerRegisterRuntimeExceptionModule function
author: windows-sdk-content
description: Registers a custom runtime exception handler that is used to provide custom error reporting for crashes.
old-location: wer\werregisterruntimeexceptionmodule.htm
tech.root: wer
ms.assetid: b0fb2c0d-cc98-43cc-a508-e80545377b7f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WerRegisterRuntimeExceptionModule, WerRegisterRuntimeExceptionModule function [Windows Error Reporting], wer.werregisterruntimeexceptionmodule, werapi/WerRegisterRuntimeExceptionModule
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: werapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - API-MS-Win-Core-Windowserrorreporting-l1-1-0.dll
 - KernelBase.dll
api_name:
 - WerRegisterRuntimeExceptionModule
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WerRegisterRuntimeExceptionModule function


## -description


Registers a custom runtime exception handler that is used to provide custom error reporting for crashes.


## -parameters




### -param pwszOutOfProcessCallbackDll [in]

The name of the exception handler DLL to register. 


### -param pContext [in, optional]

A pointer to arbitrary context information that is passed to the handler's callback functions.


## -returns



This function returns <b>S_OK</b> on success or an error code on failure, including the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WER_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The process state is not valid. For example, the process is in <a href="https://msdn.microsoft.com/9357786c-1992-4e28-ac75-c2dfda1df7f1">application recovery mode</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)</b></dt>
</dl>
</td>
<td width="60%">
The number of registered runtime exception modules exceeds the limit. A process can register up to WER_MAX_REGISTERED_RUNTIME_EXCEPTION_MODULES handlers.

</td>
</tr>
</table>
 




## -remarks



The exception handler is an out-of-process DLL that the WER service loads when a crash or unhandled exception occurs. The DLL must implement and export the following functions:

<ul>
<li>
<a href="https://msdn.microsoft.com/22033278-2be3-4621-b618-3ccd21fb4cdd">OutOfProcessExceptionEventCallback</a>
</li>
<li>
<a href="https://msdn.microsoft.com/892498db-0265-4276-9735-63a8104ecaa9">OutOfProcessExceptionEventSignatureCallback</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ecf36951-cdb5-425d-a9b1-83b7ce8aebc4">OutOfProcessExceptionEventDebuggerLaunchCallback</a>
</li>
</ul>
(The DLL must also include the <a href="https://msdn.microsoft.com/0c3e3083-9297-4626-b2a7-0062d1c2cf9e">DllMain</a> entry point.)

Using an exception handler is more secure and reliable for reporting crash information than the current, in-process event reporting feature. Also, the current generic event reporting feature is suited only for reporting non-fatal errors.

This function requires that the <i>pwszOutOfProcessCallbackDll</i> DLL be included in the <a href="https://msdn.microsoft.com/031c5591-31b0-42f1-9a98-ecf10a5d5571">WER exception handler module list</a> in the registry. After registering an exception handler, if the process crashes or raises an unhandled exception, the WER service loads your exception handler and calls the <a href="https://msdn.microsoft.com/22033278-2be3-4621-b618-3ccd21fb4cdd">OutOfProcessExceptionEventCallback</a> callback function., which you use to state your claim on the crash and provide the event name and report parameters count. Note that if the process registers more than one exception handler, the service calls each handler until one of the handlers claims the crash. If no handlers claim the crash, WER defaults to native crash reporting.

If an exception handler claims the exception, the WER service calls the <a href="https://msdn.microsoft.com/892498db-0265-4276-9735-63a8104ecaa9">OutOfProcessExceptionEventSignatureCallback</a> callback function, which provides the reporting parameters that uniquely define the problem. Then, the WER service calls the <a href="https://msdn.microsoft.com/ecf36951-cdb5-425d-a9b1-83b7ce8aebc4">OutOfProcessExceptionEventDebuggerLaunchCallback</a> callback to determine whether to offer the user the option of launching  a debugger or launching the debugger automatically. The handler can also specify a custom debugger launch string, which will override the default string (the default is the debugger specified in the AeDebug registry key).

After the handler has provided the event name, reporting parameters and debugger launch settings, the rest of the error reporting flow continues in the usual way.

You must call the <a href="https://msdn.microsoft.com/1a315923-b554-4363-a607-076690fc76a1">WerUnregisterRuntimeExceptionModule</a> function to remove the registration before your process exits. A process can register up to WER_MAX_REGISTERED_RUNTIME_EXCEPTION_MODULES handlers.



