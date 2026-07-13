---
UID: NF:werapi.WerRegisterCustomMetadata
title: WerRegisterCustomMetadata function (werapi.h)
description: Registers app-specific metadata to be collected (in the form of key/value strings) for the Windows Error Reporting (WER) error report.
helpviewer_keywords: ["WerRegisterCustomMetadata","WerRegisterCustomMetadata function [Windows Error Reporting]","wer.werregistercustommetadata","werapi/WerRegisterCustomMetadata"]
old-location: wer\werregistercustommetadata.htm
tech.root: wer
ms.assetid: 55FB3110-314A-4327-AA8F-3AF77B7006DD
ms.date: 07/25/2023
ms.keywords: WerRegisterCustomMetadata, WerRegisterCustomMetadata function [Windows Error Reporting], wer.werregistercustommetadata, werapi/WerRegisterCustomMetadata
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
 - WerRegisterCustomMetadata
 - werapi/WerRegisterCustomMetadata
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
 - Kernel32.dll
 - API-MS-Win-Core-Windowserrorreporting-l1-1-1.dll
 - KernelBase.dll
api_name:
 - WerRegisterCustomMetadata
---

# WerRegisterCustomMetadata function

## -description

Registers app-specific metadata to be collected (in the form of key/value strings) for the [Windows Error Reporting](../_wer/index.md) (WER) error report.

## -parameters

### -param key

The "key" string for the metadata element being registered.

### -param value

The value string for the metadata element being registered.

## -returns

This function returns **S_OK** on success or an error code on failure, including the following error codes.

|Return code|Description|
|--- |--- |
|**E_INVALIDARG**|Strings were **NULL**, key length was greater than 64 characters or was an invalid xml element name, or *value* length was greater than 128 characters or contained characters that were not ASCII printable characters.|
|**E_OUTOFMEMORY**|WER could not allocate a large enough heap for the data|
|**HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)**|The maximum number of registered entries (**WER_MAX_REGISTERED_ENTRIES**) or  maximum amount of registered metadata (**WER_MAX_REGISTERED_METADATA**) has been reached.|
|**WER_E_INVALID_STATE**|The process state is not valid. For example, the process is in application recovery mode.|

## -remarks

This API allows apps to integrate their own app-level telemetry with system-level telemetry (WER) by associating app metadata with crash reports corresponding to their processes.

## -see-also

[WerUnregisterCustomMetadata](/windows/desktop/api/werapi/nf-werapi-werunregistercustommetadata), [Windows Error Reporting](/windows/desktop/wer)
