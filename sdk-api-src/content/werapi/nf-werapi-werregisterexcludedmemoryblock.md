---
UID: NF:werapi.WerRegisterExcludedMemoryBlock
title: WerRegisterExcludedMemoryBlock function (werapi.h)
description: Marks a memory block (that is normally included by default in error reports) to be excluded from the error report.
helpviewer_keywords: ["WerRegisterExcludedMemoryBlock","WerRegisterExcludedMemoryBlock function [Windows Error Reporting]","wer.werregisterexcludedmemoryblock","werapi/WerRegisterExcludedMemoryBlock"]
old-location: wer\werregisterexcludedmemoryblock.htm
tech.root: wer
ms.assetid: 6CDA8EDD-C8A5-471D-9716-3AB29E571133
ms.date: 12/05/2018
ms.keywords: WerRegisterExcludedMemoryBlock, WerRegisterExcludedMemoryBlock function [Windows Error Reporting], wer.werregisterexcludedmemoryblock, werapi/WerRegisterExcludedMemoryBlock
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
 - WerRegisterExcludedMemoryBlock
 - werapi/WerRegisterExcludedMemoryBlock
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
 - WerRegisterExcludedMemoryBlock
---

# WerRegisterExcludedMemoryBlock function


## -description

Marks a memory block (that is normally included by default in error reports) to be excluded from the error report.

## -parameters

### -param address

The starting address of the memory block.

### -param size

The size of the memory block, in bytes.

## -returns

This function returns **S_OK** on success or an error code on failure, including the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>**E_INVALIDARG**</dt>
</dl>
</td>
<td width="60%">
*address* is **NULL** or *size* is 0.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>**E_OUTOFMEMORY**</dt>
</dl>
</td>
<td width="60%">
WER could not allocate a large enough heap for the data

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>**HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)**</dt>
</dl>
</td>
<td width="60%">
The number of registered entries exceeds the limit (**WER_MAX_REGISTERED_ENTRIES**).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>**WER_E_INVALID_STATE**</dt>
</dl>
</td>
<td width="60%">
The process state is not valid. For example, the process is in <a href="/windows/desktop/wsw/portal">application recovery mode</a>.

</td>
</tr>
</table>

## -remarks

This mechanism is intended for applications that hold large amounts of data in memory that aren't useful for root cause debugging and increase the size of the dump file unnecessarily.  For example, some Xbox One games hold large amounts of texture data in memory that is included in error dumps by default.

## -see-also




<a href="/windows/desktop/api/werapi/nf-werapi-werunregisterexcludedmemoryblock">WerUnregisterExcludedMemoryBlock</a>



[Windows Error Reporting](/windows/desktop/wer)