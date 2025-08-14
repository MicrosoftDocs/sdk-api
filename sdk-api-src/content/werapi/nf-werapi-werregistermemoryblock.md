---
UID: NF:werapi.WerRegisterMemoryBlock
title: WerRegisterMemoryBlock function (werapi.h)
description: Registers a memory block to be collected when Windows Error Reporting (WER) creates an error report.
helpviewer_keywords: ["WerRegisterMemoryBlock","WerRegisterMemoryBlock function [Windows Error Reporting]","base.werregistermemoryblock","wer.werregistermemoryblock","werapi/WerRegisterMemoryBlock"]
old-location: wer\werregistermemoryblock.htm
tech.root: wer
ms.assetid: 10fa2bf3-ec12-4c7c-b986-9b22cdaa7319
ms.date: 07/25/2023
ms.keywords: WerRegisterMemoryBlock, WerRegisterMemoryBlock function [Windows Error Reporting], base.werregistermemoryblock, wer.werregistermemoryblock, werapi/WerRegisterMemoryBlock
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
 - WerRegisterMemoryBlock
 - werapi/WerRegisterMemoryBlock
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
 - WerRegisterMemoryBlock
---

# WerRegisterMemoryBlock function

## -description

Registers a memory block to be collected when [Windows Error Reporting](../_wer/index.md) (WER) creates an error report.

## -parameters

### -param pvAddress [in]

The starting address of the memory block.

### -param dwSize [in]

The size of the memory block, in bytes. The maximum value for this parameter is WER_MAX_MEM_BLOCK_SIZE bytes.

## -returns

This function returns **S_OK** on success or an error code on failure, including the following error codes.

|Return code|Description|
|--- |--- |
|**WER_E_INVALID_STATE**|The process state is not valid. For example, the process is in application recovery mode.|
|**HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)**|The number of registered memory blocks and files exceeds the limit.|

## -remarks

Memory registered with this function is only added to heap or larger dump files. This memory is never added to mini dumps or smaller dump files.

For crashes and no response, the operating system automatically provides error reporting (you do not need to provide any error reporting code in your application). If you use this function to register a memory block, the operating system will add the memory block information to the dump file at the time of the crash or non-response. The memory block is added to the dump file for the report only when additional data is requested by the server.

For generic event reporting, the application has to call the WER generic event reporting functions directly. To add the memory block to a generic report, call the [WerReportAddDump](/windows/desktop/api/werapi/nf-werapi-werreportadddump) function and then call the [WerReportSubmit](/windows/desktop/api/werapi/nf-werapi-werreportsubmit) function and specify the  WER_SUBMIT_ADD_REGISTERED_DATA flag.

To remove the block from this list, call the [WerUnregisterMemoryBlock](/windows/desktop/api/werapi/nf-werapi-werunregistermemoryblock) function.

## -see-also

[WerUnregisterMemoryBlock](/windows/desktop/api/werapi/nf-werapi-werunregistermemoryblock), [Windows Error Reporting](/windows/desktop/wer)
