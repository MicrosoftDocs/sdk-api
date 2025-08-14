---
UID: NF:werapi.WerRegisterAdditionalProcess
title: WerRegisterAdditionalProcess function (werapi.h)
description: Registers a process to be included in the Windows Error Reporting (WER) report along with the main application process. Optionally specifies a thread within that registered process to get additional data from.
helpviewer_keywords: ["WerRegisterAdditionalProcess","WerRegisterAdditionalProcess function [Windows Error Reporting]","wer.werregisteradditionalprocess","werapi/WerRegisterAdditionalProcess"]
old-location: wer\werregisteradditionalprocess.htm
tech.root: wer
ms.assetid: F4E44C22-6BE1-4512-80F6-1B6741E3ADBB
ms.date: 07/25/2023
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
 - api-ms-win-core-windowserrorreporting-l1-1-3.dll
 - api-ms-win-core-windowserrorreporting-l1-1-2.dll
 - api-ms-win-core-windowserrorreporting-l1-1-1.dll
 - Kernel32.dll
 - API-MS-Win-Core-Windowserrorreporting-l1-1-0.dll
 - KernelBase.dll
api_name:
 - WerRegisterAdditionalProcess
---

# WerRegisterAdditionalProcess function

## -description

Registers a process to be included in the [Windows Error Reporting](../_wer/index.md) (WER) report along with the main application process. Optionally specifies a thread within that registered process to get additional data from.

## -parameters

### -param processId

The Id of the process to register.

### -param captureExtraInfoForThreadId [optional]

The Id of a thread within the registered process from which more information is requested.

## -returns

This function returns **S_OK** on success or an error code on failure, including the following error codes.

|Return code|Description|
|--- |--- |
|**E_INVALIDARG**|The value of *processId* is 0.|
|**E_OUTOFMEMORY**|WER could not allocate a large enough heap for the data.|
|**HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)**|Number of WER registered entries (memory blocks, metadata, files) exceeds max (**WER_MAX_REGISTERED_ENTRIES**) or number of processes exceeds max (**WER_MAX_REGISTERED_DUMPCOLLECTION**)|
|**WER_E_INVALID_STATE**|The process state is not valid. For example, the process is in application recovery mode.|

## -remarks

This API is for applications that have multiple processes interacting with each other. An application's main process would register the Id of another process. When the registering process crashes, WER will add an additional triage dump of the registered process to the resulting diagnostics. Optionally, the registering process can provide a thread Id as well to get more data for that specific thread.

## -see-also

[WerUnregisterAdditionalProcess](/windows/desktop/api/werapi/nf-werapi-werunregisteradditionalprocess), [Windows Error Reporting](/windows/desktop/wer)
