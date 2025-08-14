---
UID: NF:werapi.WerUnregisterAdditionalProcess
title: WerUnregisterAdditionalProcess function (werapi.h)
description: Removes a process from the list of additional processes to be included in the Windows Error Reporting (WER) error report.
helpviewer_keywords: ["WerUnregisterAdditionalProcess","WerUnregisterAdditionalProcess function [Windows Error Reporting]","wer.werunregisteradditionalprocess","werapi/WerUnregisterAdditionalProcess"]
old-location: wer\werunregisteradditionalprocess.htm
tech.root: wer
ms.assetid: CE840EE8-5EB6-4F0F-935E-5DA9097E950F
ms.date: 07/26/2023
ms.keywords: WerUnregisterAdditionalProcess, WerUnregisterAdditionalProcess function [Windows Error Reporting], wer.werunregisteradditionalprocess, werapi/WerUnregisterAdditionalProcess
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
 - WerUnregisterAdditionalProcess
 - werapi/WerUnregisterAdditionalProcess
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
 - WerUnregisterAdditionalProcess
---

# WerUnregisterAdditionalProcess function

## -description

Removes a process from the list of additional processes to be included in the [Windows Error Reporting](../_wer/index.md) (WER) error report.

## -parameters

### -param processId

The Id of the process to remove. It must have been previously registered with [WerRegisterAdditionalProcess](/windows/desktop/api/werapi/nf-werapi-werregisteradditionalprocess).

## -returns

This function returns **S_OK** on success or an error code on failure, including the following error codes.

|Return code|Description|
|--- |--- |
|**WER_E_INVALID_STATE**|The process state is not valid. For example, the process is in [application recovery mode](/windows/desktop/wsw/portal).|
|**WER_E_NOT_FOUND**|The list of registered processes does not contain the specified process.|

## -see-also

[WerRegisterAdditionalProcess](/windows/desktop/api/werapi/nf-werapi-werregisteradditionalprocess), [Windows Error Reporting](/windows/desktop/wer)
