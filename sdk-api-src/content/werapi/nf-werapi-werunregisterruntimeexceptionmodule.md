---
UID: NF:werapi.WerUnregisterRuntimeExceptionModule
title: WerUnregisterRuntimeExceptionModule function
author: windows-sdk-content
description: Removes the registration of your WER exception handler.
old-location: wer\werunregisterruntimeexceptionmodule.htm
old-project: wer
ms.assetid: 1a315923-b554-4363-a607-076690fc76a1
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WerUnregisterRuntimeExceptionModule, WerUnregisterRuntimeExceptionModule function [Windows Error Reporting], wer.werunregisterruntimeexceptionmodule, werapi/WerUnregisterRuntimeExceptionModule
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WEB_SOCKET_PROPERTY, *PWEB_SOCKET_PROPERTY
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
 - WerUnregisterRuntimeExceptionModule
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WerUnregisterRuntimeExceptionModule function


## -description


Removes the registration of your WER exception handler.


## -parameters




### -param pwszOutOfProcessCallbackDll [in]

The name of the exception handler DLL whose registration you want to remove.


### -param pContext [in, optional]

A pointer to arbitrary context information that was passed to the callback.


## -returns



This function returns <b>S_OK</b> on success or an error code on failure, including the following error code.

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
<dt><b>WER_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The list of registered runtime exception handlers does not contain the specified exception handler.

</td>
</tr>
</table>
 




## -remarks



To register your runtime exception handler, call the <a href="https://msdn.microsoft.com/b0fb2c0d-cc98-43cc-a508-e80545377b7f">WerRegisterRuntimeExceptionModule</a> function.



