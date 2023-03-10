---
UID: NF:werapi.WerRegisterAdditionalProcess
title: WerRegisterAdditionalProcess function (werapi.h)
description: Registers a process to be included in the error report along with the main application process. Optionally specifies a thread within that registered process to get additional data from.
helpviewer_keywords: ["WerRegisterAdditionalProcess","WerRegisterAdditionalProcess function [Windows Error Reporting]","wer.werregisteradditionalprocess","werapi/WerRegisterAdditionalProcess"]
old-location: wer\werregisteradditionalprocess.htm
tech.root: wer
ms.assetid: F4E44C22-6BE1-4512-80F6-1B6741E3ADBB
ms.date: 12/05/2018
ms.keywords: WerRegisterAdditionalProcess, WerRegisterAdditionalProcess function [Windows Error Reporting], wer.werregisteradditionalprocess, werapi/WerRegisterAdditionalProcess
req.header: werapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
 - WerRegisterAdditionalProcess
 - werapi/WerRegisterAdditionalProcess
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
 - WerRegisterAdditionalProcess
---

# WerRegisterAdditionalProcess function


## -description

Registers a process to be included in the error report along with the main application process. Optionally specifies a thread within that registered process to get additional data from.

## -parameters

### -param processId

The Id of the process to register.

### -param captureExtraInfoForThreadId [optional]

The Id of a thread within the registered process from which more information is requested.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>processId</i> is 0.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
WER could not allocate a large enough heap for the data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)</b></dt>
</dl>
</td>
<td width="60%">
Number of WER registered entries (memory blocks, metadata, files) exceeds max (<b>WER_MAX_REGISTERED_ENTRIES</b>) or number of processes exceeds max (<b>WER_MAX_REGISTERED_DUMPCOLLECTION</b>)

</td>
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
</table>

## -remarks

This API is for applications that have multiple processes interacting with each other. An application's main process would register the Id of another process. When the registering process crashes, WER will add an additional triage dump of the registered process to the resulting diagnostics. Optionally, the registering process can provide a thread Id as well to get more data for that specific thread.

## -see-also

<a href="/windows/desktop/wer/wer-functions">WER Functions</a>



<a href="/windows/desktop/api/werapi/nf-werapi-werunregisteradditionalprocess">WerUnregisterAdditionalProcess</a>



<a href="/windows/desktop/wer/windows-error-reporting">Windows Error Reporting</a>