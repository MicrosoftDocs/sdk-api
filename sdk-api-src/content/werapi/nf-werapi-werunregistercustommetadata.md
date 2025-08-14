---
UID: NF:werapi.WerUnregisterCustomMetadata
title: WerUnregisterCustomMetadata function (werapi.h)
description: Removes an item of app-specific metadata being collected during Windows Error Reporting (WER) for the application.
helpviewer_keywords: ["WerUnRegisterCustomMetadata","WerUnRegisterCustomMetadata function [Windows Error Reporting]","WerUnregisterCustomMetadata","wer.werunregistercustommetadata","werapi/WerUnRegisterCustomMetadata"]
old-location: wer\werunregistercustommetadata.htm
tech.root: wer
ms.assetid: 29DB2CE5-2A96-450B-96C8-082B786613F9
ms.date: 07/26/2023
ms.keywords: WerUnRegisterCustomMetadata, WerUnRegisterCustomMetadata function [Windows Error Reporting], WerUnregisterCustomMetadata, wer.werunregistercustommetadata, werapi/WerUnRegisterCustomMetadata
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
 - WerUnregisterCustomMetadata
 - werapi/WerUnregisterCustomMetadata
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
 - API-MS-Win-Core-Windowserrorreporting-l1-1-0.dll
 - api-ms-win-core-windowserrorreporting-l1-1-1.dll
 - KernelBase.dll
api_name:
 - WerUnRegisterCustomMetadata
---

# WerUnregisterCustomMetadata function

## -description

Removes an item of app-specific metadata being collected during [Windows Error Reporting](../_wer/index.md) (WER) for the application.

## -parameters

### -param key

The "key" string for the metadata element being removed. It must have been previously registered with the [WerRegisterCustomMetadata](/windows/desktop/api/werapi/nf-werapi-werregistercustommetadata) function.

## -returns

This function returns **S_OK** on success or an error code on failure, including the following error codes.

|Return code|Description|
|--- |--- |
|**WER_E_INVALID_STATE**|The process state is not valid. For example, the process is in application recovery mode.|
|**WER_E_NOT_FOUND**|WER could not find the metadata item to remove.|

## -see-also

[WerRegisterCustomMetadata](/windows/desktop/api/werapi/nf-werapi-werregistercustommetadata), [Windows Error Reporting](/windows/desktop/wer)