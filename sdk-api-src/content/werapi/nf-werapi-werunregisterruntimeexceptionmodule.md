---
UID: NF:werapi.WerUnregisterRuntimeExceptionModule
title: WerUnregisterRuntimeExceptionModule function (werapi.h)
description: Removes the registration of your WER exception handler.
helpviewer_keywords: ["WerUnregisterRuntimeExceptionModule","WerUnregisterRuntimeExceptionModule function [Windows Error Reporting]","wer.werunregisterruntimeexceptionmodule","werapi/WerUnregisterRuntimeExceptionModule"]
old-location: wer\werunregisterruntimeexceptionmodule.htm
tech.root: wer
ms.assetid: 1a315923-b554-4363-a607-076690fc76a1
ms.date: 12/05/2018
ms.keywords: WerUnregisterRuntimeExceptionModule, WerUnregisterRuntimeExceptionModule function [Windows Error Reporting], wer.werunregisterruntimeexceptionmodule, werapi/WerUnregisterRuntimeExceptionModule
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WerUnregisterRuntimeExceptionModule
 - werapi/WerUnregisterRuntimeExceptionModule
dev_langs:
 - c++
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
The process state is not valid. For example, the process is in <a href="/windows/desktop/wsw/portal">application recovery mode</a>.

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

To register your runtime exception handler, call the <a href="/windows/desktop/api/werapi/nf-werapi-werregisterruntimeexceptionmodule">WerRegisterRuntimeExceptionModule</a> function.