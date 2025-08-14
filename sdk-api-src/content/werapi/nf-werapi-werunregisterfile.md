---
UID: NF:werapi.WerUnregisterFile
title: WerUnregisterFile function (werapi.h)
description: Removes a file from the list of files to be added to Windows Error Reporting (WER) reports generated for the current process.
helpviewer_keywords: ["WerUnregisterFile","WerUnregisterFile function [Windows Error Reporting]","base.werunregisterfile","wer.werunregisterfile","werapi/WerUnregisterFile"]
old-location: wer\werunregisterfile.htm
tech.root: wer
ms.assetid: 2b2684a4-3030-4fae-ad1c-a60d13d2c643
ms.date: 07/26/2023
ms.keywords: WerUnregisterFile, WerUnregisterFile function [Windows Error Reporting], base.werunregisterfile, wer.werunregisterfile, werapi/WerUnregisterFile
req.header: werapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - WerUnregisterFile
 - werapi/WerUnregisterFile
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
 - WerUnregisterFile
---

# WerUnregisterFile function

## -description

Removes a file from the list of files to be added to [Windows Error Reporting](../_wer/index.md) (WER) reports generated for the current process.

## -parameters

### -param pwzFilePath [in]

The full path to the file. This file must have been registered using the [WerRegisterFile](/windows/desktop/api/werapi/nf-werapi-werregisterfile) function.

## -returns

This function returns **S_OK** on success or an error code on failure, including the following error code.

|Return code|Description|
|--- |--- |
|**WER_E_INVALID_STATE**|The process state is not valid. For example, the process is in application recovery mode.|
|**WER_E_NOT_FOUND**|The list of registered files does not contain the specified file.|

## -see-also

[WerRegisterFile](/windows/desktop/api/werapi/nf-werapi-werregisterfile), [Windows Error Reporting](/windows/desktop/wer)
