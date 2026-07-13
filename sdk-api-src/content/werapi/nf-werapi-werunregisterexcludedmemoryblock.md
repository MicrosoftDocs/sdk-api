---
UID: NF:werapi.WerUnregisterExcludedMemoryBlock
title: WerUnregisterExcludedMemoryBlock function (werapi.h)
description: Removes a memory block that was previously marked as excluded, which will again be included in Windows Error Reporting] (WER) error reports.
helpviewer_keywords: ["WerUnregisterExcludedMemoryBlock","WerUnregisterExcludedMemoryBlock function [Windows Error Reporting]","wer.werunregisterexcludedmemoryblock","werapi/WerUnregisterExcludedMemoryBlock"]
old-location: wer\werunregisterexcludedmemoryblock.htm
tech.root: wer
ms.assetid: 99FF746E-8EFC-47DB-AEE6-EC46F7BC7F0B
ms.date: 07/26/2023
ms.keywords: WerUnregisterExcludedMemoryBlock, WerUnregisterExcludedMemoryBlock function [Windows Error Reporting], wer.werunregisterexcludedmemoryblock, werapi/WerUnregisterExcludedMemoryBlock
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
 - WerUnregisterExcludedMemoryBlock
 - werapi/WerUnregisterExcludedMemoryBlock
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
 - WerUnregisterExcludedMemoryBlock
---

# WerUnregisterExcludedMemoryBlock function

## -description

Removes a memory block that was previously marked as excluded, which will again be included in [Windows Error Reporting](../_wer/index.md) (WER) error reports.

## -parameters

### -param address

The starting address of the memory block. This memory block must have been registered using the [WerRegisterExcludedMemoryBlock](/windows/desktop/api/werapi/nf-werapi-werregisterexcludedmemoryblock) function.

## -returns

This function returns **S_OK** on success or an error code on failure, including the following error code.

|Return code|Description|
|--- |--- |
|**WER_E_INVALID_STATE**|The process state is not valid. For example, the process is in application recovery mode.|

## -see-also

[WerRegisterExcludedMemoryBlock](/windows/desktop/api/werapi/nf-werapi-werregisterexcludedmemoryblock), [Windows Error Reporting](/windows/desktop/wer)
