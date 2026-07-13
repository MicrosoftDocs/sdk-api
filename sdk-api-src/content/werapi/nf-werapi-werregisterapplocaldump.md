---
UID: NF:werapi.WerRegisterAppLocalDump
title: WerRegisterAppLocalDump function (werapi.h)
description: Registers a path (relative to the LocalFolder of the packaged application) where a copy should be saved of the diagnostic memory dump that Windows Error Reporting (WER) collects when one of the processes for the application stops responding.
helpviewer_keywords: ["WerRegisterAppLocalDump","WerRegisterAppLocalDump function [Windows Error Reporting]","wer.werregisterapplocaldump","werapi/WerRegisterAppLocalDump"]
old-location: wer\werregisterapplocaldump.htm
tech.root: wer
ms.assetid: C57F5758-2BF7-444E-A22C-62C925B899A1
ms.date: 07/25/2023
ms.keywords: WerRegisterAppLocalDump, WerRegisterAppLocalDump function [Windows Error Reporting], wer.werregisterapplocaldump, werapi/WerRegisterAppLocalDump
req.header: werapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps \| UWP apps]
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
req.dll: KernelBase.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WerRegisterAppLocalDump
 - werapi/WerRegisterAppLocalDump
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
 - KernelBase.dll
 - Kernel32.dll
 - Api-ms-win-core-windowserrorreporting-l1.dll
api_name:
 - WerRegisterAppLocalDump
---

# WerRegisterAppLocalDump function

## -description

Registers a path (relative to the [LocalFolder](/uwp/api/windows.storage.applicationdata.localfolder) of the packaged application) where a copy should be saved of the diagnostic memory dump that [Windows Error Reporting](../_wer/index.md) (WER) collects when one of the processes for the application stops responding.

## -parameters

### -param localAppDataRelativePath [in]

The path relative to the local app store for the calling application. This is where a copy is saved of the diagnostic memory dump that WER collects when one of the processes for the application stops responding. The maximum length for this relative path in characters is **WER_MAX_LOCAL_DUMP_SUBPATH_LENGTH**, which has a value of 64. This maximum length includes the null-termination character.

## -returns

This function returns **S_OK** on success or an error code on failure, including the following error codes.

|Return code|Description|
|--- |--- |
|**WER_E_INVALID_STATE**|The process cannot store the memory dump, or WER cannot create a location to store the memory dump.|
|**E_INVALIDARG**|The *localAppDataRelativePath* parameter is NULL or is longer than 64 characters.|

## -remarks

A packaged application calls **WerRegisterAppLocalDump** when the application launches to request a copy of the diagnostic memory dump that WER collects if or when one of the processes for the application stops responding.

WER does not manage storage at the location that the relative path specifies or the number of memory dumps that are collected for the application.

## -see-also

[WerUnregisterAppLocalDump function](nf-werapi-werunregisterapplocaldump.md), [Windows Error Reporting](/windows/desktop/wer)
